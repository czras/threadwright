# ASSESSMENT-0003 — Intent Must Be Extracted From Input

**Status:** Proposed
**Type:** Methodology Assessment
**Subject:** Initial input may be a representation of intent rather than intent itself

---

## 1. Observation

Threadwright currently treats the intended outcome of a Change as the basis for assessing current state and consequential gaps.

The methodology correctly distinguishes between different epistemic states such as observation, hypothesis, proposal, decision, and validation. It also explicitly warns against treating a proposal as authoritative merely because it has been written down.

However, the methodology does not currently make explicit a preceding problem:

> **The initial human input may itself be a proposed interpretation or implementation of an underlying intent.**

Examples:

> “We need a mobile app.”

This may be an implementation proposal rather than the underlying intent.

The underlying intent might instead be:

> “Field workers need to access and update information while away from their desks.”

Likewise:

> “I want to find love.”

may represent many materially different underlying intents, such as seeking a long-term relationship, companionship, intimacy, sexual connection, novelty, or something not yet understood by the person expressing it.

The initial statement therefore cannot necessarily be assumed to be an adequate representation of the intent that should orient subsequent work.

---

## 2. Insight

### Input is evidence about intent, not necessarily intent itself.

A human may provide Threadwright with:

* an intended outcome;
* a problem statement;
* an implementation proposal;
* an assumed solution;
* a constraint;
* an interpretation;
* a desired experience;
* a mixture of several of these;
* or an expression whose underlying intent is not yet clear.

Threadwright should therefore be capable of **scrutinizing the input and extracting the underlying intent before treating that interpretation as authoritative**.

This does not mean that Threadwright should replace the human's judgment or silently reinterpret what they said.

The extraction itself is an interpretation and therefore must remain epistemically explicit.

---

## 3. Relationship to Existing Methodology

This finding is strongly consistent with existing Threadwright principles.

### Epistemic integrity

The current methodology requires distinguishing what is observed, hypothesized, proposed, decided, accepted, and validated.

The same discipline should apply to the relationship between:

```text
Human input
    ↓
Threadwright interpretation
    ↓
Candidate underlying intent
```

The candidate intent must not become authoritative merely because Threadwright inferred it.

### Outcome orientation

The methodology currently requires a Change to establish an intended transformation and intended outcome.

The new finding raises a prior question:

> **How do we establish what the intended transformation actually is when the initial input may contain a proposed solution or an incomplete interpretation of intent?**

### Feedback

The methodology already allows new evidence to change scope, intended outcome, approach, or even the Change itself.

Intent extraction therefore appears to be a natural extension of the existing feedback model rather than a separate lifecycle phase.

---

## 4. Consequential Gap

There is currently a potential gap between:

> **what the human says**

and:

> **what the Change is actually intended to accomplish.**

If this gap is material and remains unnoticed, subsequent work may be internally coherent while pursuing the wrong thing.

This can result in:

* premature commitment to a proposed implementation;
* solving a symptom rather than the underlying problem;
* optimizing the wrong outcome;
* unnecessary implementation;
* significant downstream rework;
* incorrect assumptions becoming authoritative;
* loss of the original human intent beneath increasingly detailed artifacts.

The existing “Starting with implementation” failure mode addresses part of this problem, but currently frames it primarily as starting implementation before determining the desired outcome.

The new observation is broader:

> **The problem can occur before implementation: the initial request itself may already encode an unexamined implementation or interpretation.**

---

## 5. Cross-Domain Evidence

The phenomenon appears in substantially different domains.

### Software/product engineering

A customer may request:

> “We need a mobile application.”

The request may actually represent a proposed solution to an underlying customer or business need.

Agile development demonstrates why this distinction matters: interaction with prototypes, implementations, customers, and real-world evidence can reveal that the originally expressed requirement was incomplete or incorrect.

### Human/personal intent

A person may say:

> “I want to find love.”

The phrase does not uniquely determine the desired outcome or the appropriate course of action.

The person's intent may only become clearer through exploration and experience.

### Generalization

These examples suggest that this is not a domain-specific phenomenon.

Rather:

> **Humans frequently express intentions through interpretations, desired solutions, labels, or incomplete abstractions of what they actually want to accomplish.**

Therefore it is potentially a fundamental property of the input boundary of Threadwright.

---

## 6. Proposed Methodological Implication

Threadwright should not necessarily begin with:

```text
Input → Change
```

A more faithful model may be:

```text
Input
  ↓
Scrutinize
  ↓
Identify what the input represents
  ↓
Extract candidate intent
  ↓
Make interpretation explicit
  ↓
Establish intended outcome / Change
  ↓
Proceed with the normal TW control loop
```

Importantly, **intent extraction should not become a mandatory heavyweight phase**.

For a clear, low-consequence input, the interpretation may be immediate.

For an ambiguous or consequential input, additional exploration may be warranted.

This follows the existing principle of proportionality: assurance should be proportionate to uncertainty, risk, consequences, reversibility, and the decision or action being supported.

---

## 7. Important Constraint

Threadwright must not silently substitute its own interpretation for the human's intent.

Instead, a candidate interpretation should remain distinguishable from an established intent.

For example:

```text
Input:
    "We need a mobile app."

Interpretation:
    "The requester appears to believe a mobile app is an appropriate
     means of solving the problem."

Candidate underlying intent:
    "Field workers need to access and update information while away
     from their desks."

Confidence:
    Uncertain

Open question:
    "Is this the outcome you are actually trying to achieve?"
```

This preserves epistemic integrity while allowing Threadwright to challenge premature solution framing.

---

## 8. Relationship to Intent Evolution

This assessment also strengthens the emerging understanding of Threadwright as an enabler of **evolution of intent and knowledge**.

Intent may evolve not only after work has been performed, but also during the initial process of understanding what the input means.

Therefore:

```text
Initial input
      ↓
Candidate intent
      ↓
Exploration
      ↓
Better understanding
      ↓
Refined intent
      ↓
Action
      ↓
New knowledge
      ↓
Further evolution of intent
```

Intent extraction and intent evolution are therefore related but distinct:

* **Intent extraction:** What does the current input actually appear to be trying to accomplish?
* **Intent evolution:** How does that intent change as knowledge and experience accumulate?

---

## 9. Assessment

**Finding:** Substantial.

The current methodology already contains the necessary conceptual foundations — artifacts, relationships, outcome orientation, epistemic integrity, and feedback — but does not explicitly account for the possibility that the initial input is itself an imperfect or solution-oriented representation of intent.

This may warrant a methodological addition concerning **intent extraction / input scrutiny**.

However, the finding should first be tested against the existing methodology to determine whether:

1. it requires a new explicit methodological principle;
2. it can be expressed as an application of existing principles;
3. it requires an extension to the definition of Change or Outcome;
4. or it is better treated as an application heuristic rather than a methodology primitive.

---

## 10. Recommended Next Assessment

Before changing the methodology, examine the consequences of introducing explicit intent extraction for:

* the definition of **Change**;
* **Outcome Orientation**;
* **Epistemic Integrity**;
* the **Assess** step;
* the distinction between input, intent, interpretation, and proposed implementation;
* artifact relationships;
* intent evolution;
* and the existing claim that the methodology has only four fundamental concepts.

The objective should be to determine the **smallest methodological change that makes the new insight true without unnecessarily expanding the methodology.**
