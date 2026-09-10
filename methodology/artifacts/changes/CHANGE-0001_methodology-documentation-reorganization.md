# CHANGE-0001: Methodology Documentation Reorganization

**Status:** Proposed
**Type:** Documentation / Conceptual Architecture
**Date:** 2026-09-07

## Intended outcome

Establish a coherent public documentation architecture for Threadwright that distinguishes its intellectual foundation, infrastructure concept, methodology, operational guidance, project conventions, and potential tooling while making the repository understandable without requiring knowledge of the project's development history.

## Current state

The repository currently presents Threadwright primarily as a methodology. The methodology, heuristics, and scenarios are concentrated in a small number of large documents, while project conventions live alongside the conceptual material without an explicit explanation of their different roles.

The licensing model also describes the distinction in terms of methodology versus tooling, which becomes increasingly awkward as the repository contains HSA, conventions, scenarios, and other documentary material.

## Proposed state

The documentation architecture becomes:

```text
Homo Sapiens Agenticus
        ↓
       thesis
        ↓
   Threadwright
        ↓
 infrastructure concept
        ↓
    methodology
        ↓
 heuristics + scenarios
        ↓
 potential tooling
```

The repository itself has an orthogonal project-governance layer:

```text
conventions/ → how this project is developed and maintained
meta/        → project identity and brand
```

### Homo Sapiens Agenticus

Add [homo-sapiens-agenticus.md](../homo-sapiens-agenticus.md) as an independent precursor thesis about human–agent cognitive partnership.

HSA must remain conceptually independent of Threadwright. In particular, it should not depend on Threadwright's thread metaphor or terminology to make its argument.

### Threadwright

Rename:

```text
methodology/methodology.md
→ methodology/threadwright.md
```

The existing methodology remains the core content, with framing updated so that Threadwright is understood as infrastructure for the evolution of intent and knowledge rather than merely as a methodology.

### Methodology directory

Add `methodology/README.md` as the directory-level map explaining the relationship between HSA, Threadwright, methodology, heuristics, scenarios, and artifacts.

### Heuristics

Decompose `methodology/application-heuristics.md` into independently addressable documents under `methodology/heuristics/`, retaining the existing operational guidance and epistemic-integrity material.

### Scenarios

Decompose `methodology/scenarios.md` into independently addressable scenario documents under `methodology/scenarios/`.

### Artifacts

Retain the existing methodology artifacts as persistent evidence of how the methodology evolved. Add this Change artifact to record the documentation architecture decision.

### Conventions

Retain `conventions/` as a distinct repository-governance layer. Conventions describe how the Threadwright project itself is developed and maintained; they are not part of the Threadwright conceptual model.

### Licensing

Replace the conceptual distinction between a generic software license and a methodology-specific license with a material-type distinction:

```text
Software material
    → AGPL-3.0

Intellectual and documentary material
    → CC BY-NC-SA 4.0
```

Rename the license documents:

```text
LICENSE
→ LICENSE-SOFTWARE

LICENSE-METHODOLOGY
→ LICENSE-INTELLECTUAL
```

The license follows the nature of the material rather than its directory. This means that conventions, HSA, Threadwright documentation, heuristics, scenarios, and other documentary material use the intellectual-material license, while executable software uses the software license.

Brand identity remains separately reserved unless explicitly licensed.

## Rationale

The repository is beginning to express several distinct kinds of knowledge. Treating all of them as "methodology" makes the conceptual architecture harder to understand and makes the licensing model increasingly artificial.

The new structure separates concerns without creating unnecessary conceptual layers:

- HSA explains a broader cognitive thesis.
- Threadwright names the infrastructure concept.
- The methodology explains how to apply it.
- Heuristics provide reusable reasoning guidance.
- Scenarios demonstrate and challenge the approach.
- Tooling is a possible implementation.
- Conventions govern the development of this repository itself.

The licensing distinction follows the same principle of explicit boundaries: it is based on what a piece of repository material **is**, rather than where it happens to live.

## Consequences

### Positive

- The conceptual architecture becomes explicit.
- HSA can evolve independently of Threadwright.
- Individual heuristics and scenarios can be referenced, discussed, and revised independently.
- Repository conventions have a clear role without being mistaken for methodology.
- Licensing scales to future repository contents without redefining "methodology".
- Tooling remains clearly an implementation choice rather than part of the conceptual definition.

### Trade-offs

- More files create more navigation overhead.
- The conceptual boundaries must be maintained as the project evolves.
- The repository now contains two complementary licensing regimes for different material types.

## Decision boundary

This Change concerns the **documentation and conceptual architecture** of the repository. It does not commit Threadwright to a particular software architecture or tooling implementation.

## Relationships

This Change supersedes the earlier documentation-restructuring assessment as the authoritative record of the proposed repository-state transition.
