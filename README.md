# Threadwright

> **Threadwright is an implementation-agnostic methodology for developing and evolving products through persistent artifacts, explicit relationships, consequential-gap identification, useful activity, and continuous reassessment.**

## Overview

Threadwright provides a minimal, implementation-agnostic way to guide product development from an initial idea or requirement through product realization and subsequent evolution. It is deliberately iterative rather than phase-driven and does not prescribe a specific lifecycle (prototype → beta → MVP), methodology (Agile, Waterfall, Scrum), or organizational process.

The methodology is designed to be usable by humans without specialized tooling. AI-native tooling, agents, workflows, and document systems are implementation choices made separately from the methodology.

Its core purpose is to help people continuously answer:

> **Given what we are trying to achieve and what we currently know, what should we do next?**

---

## Core Model

The methodology has four fundamental concepts — no additional primitives are required:

| Concept | Description |
|---------|-------------|
| **Change** | An intended transformation (new product, MVP, feature, remediation, strategic shift, etc.) with an outcome against which progress is assessed |
| **Artifact** | Persistent knowledge or state relevant to development (requirements, decisions, designs, evidence, test results, documentation, etc.) |
| **Activity** | Work performed to change the state of the development effort (research, design, implementation, testing, validation, decision-making, etc.) |
| **Relationship** | Semantic connections between artifacts, activities, and Changes (supports, derived from, satisfies, implements, verifies, depends on, contradicts, supersedes, etc.) |

---

## The Control Loop

Development proceeds through continuous reassessment:

```text
                  Intended Outcome
                        │
                        ▼
                  Current State
                        │
                        ▼
               Consequential Gaps
                        │
                        ▼
           What must be learned,
           decided, or changed?
                        │
                        ▼
                Activity / Activities
                        │
                        ▼
              Updated Artifact State
                        │
                        ▼
                     Reassess
                        │
                        └───────────────↺
```

1. **Assess** — Determine what is currently known, decided, implemented, validated, unresolved
2. **Identify gaps** — Find what materially prevents or threatens the intended outcome
3. **Determine needs** — Decide what must be learned, decided, or changed
4. **Act** — Choose and perform the most useful activity
5. **Update** — Persist results as artifacts
6. **Reassess** — After meaningful work or material change, re-evaluate

---

## Four Invariants

| Invariant | Principle |
|-----------|-----------|
| **I1 — Persistence** | Meaningful work must leave its relevant results in persistent artifacts |
| **I2 — Outcome Orientation** | A Change must establish an intended transformation against which state and results can be assessed |
| **I3 — Epistemic Integrity** | Artifacts must not represent knowledge as more certain, supported, or authoritative than their basis justifies |
| **I4 — Feedback** | After meaningful work, the current state must be reassessed and subsequent work must respond to that reassessment |

---

## What This Repository Contains

### `methodology/`

| File | Description |
|------|-------------|
| [`methodology.md`](methodology/methodology.md) | The core methodology specification (v0.4) — defines the four primitives, control loop, invariants, boundaries, and what the methodology can/cannot guarantee |
| [`scenarios.md`](methodology/scenarios.md) | Validation scenarios demonstrating the methodology across diverse situations: greenfield products, enterprise SSO, urgent production changes, multi-change interactions, resource scarcity, irreducible uncertainty, change of direction, long-running products, compliance constraints, and failure mode distinctions |
| [`application-heuristics.md`](methodology/application-heuristics.md) | Practical heuristics for human application: addressing consequential gaps (H1), framing uncertainty around decisions (H2), choosing useful work (H3), reassessing (H4), plus epistemic integrity guidance and common failure modes |

---

## Methodology Boundaries

Threadwright **deliberately does not prescribe**:

- Specific product lifecycles or phases
- Management frameworks (Agile, Scrum, Kanban, Waterfall)
- Organizational roles
- Project-management tooling
- Document formats or specification languages
- Architecture methods
- Programming languages
- AI tools or agent architectures
- Approval workflows
- Estimation or prioritization formulas

These are implementation choices made separately.

---

## Key Distinctions

### Methodology Failure vs. Judgment Failure vs. Organizational Failure

| Category | Examples |
|----------|----------|
| **Methodology failure** | Meaningful work lost; implementation represented as outcome; evidence overstated; contradictions hidden; reassessment skipped |
| **Judgment failure** | Wrong market selected; wrong architecture; misunderstood customers; excessive risk accepted — despite following the methodology |
| **Organizational/external failure** | No decision authority; insufficient resources; organizational conflict; legal ambiguity; market conditions — methodology can represent but not eliminate |

> **The methodology structures human judgment; it does not replace it.**

---

## Minimal Human Operating Model

A team that remembers only this can apply the methodology:

> **What are we trying to achieve?**
> **What prevents us from achieving it?**
> **What matters most among those gaps?**
> **What do we need to learn, decide, or change?**
> **What is the most useful thing we can do next?**
> **What did we learn or change?**
> **What is different now?**
> **Repeat.**
>
> **Throughout: Represent what we know no more strongly than the evidence justifies.**

---

## What's Coming

The methodology is implementation-agnostic, but practical adoption benefits from tooling. The following are planned:

| Tool | Purpose |
|------|---------|
| **Agentic Skill** | An AI-agent skill that helps users implement the Threadwright methodology for their specific use case — guiding artifact creation, relationship mapping, gap identification, activity selection, and reassessment cycles |
| **Artifact Graph Visualizer** | An interactive tool for humans and AI agents to visualize, search, filter, browse, and explore the artifact graph — supporting traceability, impact analysis, gap discovery, and reassessment across Changes, artifacts, activities, and relationships |

---

## License

See [LICENSE](LICENSE) for details.