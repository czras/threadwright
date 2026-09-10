---
name: feature-workflow
description: Orchestrate the full feature development workflow. Use when user says "start feature <TICKET>", "new feature", "init feature", or wants to run the feature workflow. Handles init, decisions, planning, implementation, review, fix, and rebase phases.
---

# Feature Workflow Orchestrator

Coordinate the feature development workflow by spawning subagents for each phase.

## Workflow

### 1. Extract JIRA ticket ID

Parse the ticket ID from the user's prompt (e.g., `EVPP-620`).

### 1b. Fetch and save JIRA ticket

Use `jira_get_issue` to fetch the ticket. Extract and save the following to:
```
.workflow/feature_<TICKET>_<slug>/jira_ticket.md
```

Where `<TICKET>` is the ticket ID and `<slug>` is derived from the summary (lowercased, spaces→hyphens, special chars removed).

The file format:

```markdown
# JIRA Ticket: <TICKET>

## Link
[<TICKET>](<JIRA_URL>)

## Summary
<ticket summary>

## Description
<ticket description>

## Fix Versions
- <version 1>
- <version 2>

## Related Tickets
- <LINK_TYPE> <TICKET-KEY> - <summary>
- <LINK_TYPE> <TICKET-KEY> - <summary>
```

Include all linked/related issues from the ticket (e.g., "is blocked by", "relates to", "is caused by"). If there are no fix versions or related tickets, write "None" under the respective heading.

Create the workflow directory if it doesn't exist:
```bash
mkdir -p .workflow/feature_<TICKET>_<slug>
```

### 2. Initialize feature branch

Spawn `feature_init` subagent with prompt "Initialize feature branch for <TICKET>". Wait for completion.

The JIRA ticket has already been fetched and saved to `jira_ticket.md` — the init subagent reads it from there instead of calling JIRA directly.

The init subagent writes the base branch and feature branch to `init.md`:

```markdown
# Feature Init: <TICKET>

## Feature Branch
<feature_branch>

## Base Branch
<base_branch>
```

All later stages read the branch information from `init.md` — do not re-derive it or ask the user again.

### 3. Explore codebase

Determine the feature branch slug by reading `.workflow/feature_<TICKET>_<slug>/init.md` (the part of the feature branch name after `feature/`).

Check if the codebase context file already exists:
```
.workflow/feature_<TICKET>_<slug>/codebase_context.md
```

If the file exists, skip codebase exploration and proceed to step 4.

If the file does not exist, spawn `jetbrains_explore` subagent with prompt:
"Explore codebase for feature <TICKET>. Find: project structure, related modules, existing patterns, conventions, test infrastructure. Based on JIRA ticket summary: <SUMMARY>"

Save the exploration results to:
```
.workflow/feature_<TICKET>_<slug>/codebase_context.md
```

This file will be read by subagents that need codebase context (decisions, plan, implement).

### 4. Detect partially completed workflow

Check which directory exists in `.workflow/`:
- `feature_<TICKET>_<slug>/init.md`
- `feature_<TICKET>_<slug>/jira_ticket.md`
- `feature_<TICKET>_<slug>/codebase_context.md`
- `feature_<TICKET>_<slug>/decisions.md`
- `feature_<TICKET>_<slug>/plan.md`
- `feature_<TICKET>_<slug>/review.md`

If `init.md` exists, read it to get the base branch and feature branch. If `init.md` is missing, run the init phase (step 2) to create it before continuing.

Check git log for commits on feature branch:
```bash
git log --oneline <base_branch>..<feature_branch>
```

If plan file exists, read it and compare implemented phases against commits.

### 5. Determine resume point and offer options

- **No files, no commits**: Offer (1) Run grill-me session (recommended), (2) Skip to planning
- **Only decisions file**: Offer (1) Continue to planning, (2) Re-run decisions
- **Plan file exists, no commits**: Offer (1) Continue to implementation, (2) Re-run planning
- **Plan exists with partial commits**: Offer (1) Continue implementing remaining phases, (2) Re-run implementation from start, (3) Re-run planning
- **Plan fully implemented, no review**: Offer (1) Continue to review, (2) Re-run implementation
- **Review exists, no Requested Fixes section**: Offer (1) Continue to rebase (if fixup commits exist), (2) Re-run review
- **Review exists with Requested Fixes, no fixup commits**: Offer (1) Continue to fix implementation, (2) Re-run review
- **Review exists with Requested Fixes and partial fixup commits**: Offer (1) Continue implementing remaining fixes, (2) Re-run fix implementation from start, (3) Re-run review
- **All fixes implemented (all checkboxes checked)**: Offer (1) Continue to rebase, (2) Re-run fix implementation
- **No fixup commits**: Skip rebase, report workflow complete

Use the `question` tool to present options to the user.

### 6. Execute chosen phase

Based on user selection, spawn the appropriate subagent:

#### Decisions Phase
- Spawn `feature_decisions` subagent with prompt "Run grill-me session for <TICKET>"
- Focus: discover gaps in requirements and align on design approach (functionality + architecture)
- Wait for completion

#### Planning Phase
- Spawn `feature_plan` subagent with prompt "Create implementation plan for <TICKET>"
- Wait for completion

#### Implementation Phase
- Read plan file and extract the `Complexity: normal|high` field from the summary
- **If partial implementation detected**:
  - Identify unimplemented phases from plan file
  - Prompt user: "Plan is partially implemented. Continue from which phase? (list unimplemented phases)"
- **If complexity is high**:
  - Ask user via `question` which subagent to use: `feature_implement` or `feature_implement_complex`
  - Recommend `feature_implement_complex` in the prompt
  - If complex variant chosen, append to prompt: "Note: This is a high-complexity task - take extra care with edge cases, error handling, and comprehensive testing."
- **If complexity is normal**:
  - Use `feature_implement`
- Spawn chosen subagent with appropriate prompt
- Wait for completion

#### Review Phase
- Spawn `feature_review` subagent with prompt "Review changes for <TICKET> using base branch <BASE_BRANCH>"
- Wait for completion
- The review subagent will present findings, ask the user which issues to fix, assess fix complexity, and write the Requested Fixes section to review.md

#### Fix Phase
- Read review.md and check the `## Requested Fixes` section for unchecked items (`- [ ]`)
- If all items are checked (or no Requested Fixes section), skip to Rebase Phase
- Read the `Fix complexity: normal|high` field from the Requested Fixes section
- **If complexity is high**:
  - Ask user via `question` which subagent to use: `feature_fix` or `feature_fix_complex`
  - Recommend `feature_fix_complex` in the prompt
  - If complex variant chosen, append to prompt: "Note: This is a high-complexity task - take extra care with edge cases, error handling, and comprehensive testing."
- **If complexity is normal**:
  - Use `feature_fix`
- Spawn chosen subagent with appropriate prompt
- Wait for completion

#### Rebase Phase
- Check if any fixup commits exist on the feature branch:
  ```bash
  git log --oneline <base_branch>..<feature_branch> --grep="fixup!"
  ```
- If no fixup commits exist, inform user: "No fixup commits to squash. Rebase is unnecessary." and skip to next phase.
- If fixup commits exist, spawn `feature_rebase` subagent with prompt "Rebase feature branch for <TICKET>"
- Wait for completion

## Partial Implementation Detection

To detect if plan is partially implemented:
1. Read `init.md` for the base branch and feature branch names
2. Read plan file and extract phase names/descriptions
3. Get commit messages on feature branch: `git log --oneline <base_branch>..<feature_branch>`
4. Compare: check if commit messages contain phase names or file changes match phase descriptions
5. Identify which phases have been implemented and which are pending
6. Present unimplemented phases to user for selection

## Partial Fixes Detection

To detect if fixes are partially implemented:
1. Read `review.md` `## Requested Fixes` section
2. Lines with `- [ ] ISSUE_ID` are pending fixes
3. Lines with `- [x] ISSUE_ID:hash` are completed fixes
4. Present pending fixes to user for selection

## Complexity Assessment Criteria

### Implementation Phase
High complexity if ANY of:
- More than 5 phases that add/change code or test files (EXCLUDING documentation phases like CHANGELOG.md, README.md, *.md docs)
- More than 10 code or test files to modify (EXCLUDING documentation files: CHANGELOG.md, README.md, *.md docs)
- Phase descriptions contain keywords: "concurrent", "migration", "security", "performance", "edge cases", "complex"
- Average description length per phase (EXCLUDING documentation phases) > 500 characters
- Decisions file contains unresolved questions

## State passing

All state is derived from git branch and `.workflow/` files; no explicit context passing needed between subagents.

Key shared files (inside `.workflow/feature_<TICKET>_<slug>/`):
- `init.md` — base branch and feature branch names (created by init, read by all later stages: plan/decisions/implement/review/fix/rebase)
- `jira_ticket.md` — JIRA ticket details including fix versions and related tickets (created by skill, read by init/decisions/plan/review)
- `codebase_context.md` — codebase exploration results (created by skill, read by decisions/plan/implement)
- `decisions.md` — grill-me transcript (created by decisions, read by plan/implement)
- `plan.md` — implementation plan with complexity field (created by plan, read by implement/review)
- `review.md` — code review findings and requested fixes with fix complexity (created by review, read by fix)

## Error handling

If a subagent fails, report the error to the user and ask whether to continue or abort.

## Do not

- Never run `git fetch` or `git pull` — work with local branches only
- Never push to remote
- Never modify git config
- Never skip steps or reorder the workflow
- Never make decisions on behalf of the user — always present options and wait for selection
- Never proactively suggest next steps beyond the current phase
- Never assume user intent — follow the workflow exactly as written
