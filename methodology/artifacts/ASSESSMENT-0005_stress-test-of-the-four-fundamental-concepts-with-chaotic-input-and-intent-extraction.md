# ASSESSMENT-0005 — Stress Testing the Four Fundamental Concepts

**Status:** Proposed
**Type:** Methodology Assessment
**Subject:** Testing whether input scrutiny and intent extraction require a new fundamental concept
**Related:** [ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md), [ASSESSMENT-0004](ASSESSMENT-0004_establishing-intent-from-input.md)

## Purpose

[ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) established that initial human input may be an imperfect representation of an underlying intent.

[ASSESSMENT-0004](ASSESSMENT-0004_establishing-intent-from-input.md) identified a consequential gap in the current methodology:

> TW begins its control loop with an Intended Outcome but does not explicitly explain how an initial input becomes an Intended Outcome.

The current methodology has four fundamental concepts:

1. Change
2. Artifact
3. Activity
4. Relationship

This assessment tests whether these four concepts are sufficient to represent the newly identified distinction between:

> Input → Interpretation → Candidate Intent → Intended Outcome

The purpose is **not** to introduce a fifth concept.

Instead, deliberately attempt to model several forms of real-world input using only the existing concepts.

If the four concepts cannot represent the distinction without becoming misleading, this becomes evidence that the ontology itself may need to change.

---

# Test Cases

## Case 1 — Explicit Outcome

### Input

> "I want to reduce checkout abandonment by 20%."

This is already relatively close to an intended outcome.

### Representation

**Artifact**

The original statement can be persisted as an input artifact.

**Change**

A Change can represent the effort to achieve the reduction.

**Intended Outcome**

The statement can become the currently accepted intended outcome.

**Activity**

Activities can establish the baseline, investigate causes, identify consequential gaps, and evaluate interventions.

**Relationship**

Relationships can connect:

> Input → Change → Intended Outcome → Activities → Evidence

### Result

No apparent ontology problem.

The four concepts are sufficient.

---

## Case 2 — Problem Statement

### Input

> "Customers keep abandoning checkout."

This does not state an outcome directly.

### Possible interpretation

> "The organization wants to reduce checkout abandonment."

### Representation

**Artifact**

The original problem statement is persisted as an input artifact.

**Activity**

An activity can investigate whether abandonment is actually consequential and determine what outcome matters.

**Artifact**

The interpretation can be represented explicitly rather than replacing the original input.

**Change**

Once the intended outcome is sufficiently established, a Change can be created around it.

**Relationship**

Relationships preserve:

> Problem Statement → Interpretation → Change → Intended Outcome

### Result

The four concepts appear sufficient.

Importantly, **Interpretation does not need to be a new primitive**.

It can be represented as an artifact whose relationship to the original input makes its provenance explicit.

---

## Case 3 — Proposed Implementation

### Input

> "We need a mobile app."

This is particularly important because the input appears to specify a solution rather than an outcome.

### Possible interpretation

> "The requester believes a mobile application is an appropriate means of achieving something."

The underlying outcome might instead be:

> "Field workers need to access and update information while away from their desks."

### Representation

**Artifact**

Persist:

> "We need a mobile app."

as the original input.

**Artifact**

Persist the interpretation:

> "The requester appears to believe a mobile app is an appropriate means of solving the problem."

**Activity**

Investigate what the requester is actually trying to accomplish.

**Artifact**

Persist candidate outcomes discovered through that activity.

**Relationship**

Represent:

> Input → Interpretation → Candidate Outcome

**Change**

Only after an intended outcome is sufficiently established should the Change be framed around it.

### Result

Again, the four concepts appear sufficient.

This is a particularly strong result because the problematic element — the proposed implementation — does not require a new primitive.

It is simply **an artifact with a particular role in the reasoning**.

---

# Case 4 — Vague Intent

### Input

> "I want to find love."

This is deliberately difficult because the surface statement may correspond to substantially different underlying outcomes.

Possible interpretations could include:

- seeking a long-term romantic relationship,
- seeking companionship,
- seeking a sexual relationship,
- seeking a casual encounter,
- seeking an affair,
- or something else entirely.

The methodology must not choose among these interpretations on the person's behalf.

### Representation

**Artifact**

Persist the original statement.

**Activity**

Perform clarification or exploration.

**Artifact**

Persist candidate interpretations as provisional artifacts.

For example:

> Candidate interpretation A: seeking a long-term romantic relationship.

> Candidate interpretation B: seeking companionship.

**Relationship**

Connect each candidate interpretation to the original input.

**Human judgment**

The person can confirm, reject, combine, or refine the candidates.

**Change**

The eventual Change is based on the currently accepted intended outcome.

### Result

The four concepts remain sufficient.

The important observation is that **candidate intent is not itself necessarily a new primitive**.

It can be represented as an artifact with a provisional status and an explicit relationship to its source.

---

# Case 5 — Constraint Disguised as Intent

### Input

> "We have to use Kubernetes."

This is neither obviously an outcome nor necessarily an implementation requirement.

It could represent:

- an actual organizational constraint,
- a preference,
- an architectural assumption,
- an already-made decision,
- or a perceived requirement that has never been validated.

### Representation

**Artifact**

Persist the statement as input.

**Activity**

Investigate why Kubernetes is considered necessary.

**Artifact**

Represent the resulting interpretation or constraint explicitly.

For example:

> "The organization requires Kubernetes for deployment."

or:

> "The requester believes Kubernetes is required."

**Relationship**

Connect the original statement to the resulting interpretation and evidence.

**Change**

The Change remains focused on the outcome rather than automatically accepting Kubernetes as its solution.

### Result

The four concepts appear sufficient.

Again, the key mechanism is not a new primitive but **explicit artifact state and provenance**.

---

# Case 6 — Mixed Input

### Input

> "We need an AI chatbot because support is too expensive."

This combines several different kinds of information:

- proposed implementation: AI chatbot,
- perceived problem: support is too expensive,
- implied outcome: reduce support cost,
- causal assumption: chatbot → lower support cost.

### Representation

The input should not be flattened into a single authoritative statement.

Instead:

**Artifact**

Original input.

**Activity**

Scrutinize the statement.

**Artifacts**

Separate representations may emerge:

> Problem: support cost is considered too high.

> Proposed implementation: AI chatbot.

> Assumption: chatbot adoption will reduce support cost.

> Candidate outcome: reduce the cost of providing support while maintaining an acceptable level of service.

**Relationships**

Represent the relationships between these elements.

For example:

> Input → Problem

> Input → Proposed Implementation

> Input → Assumption

> Problem → Candidate Outcome

> Proposed Implementation → Assumption

### Result

The four concepts remain sufficient.

This case provides particularly strong evidence that the distinction is primarily about **how artifacts and relationships are used**, rather than requiring additional primitives.

---

# Cross-Case Findings

All six cases can be represented using the existing four concepts:

| Input type | Artifact | Activity | Change | Relationship |
|---|---|---|---|---|
| Explicit outcome | ✓ | ✓ | ✓ | ✓ |
| Problem statement | ✓ | ✓ | ✓ | ✓ |
| Proposed implementation | ✓ | ✓ | ✓ | ✓ |
| Vague intent | ✓ | ✓ | ✓ | ✓ |
| Constraint / assumption | ✓ | ✓ | ✓ | ✓ |
| Mixed input | ✓ | ✓ | ✓ | ✓ |

No case requires a fifth primitive.

However, the exercise exposes an important weakness in the current methodology.

## The Missing Element Is Not a Primitive

The problem is not that TW lacks a concept capable of representing intent.

The problem is that TW currently does not make sufficiently explicit that:

> **Artifacts can represent different epistemic roles, and relationships can represent the provenance and transformation between them.**

The existing concepts therefore appear capable of expressing:

> Input → Interpretation → Candidate Outcome → Accepted Intended Outcome

without introducing:

> Intent

as a fundamental concept.

---

# A More Important Discovery

The stress test suggests that **Intent may not be an object in the same ontological category as Change, Artifact, Activity, and Relationship.**

Instead, intent appears to be something that can be:

- expressed by a human,
- inferred from input,
- represented in artifacts,
- questioned through activities,
- supported or contradicted by evidence,
- accepted or rejected,
- refined through feedback,
- and changed over time.

This makes intent look more like an **evolving property or epistemic representation associated with a Change** than an independent primitive.

That distinction matters.

If intent were introduced as a fifth fundamental concept, TW might accidentally imply that intent exists independently of the artifacts, evidence, relationships, and activities through which it becomes knowable.

The stress test provides no evidence that this is necessary.

---

# New Candidate Model

The current evidence supports the following provisional model:

> **Input is an artifact.**
>
> **Interpretation is an artifact.**
>
> **Candidate intent is an artifact.**
>
> **Accepted intended outcome is part of the current framing of a Change.**
>
> **Relationships preserve how one became derived from another.**
>
> **Activities create the opportunity to question, validate, reject, or refine these representations.**

This means the evolution of intent can potentially be represented entirely through the existing TW machinery.

For example:

```text
Human Input
    │
    ▼
[Input Artifact]
    │
    │ interpreted as
    ▼
[Candidate Interpretation]
    │
    │ explored through
    ▼
[Activity]
    │
    ├──────────────► [Evidence]
    │
    ▼
[Candidate Intended Outcome]
    │
    │ accepted for now
    ▼
[Change]
    │
    ▼
[Intended Outcome]
    │
    │ feedback / new evidence
    ▼
[Reassessment]
    │
    └──────────────► revised interpretation / outcome
```

The diagram is deliberately expressed using existing TW primitives rather than introducing an "Intent" node as a new primitive.

---

# Consequential Gap That Remains

Although the ontology appears sufficient, the methodology currently does not give practitioners enough guidance about **how to recognize and handle the different roles contained within human input**.

The missing capability therefore appears to be methodological rather than ontological.

TW likely needs to make explicit that before accepting an input as the basis for a Change, practitioners should consider:

1. What exactly has been provided?
2. Is it an outcome, problem, assumption, constraint, implementation proposal, interpretation, experience, or mixture?
3. What interpretation is being made?
4. What evidence supports that interpretation?
5. What remains uncertain?
6. What intended outcome can currently be established?
7. What should remain provisional?

This is the likely bridge between [ASSESSMENT-0004](ASSESSMENT-0004_establishing-intent-from-input.md) and a methodology change.

---

# Further Implication: Scrutiny Is Not Always a Separate Activity

The stress test also raises an important proportionality question.

It would be undesirable for TW to require a formal "intent extraction" ceremony for every simple, unambiguous request.

For example:

> "Change the heading from '2025-1 - 2025-02' to '2025-01 to 2025-02'."

The intended outcome is sufficiently clear that elaborate intent extraction would add more cost than value.

Therefore, input scrutiny should likely be **proportional to ambiguity, consequence, and uncertainty**.

This is consistent with TW's existing principle of proportional assurance.

The methodology may therefore need to say something closer to:

> **Before treating an input as an intended outcome or basis for a Change, scrutinize it sufficiently to determine what it represents and whether its interpretation is consequential.**

The required depth of scrutiny is itself determined by context.

---

# Assessment

The stress test provides strong evidence that:

> **Intent extraction does not require Intent to become a fifth fundamental concept.**

The existing four concepts appear capable of representing the full process.

The more substantial methodological gap is that TW does not currently make explicit enough that **initial input must be interpreted before it can safely become the basis for an Intended Outcome or Change**.

The likely smallest change is therefore to strengthen the methodology around:

- input scrutiny,
- interpretation,
- epistemic status,
- provenance,
- proportionality,
- and the establishment of Intended Outcomes.

The four fundamental concepts should remain unchanged unless further testing produces contradictory evidence.

---

# Recommended Next Step

Examine the current methodology text and determine exactly where this principle belongs.

In particular, test whether the smallest coherent change is:

1. a refinement of **Outcome Orientation**,
2. a refinement of **Epistemic Integrity**,
3. an addition to the **control loop**,
4. an application heuristic,
5. or a combination of these.

The target should be:

> **Make input scrutiny and intent extraction explicit without turning them into a heavyweight mandatory process and without expanding the fundamental ontology.**

Only after this has been established should `methodology.md` be modified.