# Threadwright Git Conventions

Git records repository history and provides the versioning and traceability mechanism for changes to the repository.

The conventions below are intended to make history concise, reviewable, and easy to reason about while preserving traceability to the work and artifacts that produced each change.

## Commits

Commits use the [Conventional Commits specification](https://www.conventionalcommits.org/).

A commit normally consists of a concise one-line summary:

```text
<type>(<scope>): <description>
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

The commit diff is authoritative for the concrete repository change. Commit messages should not duplicate information that can be understood directly from the diff.

## Branches

Every working branch starts with the identifier of the GitHub issue or other work item it addresses.

For example:

```text
123-clarify-intent-establishment
123-fix-artifact-links
123-update-git-conventions
```

The branch name is not an artifact identifier. Artifact references are maintained through commits, pull requests, and artifact relationships.

## Fixups

When correcting a commit already present on the working branch, create a fixup commit targeting the original commit:

```text
fixup! <original commit subject>
```

Before proposing a pull request, fixup commits should normally be autosquashed. During review, keep review-stage commits visible until review is complete.

## Pull requests

A pull request describes the artifact-state transition being proposed.

A PR should make clear:

- which artifacts were created or changed,
- which artifact relationships were created or changed,
- which work item the change addresses,
- and what resulting repository state is being proposed.

The PR should describe the meaningful artifact transition rather than reproduce the commit history.

## Review history

During review, preserve the commits necessary to map review comments to their corresponding changes.

Before merging, consolidate the branch into a concise and coherent history.

## Merge strategy

Branches are rebased onto their target branch before merging. Conflicts are resolved during the rebase and fixup commits are autosquashed before the final merge.

The resulting branch is then merged using a non-fast-forward merge:

```text
git merge --no-ff <branch>
```

Merge commits provide discrete milestones on the main or release branches. The merge commit should reference the artifact that directly concluded the reasoning leading to the repository change.

## Quality gate

A branch is mergeable only when all required checks pass.

The quality gate is a prerequisite for merging, not a replacement for human review or judgment.

```text
Review complete
    +
Quality gate passed
    ↓
Merge
```

## File endings

All text files should end with a trailing newline.

## History principle

Git history should be optimized for understanding the evolution of the repository, not for preserving the exact sequence of actions taken while producing it.

Reasoning that materially affects the meaning of a change belongs in Threadwright artifacts rather than being reconstructed from an increasingly detailed commit transcript.

The relationship is:

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

The artifact system preserves meaningful state and reasoning. Git preserves resulting repository history and state transitions. Neither system needs to duplicate the role of the other.
