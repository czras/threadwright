# Threadwright Git Conventions

Git records repository history and provides the versioning and traceability mechanism for changes to the repository.

The conventions below are intended to make history concise, reviewable, and easy to reason about while preserving traceability to the work and artifacts that produced each change.

## Commits

Commits use the [Conventional Commits specification](https://www.conventionalcommits.org/).

A commit normally consists of a concise one-line summary:

```text
<type>(<scope>): <description>
```

For example:

```text
docs(methodology): clarify intended outcome
```

The commit message should contain a traceability reference in its footer.

When the change originates from a GitHub issue or other work item, reference that work item:

```text
Refs: #123
```

When a commit directly implements or records the conclusion of an artifact, the relevant artifact may also be referenced:

```text
Refs: #123
Artifact: ASSESSMENT-0006
```

The exact combination of work-item and artifact references depends on what the commit represents.

The commit diff is authoritative for the concrete repository change. Commit messages should not duplicate information that can be understood directly from the diff.

A detailed commit body is therefore exceptional rather than the default. It may be useful when the commit contains information that cannot be adequately understood from the diff, such as:

- an important hypothesis,
- a non-obvious constraint,
- a significant compatibility consideration,
- or reasoning that would otherwise be lost.

Commit history should remain concise and coherent rather than becoming a transcript of the development process.

## Branches

Every working branch starts with the identifier of the GitHub issue or other work item it addresses.

For example:

```text
123-clarify-intent-establishment
123-fix-artifact-links
123-update-git-conventions
```

The work-item identifier provides immediate traceability from the branch to the work being performed.

The branch name is not an artifact identifier. Artifact references are maintained through commits, pull requests, and artifact relationships.

## Fixups

When correcting a commit already present on the working branch, create a fixup commit targeting the original commit:

```text
fixup! <original commit subject>
```

If a correction targets a fixup commit itself, chain the target:

```text
fixup! fixup! <original commit subject>
```

This allows the branch history to preserve the relationship between corrections and the commits they modify while work is in progress.

Before proposing a pull request, fixup commits should normally be autosquashed.

If additional corrections are made during the review process, they should remain as fixup commits until the review is complete.

During pull request review, do not autosquash commits merely to clean up the branch. Keeping review-stage commits visible preserves the mapping between review comments and the changes that address them.

After review and approval, the branch may be autosquashed before merging.

The final branch history should tell a coherent and concise story about what changed. The exact sequence in which the branch evolved during development is not itself important.

## Pull requests

A pull request describes the artifact-state transition being proposed.

A PR should make clear:

- which artifacts were created or changed,
- which artifact relationships were created or changed,
- which work item the change addresses,
- and what resulting repository state is being proposed.

For example:

```markdown
## Artifacts

Created:
- ASSESSMENT-0006

Changed:
- methodology.md
- application-heuristics.md
- scenarios.md

## Relationships

- ASSESSMENT-0006 derived from ASSESSMENT-0005
- ASSESSMENT-0006 informs methodology.md
- ASSESSMENT-0006 informs application-heuristics.md
- ASSESSMENT-0006 informs scenarios.md

## Result

The methodology now explicitly accounts for scrutiny of ambiguous
initial input without introducing a fifth fundamental concept.
```

The PR should describe the meaningful artifact transition rather than reproduce the commit history.

## Review history

The branch history serves two different purposes during development:

1. **Review traceability** — individual commits and fixups show how review comments were addressed.
2. **Final project history** — the merged history shows the coherent result of the work.

These purposes should not be conflated.

During review, preserve the commits necessary to map review comments to their corresponding changes.

Before merging, consolidate the branch into a concise and coherent history.

## Merge strategy

Branches are rebased onto their target branch before merging.

Conflicts are resolved during the rebase.

Fixup commits are autosquashed before the final merge.

The resulting branch is then merged using a non-fast-forward merge, creating an explicit merge commit:

```text
git merge --no-ff <branch>
```

The purpose is to keep the main/release branch history divided into discrete, meaningful steps.

Conceptually:

```text
main ─────●───────────────●───────────────●────
           \             / \             /
            ●──●──●──●──●   ●──●──●──●──●
                 work           work
```

The individual branch commits provide the detailed history of a change, while the merge commits provide concise milestones in the history of the main or release branches.

A merge commit represents a completed, reviewable change on its target branch.

The merge commit should reference the artifact that directly concluded the reasoning leading to the repository change.

For example:

```text
docs(methodology): evolve intent establishment

Artifact: ASSESSMENT-0006
```

The merge commit therefore connects the repository's historical structure with the artifact system's reasoning structure.

## Quality gate

A branch is mergeable only when all required checks pass.

The quality gate is a prerequisite for merging, not a replacement for human review or judgment.

A merge should therefore occur only when:

```text
Review complete
    +
Quality gate passed
    ↓
Merge
```

## Diverging branches

When branches diverge, completed changes should normally be transferred using the relevant merge commit.

Prefer creating a fix on the main/development branch and backporting it to release branches when practical.

When a fix must instead originate on a release branch, it may subsequently be forward-ported to the main/development branch.

When transferring a completed change between diverging lines of development, prefer cherry-picking the merge commit representing that change.

The objective is to keep the Git graph straightforward to reason about while preserving the relationship between the original change and its transferred versions.

Where appropriate, the transferred change should retain its original traceability references.

## File endings

All text files should end with a trailing newline.

This is a repository convention rather than a property of any particular file type.

## History principle

Git history should be optimized for understanding the evolution of the repository, not for preserving the exact sequence of actions taken while producing it.

The desired history has two levels:

- **Commits** provide concise, concrete changes.
- **Merge commits** provide discrete milestones on the main/release branches.

Reasoning that materially affects the meaning of a change belongs in Threadwright artifacts rather than being reconstructed from an increasingly detailed commit transcript.

The resulting relationship is:

```text
Work item
    ↓
Activity / implementation
    ↓
Artifacts and relationships
    ↓
Repository changes
    ↓
Commits
    ↓
Pull request
    ↓
Merge commit
```

The artifact system preserves the meaningful state and reasoning.

Git preserves the resulting repository history and state transitions.

Neither system needs to duplicate the role of the other.