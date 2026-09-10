# ASSESSMENT-0004 — Establishing Intent From Input

**Status:** Proposed
**Type:** Methodology Assessment
**Subject:** Consequential gaps exposed by input scrutiny and intent extraction
**Related:** [ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md)

## Observation

[ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) established that an initial human input may be an imperfect representation of an underlying intent.

The input may express:

- a desired outcome,
- a problem,
- an assumption,
- a constraint,
- an interpretation,
- a proposed implementation,
- an experience,
- or a mixture of these.

Therefore, treating the initial statement as the intended outcome without scrutiny can cause the methodology to begin from an interpretation that has already been prematurely fixed.

The current methodology begins its control loop with:

> Intended Outcome → Current State → Consequential Gaps → ...

However, it does not explicitly describe how the intended outcome is established from the initial input.

## Consequential Gap

The current methodology has no explicit methodological step between:

> **Human input**

and:

> **Intended Outcome**

This creates several risks.

### 1. A proposed implementation can become mistaken for intent

For example:

> "We need a mobile app."

may represent an underlying intent such as:

> "Field workers need to access and update information while away from their desks."

If the first statement is immediately treated as the intended outcome, the methodology can begin optimizing a solution before establishing what outcome actually matters.

### 2. A vague intent can conceal materially different outcomes

For example:

> "I want to find love."

could correspond to substantially different intended outcomes depending on the person's actual situation and purpose.

The surface statement alone is therefore insufficient to establish the Change being pursued.

### 3. Interpretation can become invisible

When a human statement is transformed into an intended outcome, someone has necessarily interpreted it.

If that interpretation is not made explicit, it can acquire unwarranted authority simply because it became part of the working artifacts.

This conflicts with TW's existing commitment to epistemic integrity.

### 4. The methodology can prematurely constrain exploration

Once an interpretation has been accepted as the intended outcome, subsequent activities may optimize within that framing.

This can prevent the system from discovering that the original framing itself was wrong.

## Relationship to Existing Concepts

This gap does **not yet demonstrate that Intent must become a fifth fundamental concept**.

The existing four concepts may be sufficient:

- **Change** provides the object of purposeful evolution.
- **Artifact** provides persistence for the input, interpretation, candidate outcome, evidence, and resulting decisions.
- **Activity** provides the means by which uncertainty is reduced and decisions are made.
- **Relationship** provides provenance between the original input, its interpretations, outcomes, evidence, and subsequent changes.

The apparent missing capability may therefore be a refinement of how these concepts are applied rather than a new primitive.

## Proposed Distinction

TW should distinguish at least the following:

### Input

What a human or other source actually provides.

Input is evidence. It is not automatically authoritative intent.

### Interpretation

A representation of what the input appears to mean.

An interpretation is itself an artifact or artifact state and should remain distinguishable from the source input.

### Candidate Intent

The outcome or purpose that the input appears to imply.

A candidate intent is provisional until sufficiently established.

### Intended Outcome

The currently accepted representation of what the Change is intended to achieve.

This is the point at which the normal TW control loop can operate.

These are not necessarily additional fundamental concepts. They may instead describe different epistemic states and relationships around existing artifacts and Changes.

## Consequence for the Control Loop

The existing control loop may therefore require an explicit preceding phase:

> **Input → Scrutinize → Interpret → Establish Intended Outcome → Current State → Consequential Gaps → Activity → Updated Artifact State → Reassess**

The important addition is not necessarily a new permanent phase in every workflow.

The scrutiny should be proportional to the ambiguity and consequences of the input.

A well-defined input may require little or no additional work.

A vague, contradictory, assumption-heavy, or implementation-prescriptive input may require substantial exploration before an intended outcome can be established.

## Relationship to Epistemic Integrity

This insight appears strongly connected to the existing principle of epistemic integrity.

The methodology already distinguishes what is known, proposed, assumed, and evidenced.

The new gap extends that principle to the **origin of intent itself**.

A statement should not become authoritative merely because it was supplied by a human, nor should an interpretation become authoritative merely because an agent or practitioner produced it.

The provenance should remain visible:

> Source Input → Interpretation → Candidate Intent → Accepted Intended Outcome

This makes the reasoning behind the Change inspectable.

## Relationship to Outcome Orientation

Outcome orientation currently prevents TW from beginning with implementation instead of the outcome being pursued.

[ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) reveals a deeper version of the same problem:

> **The stated request may itself already be an implementation or interpretation of an unstated outcome.**

Therefore, outcome orientation may need to operate **before** the intended outcome is accepted, rather than assuming that the initial request already represents one.

This suggests that the existing principle may be sufficient, but its scope may need clarification.

## Relationship to Reassessment

Intent establishment should not necessarily be a one-time activity.

As knowledge accumulates, the interpretation of the original input may change.

For example:

> Input → Candidate Intent A → Evidence → Intent B

This is not necessarily failure.

It may represent healthy evolution of the Change.

Therefore, intent should remain revisable through the normal TW feedback loop.

This connects directly to the emerging view of Threadwright as an enabler of the **evolution of intent and knowledge**.

## Important Constraint

TW must not silently replace a person's stated intent with an inferred interpretation.

The purpose of scrutiny is not to decide what the human "really meant" independently of them.

Instead:

> **TW makes interpretations explicit so that they can be examined, challenged, confirmed, rejected, or refined.**

The human remains an important source of authority regarding their own intent.

Intent extraction is therefore an epistemic activity, not an authority transfer from human to methodology or tooling.

## Implications for Tooling

This distinction also reinforces the implementation-agnostic nature of TW.

A TW tool does not necessarily need domain knowledge to perform the structural work of intent extraction.

It can identify that:

- input exists,
- an interpretation has been proposed,
- the interpretation is uncertain,
- clarification is required,
- evidence supports or contradicts it,
- the intended outcome has changed,
- relationships exist between these artifacts.

Domain-specific knowledge may improve the quality of interpretation, but it is not necessarily required for the methodology itself.

This is consistent with the observation that the tooling can operate on the structure and evolution of knowledge without needing to understand the domain in which that knowledge applies.

## Assessment

The consequential gap exposed by [ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) appears to be:

> **TW assumes an intended outcome exists before explicitly explaining how an initial input becomes an intended outcome.**

The smallest promising resolution is therefore **not yet to introduce Intent as a new fundamental concept**.

Instead, investigate whether the methodology can be strengthened by explicitly defining:

1. input as evidence rather than automatically accepted intent,
2. interpretation as a provisional representation,
3. candidate intent as something to be established,
4. intended outcome as the currently accepted representation,
5. provenance between these states,
6. proportional scrutiny based on ambiguity and consequence,
7. continued revisability of intent through reassessment.

## Recommended Next Step

Before changing `methodology.md`, examine the proposed distinction against the complete methodology and determine the smallest coherent modification to:

- the definition of Outcome Orientation,
- Epistemic Integrity,
- the control loop,
- the definition of Change,
- the role of artifacts and relationships,
- the application heuristics,
- and the claim that TW has four fundamental concepts.

The key question is:

> **Can input scrutiny and intent extraction be expressed entirely through the existing TW primitives, or does doing so expose a genuine missing primitive?**

Do not add a fifth fundamental concept unless the existing ontology demonstrably cannot express the distinction without becoming misleading or convoluted.