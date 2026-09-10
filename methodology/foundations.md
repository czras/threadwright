# Threadwright Foundations and Provenance

> This document explains where Threadwright comes from and how its three conceptual layers relate. It provides provenance without prescription.

---

## Three Distinct Layers

### Layer 1 — The Creator's Lens

The creator's way of engaging with reality, shaped by decades of software engineering, building, running, learning, and living. It is evolving but relatively stable.

**Recognizable preferences:**
- Agile
- Lean
- Minimal
- Concise
- Explicit
- Evidence-oriented
- Evolutionary
- Interconnected

**Abstract character (what the preferences reflect):**
- Simplicity
- Explicitness
- Adaptability
- Economy
- Interconnectedness
- Learning through observation

> These are characteristics of *one person's* way of engaging with reality. They are not universal principles, not Threadwright principles, and not required of practitioners.

---

### Layer 2 — Homo Sapiens Agenticus (HSA)

The creator's emerging thesis about human–agent cognitive partnership. It explores what becomes possible when persistent agentic systems become a normal extension of human capabilities.

**HSA is:**
- A thesis and area of exploration
- Independent of Threadwright
- About complementary cognition (humans make meaning; agents retain, relate, revisit)
- Concerned with the danger of premature structure
- About evolution of knowledge and intent as evolving states

**HSA is not:**
- A prediction that agents should replace human judgment
- A definition of Threadwright
- A prerequisite for using Threadwright

---

### Layer 3 — Threadwright

The synthesis of the creator's lens and the HSA understanding into a practical, implementation-agnostic methodology for pursuing intentions and outcomes with agentic systems.

**Threadwright is:**
- Infrastructure and methodology for the evolution of intent and knowledge
- A response to problems/opportunities compatible with HSA
- Structured around five concepts (Change, Artifact, Activity, Relationship, Consequential Gap) and an adaptive control loop
- Deliberately boundary-limited (does not prescribe lifecycle, roles, tooling, etc.)
- An optimization approach for reducing consequential uncertainty — see [ASSESSMENT-0008_manufactured-vs-evolved](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md)

**Threadwright is not:**
- A direct implementation of HSA
- A codification of the creator's preferences
- A product implementation of HSA
- Identical to HSA

For the complete methodology, see [`threadwright.md`](threadwright.md). For practical heuristics, see [`heuristics/README.md`](heuristics/README.md). For test scenarios, see [`scenarios/README.md`](scenarios/README.md).

---

## Evolutionary Relationship

The relationship is **evolutionary and feedback-driven**, not linear:

```
Reality
    ↓
Creator's Lens (how the creator engages with reality)
    ↓
HSA Understanding (thesis about human–agent partnership)
    ↓
Threadwright Synthesis (practical methodology)
    ↓
Practice (application in real contexts)
    ↓
Observation (evidence from practice)
    ↓
Refinement (changes to any layer)
    ↺
         ↑
└── Threadwright learns from its own use (recursive self-application)
              [ASSESSMENT-0008_manufactured-vs-evolved §11](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#11-threadwrights-recursive-property)
              [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §14](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#14-recursive-self-application)
```

**Key properties:**
- Each layer remains distinct and independently meaningful
- Practice can provide evidence that changes HSA understanding, changes Threadwright, or reveals something new about the lens
- The loop is continuous — there is no "final" state
- Observation precedes naming; structure follows utility
- **Threadwright is both an instrument for knowledge evolution and an object of knowledge evolution** — it evolves through its own application

For the recursive self-application in practice, see the scenario [SCENARIO-0008_recursive-self-application](scenarios/SCENARIO-0008_recursive-self-application.md) and [HEURISTIC-0004_reassess](heuristics/HEURISTIC-0004_reassess.md#recording-reassessment).

---

## Provenance Is Not Prescription

This foundation explains **why Threadwright has the character it does**. It does **not** mean:

- Practitioners must share the creator's preferences, worldview, or conclusions
- HSA is a prerequisite for using Threadwright
- Threadwright is a product implementation of HSA
- The three layers collapse into a single concept
- The creator's lens is a complete philosophy or manifesto
- Observations from practice immediately become doctrine

> Threadwright should be evaluated by what it enables and by evidence from practice, not by agreement with its creator's personal preferences.

---

## Observational Evidence

The creator's personal site emerged from raw material (CV, running history, fragments) placed into Markdown and explored/evolved through interaction with an agent while building the site.

This reinforces: **observe first, name later** — the lens can be discovered through artifacts and choices that emerge from working, not only described beforehand.

## Provenance of Core Formulation

The central optimization formulation emerged through a documented sequence:

1. **[ASSESSMENT-0008_manufactured-vs-evolved](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md)** — Emerged from applying Threadwright across multiple real contexts. Observed the manufactured vs. evolved knowledge distinction, refined to dynamic think/experience boundary, formulated as optimization problem.

2. **[ASSESSMENT-0009_assessment-of-ASSESSMENT-0008](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md)** — Second-order assessment validating ASSESSMENT-0008 against scientific research practice. Strengthened core hypothesis, added refinements: messy input → formulation, adaptive character, autonomy vs. automation distinction, HSA orthogonality, general epistemic machinery framing.

3. **[RESEARCH-0000_evolutionary-computation](artifacts/research/RESEARCH-0000_evolutionary-computation.md)** — Research direction exploring whether evolutionary computation and related fields (active learning, information theory, decision theory, experimental design, reinforcement learning) provide useful mechanisms for implementing the optimization. Currently reference only; not integrated into methodology.

This sequence demonstrates the recursive property: **Threadwright was used to develop Threadwright**.

### Heuristics and Scenarios Derived from This Provenance

| Assessment | Heuristics | Scenarios |
|------------|------------|-----------|
| ASSESSMENT-0008 (manufactured vs evolved) | [HEURISTIC-0005_choose-knowledge-action](heuristics/HEURISTIC-0005_choose-knowledge-action.md), [HEURISTIC-0006_dynamic-think-experience-boundary](heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md) | [SCENARIO-0004_dynamic-think-experience-boundary](scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md), [SCENARIO-0005_optimization-invariant-i5](scenarios/SCENARIO-0005_optimization-invariant-i5.md) |
| ASSESSMENT-0009 (assessment of 0008) | [HEURISTIC-0007_evolve-intent-from-messy-input](heuristics/HEURISTIC-0007_evolve-intent-from-messy-input.md), updated [HEURISTIC-0001_address-consequential-gaps](heuristics/HEURISTIC-0001_address-consequential-gaps.md), [HEURISTIC-0004_reassess](heuristics/HEURISTIC-0004_reassess.md) | [SCENARIO-0007_evolve-intent-from-messy-input](scenarios/SCENARIO-0007_evolve-intent-from-messy-input.md), [SCENARIO-0008_recursive-self-application](scenarios/SCENARIO-0008_recursive-self-application.md) |
| Both | Updated [HEURISTIC-0008_epistemic-integrity](heuristics/HEURISTIC-0008_epistemic-integrity.md) | [SCENARIO-0006_manufactured-vs-experiential-artifacts](scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md) |
