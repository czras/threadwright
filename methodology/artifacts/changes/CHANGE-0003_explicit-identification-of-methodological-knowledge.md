# CHANGE-0003 — Explicit Identification and Organization of Methodological Knowledge

**Status:** Implemented

## Context

Threadwright currently contains several kinds of methodological artifacts:

- invariants
- heuristics
- scenarios
- assessments
- research
- validation
- changes

Some artifact types already have identifiers, while others are identified primarily by filenames or document location.

Invariants and heuristics currently use short local identifiers such as:

- `I1`
- `H1`

Scenarios are currently growing without identifiers.

As the body of methodology grows, two related problems are emerging:

1. individual methodological elements need stable, explicit identities so they can be referenced precisely;
2. growing collections of artifacts need a predictable physical organization so that artifacts remain discoverable and manageable.

The current flat or partially organized structure will become increasingly difficult to navigate as artifact counts grow.

## Change

Make methodological knowledge explicitly identifiable, referenceable, and organized by artifact type.

This consists of two related structural changes:

### 1. Introduce explicit stable identifiers

Use explicit identifiers for methodological knowledge that needs independent reference:

| Artifact type | Current | New |
|---|---|---|
| Invariant | `I1...` | `INVARIANT-XXXX` |
| Heuristic | `H1...` | `HEURISTIC-XXXX` |
| Scenario | none | `SCENARIO-XXXX` |

Existing invariants and heuristics migrate to the new identifier format.

Existing scenarios receive identifiers.

Other artifact types already use explicit identifiers such as `ASSESSMENT-XXXX`, `RESEARCH-XXXX`, `VALIDATION-XXXX`, and `CHANGE-XXXX`.

Identifiers are stable once assigned.

### 2. Organize artifacts into type-specific subdirectories

Each artifact type should have its own subdirectory.

For example:

```text
invariants/
heuristics/
scenarios/
assessments/
research/
validation/
changes/
```

Artifacts of a given type are stored in the corresponding directory.

This organization should follow the conceptual artifact taxonomy that has already emerged rather than introducing additional categories merely for structural symmetry.

The exact directory naming and repository structure may evolve as the methodology evolves.

## Rationale

The methodology is increasingly becoming an interconnected body of knowledge rather than a single linear document.

Stable identifiers make individual elements addressable.

Type-specific directories make growing collections discoverable and manageable.

Together they provide a simple addressing model:

```text
artifact type → stable identifier → document
```

For example:

```text
heuristics/HEURISTIC-0009.md
scenarios/SCENARIO-0007.md
assessments/ASSESSMENT-0012.md
```

An identifier therefore provides identity independent of physical location, while the directory provides predictable organization.

This also makes cross-document relationships easier to express:

```text
INVARIANT-0001
    ↓
HEURISTIC-0003
    ↓
SCENARIO-0007
    ↓
ASSESSMENT-0012
```

This is illustrative only. It does not prescribe a particular relationship model.

## Identifier Format

Identifiers use four-digit sequential numbers:

```text
INVARIANT-0001
HEURISTIC-0001
SCENARIO-0001
ASSESSMENT-0001
RESEARCH-0001
VALIDATION-0001
CHANGE-0001
```

Each artifact type has its own sequence.

Identifiers:

- are stable once assigned;
- are not reused;
- do not encode semantic meaning beyond artifact type and sequence;
- should be used for cross-document references where precise identification is useful.

The numbering scheme is deliberately simple. It is an identity mechanism, not a taxonomy.

## Relationship Between Identity and Organization

Identifiers and directories solve different problems.

**Identifier:**
> Which artifact is this?

**Directory:**
> Where do artifacts of this kind belong?

The identifier should remain meaningful even if the physical repository structure changes.

Conversely, the directory should provide useful organization without requiring the identifier to encode hierarchy or semantic relationships.

This separation allows the methodology to evolve without coupling conceptual identity to repository layout.

## Relationship to Other Artifacts

The artifact structure may form an evolving knowledge graph:

```text
Intent / observation
        ↓
Assessment / research / validation
        ↓
Methodological knowledge
        ↓
Invariant / heuristic
        ↓
Scenario / application
        ↓
Evidence / further assessment
        ↓
Methodology evolution
```

These relationships are illustrative.

The change does not prescribe that every artifact must have a particular relationship to every other artifact.

Relationships should emerge through actual use.

## Scope

This change establishes:

- explicit stable identifiers for methodological artifacts that require independent reference;
- identifiers for scenarios;
- migration of existing short invariant and heuristic identifiers;
- type-specific artifact directories;
- predictable organization of growing artifact collections;
- use of identifiers for precise cross-document references.

This change does **not**:

- establish a complete or final artifact taxonomy;
- prescribe every possible relationship between artifacts;
- redesign the entire information architecture;
- require every statement to become a separate artifact;
- prescribe a fixed relationship graph;
- require a particular document template for every artifact type;
- assume that the current directory structure is permanent.

The purpose is to provide enough structure for the growing body of methodology to remain identifiable, referenceable, and manageable.

## Migration

1. Identify all existing invariant references such as `I1...`.
2. Assign stable `INVARIANT-XXXX` identifiers.
3. Identify all existing heuristic references such as `H1...`.
4. Assign stable `HEURISTIC-XXXX` identifiers.
5. Update references to the new identifiers.
6. Identify existing scenarios.
7. Assign stable `SCENARIO-XXXX` identifiers.
8. Update scenario references where useful.
9. Create artifact-type subdirectories.
10. Move existing artifacts into their corresponding directories.
11. Update paths and references affected by the move.
12. Update repository conventions and documentation describing artifact organization.
13. Preserve sufficient old-to-new mapping during migration to make the restructuring auditable.

The identifier migration and physical reorganization are implementation consequences of this change, not separate conceptual changes.

## Expected Result

The methodology should have:

- explicit, stable identity for independently referenceable artifacts;
- self-describing artifact identifiers;
- predictable organization by artifact type;
- manageable directories as artifact counts grow;
- precise cross-document references;
- separation between conceptual identity and physical location;
- a structure that can continue growing without requiring increasingly complex navigation conventions.

For example:

```text
methodology/
├── invariants/
│   ├── INVARIANT-0001_persistence.md
│   └── ...
├── heuristics/
│   ├── HEURISTIC-0001_address-consequential-gaps.md
│   └── ...
├── scenarios/
│   ├── SCENARIO-0001_greenfield-product-idea.md
│   └── ...
├── artifacts/
│   ├── assessments/
│   │   ├── ASSESSMENT-0001_....md
│   │   └── ...
│   ├── research/
│   │   ├── RESEARCH-0001_....md
│   │   └── ...
│   ├── validation/
│   │   ├── VALIDATION-0001_....md
│   │   └── ...
│   └── changes/
│       ├── CHANGE-0001_....md
│       └── ...
```

The filenames of artifacts that already use descriptive slugs may retain those slugs. The stable identifier provides identity; the slug provides human-readable context.

## Open Questions

The following remain intentionally unresolved:

- whether every heuristic or invariant needs its own standalone document;
- whether all scenarios should share a common structure;
- which relationships between artifacts warrant explicit representation;
- whether additional artifact types should receive identifiers;
- whether some artifact types should eventually be split or combined;
- whether the directory structure remains sufficient as the corpus grows.

These questions should be answered through use rather than speculation.

## Validation

Evaluate the change against two properties:

### Interconnectedness

Does the structure make it easier to discover, reference, and connect related pieces of methodological knowledge?

### Compactness

Does the structure improve comprehension, navigation, and maintainability without introducing unnecessary ceremony or cognitive overhead?

The change succeeds if the growing methodology becomes easier to reference and navigate while remaining compact and understandable.

## Current Position

This is a proposed structural change.

The underlying need has emerged from actual growth of the methodology and increasing cross-document relationships.

The specific identifier and directory conventions should remain deliberately simple. If future use demonstrates that they are insufficient, they can evolve through subsequent changes.