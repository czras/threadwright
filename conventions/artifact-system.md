# Threadwright Artifacts

The repository contains the persistent artifacts produced while developing and applying Threadwright.

The artifact system is intentionally simple and may evolve as we learn what works.

## Artifact scope

Artifact identifiers are unique within an **artifact scope**.

An artifact scope is the part of the repository or artifact system within which artifacts are managed as a coherent set. For example:

```text
methodology/
implementation/
```

may each contain an independent artifact scope.

This allows the same identifier to exist in different scopes:

```text
methodology/ASSESSMENT-0006
implementation/ASSESSMENT-0006
```

When a relationship crosses artifact scopes, the scope should be included in the reference so that the artifact is unambiguous.

Within a single scope, the short identifier is sufficient:

```text
ASSESSMENT-0006
```

When necessary, use the scope-qualified form:

```text
methodology/ASSESSMENT-0006
implementation/ASSESSMENT-0006
```

Artifact identifiers should not be made globally unique merely to avoid scope qualification.

## Naming convention

Artifacts use filenames of the form:

```text
<id>_<slug-with-dashes>.md
```

For example:

```text
methodology/artifacts/ASSESSMENT-0006_smallest-methodological-change.md
```

The artifact identifier uses the form:

```text
<TYPE>-<4-digit-id>
```

where `TYPE` is uppercase.

Examples:

```text
CHANGE-0000
ASSESSMENT-0000
DECISION-0000
ACTIVITY-0000
```

An artifact's identifier is independent of its filename.

The slug is descriptive and may change if necessary; the identifier is the stable reference.

## Artifact references and links

When an artifact references another artifact, it should link to that artifact whenever the format supports linking.

The link text should be the artifact identifier. For references between artifact scopes, use the scope-qualified identifier.

For example, in Markdown:

```markdown
This assessment is derived from [ASSESSMENT-0005](./ASSESSMENT-0005_stress-testing-the-four-fundamental-concepts.md).
```

For a cross-scope reference:

```markdown
This assessment is derived from [methodology/ASSESSMENT-0005](../methodology/artifacts/ASSESSMENT-0005_stress-testing-the-four-fundamental-concepts.md).
```

Artifact titles should not be used as link text. Titles are descriptive and may change; the identifier is the stable reference.

Links provide navigation but are not the identity of an artifact. A relationship remains meaningful even when the representation does not support linking or a link cannot be resolved.

Artifact references should therefore preserve the identifier independently of the link target.

## Artifact storage

Artifacts are stored under an `artifacts/` directory within their scope.

Artifacts may initially be stored directly in that directory:

```text
methodology/
└── artifacts/
    ├── CHANGE-0000_create-threadwright.md
    ├── ASSESSMENT-0001_initial-state.md
    ├── ASSESSMENT-0002_consequential-gaps.md
    └── DECISION-0000_select-next-activity.md
```

As the number of artifacts grows, artifacts may be organized into type-specific subdirectories:

```text
methodology/
└── artifacts/
    ├── changes/
    │   └── CHANGE-0000_create-threadwright.md
    ├── assessments/
    │   ├── ASSESSMENT-0001_initial-state.md
    │   └── ASSESSMENT-0002_consequential-gaps.md
    └── decisions/
        └── DECISION-0000_select-next-activity.md
```

The directory structure is an organizational mechanism, not part of the artifact's identity.

The choice between a flat structure and type-specific subdirectories should remain proportional to the number of artifacts and the usefulness of the resulting organization.

## Artifact titles

Each Markdown artifact starts with its identifier and title:

```markdown
# ASSESSMENT-0006: The Smallest Methodological Change
```

The identifier is the stable reference to the artifact; the title describes its subject.

## Artifact types

Artifact types are introduced when they become useful. We do not define a complete artifact taxonomy in advance.

For example:

* `changes/` — Changes and their intended outcomes
* `assessments/` — Assessments of current state and consequential gaps
* `decisions/` — Consequential decisions and their basis
* `activities/` — Activities and their selection or results

These are examples rather than a fixed taxonomy.

The actual set of types, their structure, and their relationships may change as the repository develops.

## IDs

IDs are four-digit integers scoped to the artifact type within an artifact scope:

```text
CHANGE-0000
ASSESSMENT-0000
DECISION-0000
ACTIVITY-0000
```

For example, a methodology scope and an implementation scope may each contain:

```text
ASSESSMENT-0006
```

These are distinct artifacts because their scopes differ.

IDs provide concise, human-readable references between artifacts.

## Principle

Artifacts should capture **meaningful state and reasoning**, not a transcript of the work that produced them.

The goal is to preserve enough information to understand:

* what was known or believed,
* what mattered,
* what was decided or proposed,
* why an activity was selected,
* what changed as a result,
* and how the current state was reached.

The artifact structure should remain proportional to its purpose. If a convention becomes unnecessary ceremony, we should reconsider it.
