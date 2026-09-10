# ASSESSMENT-0006 — The Smallest Methodological Change

**Status:** Proposed
**Type:** Methodology Assessment
**Subject:** Minimal methodology change required to incorporate input scrutiny and intent extraction
**Related:** [ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md), [ASSESSMENT-0004](ASSESSMENT-0004_establishing-intent-from-input.md), [ASSESSMENT-0005](ASSESSMENT-0005_stress-test-of-the-four-fundamental-concepts-with-chaotic-input-and-intent-extraction.md)

## Purpose

[ASSESSMENT-0005](ASSESSMENT-0005_stress-test-of-the-four-fundamental-concepts-with-chaotic-input-and-intent-extraction.md) found that the existing four fundamental concepts are sufficient to represent:

> Input → Interpretation → Candidate Intent → Intended Outcome

without introducing Intent as a fifth fundamental concept.

The remaining question is therefore:

> **What is the smallest methodological change that makes this capability explicit without creating unnecessary process or terminology?**

This assessment examines the existing methodological structures most directly affected:

- Outcome Orientation
- Epistemic Integrity
- the control loop
- application heuristics
- proportional assurance

---

# Finding 1 — Outcome Orientation Is the Primary Location

The existing Outcome Orientation principle already protects TW from beginning with implementation instead of the outcome being pursued.

[ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) exposed a deeper version of the same problem:

> The initial input may itself be an implementation proposal or another imperfect representation of the underlying outcome.

Therefore the principle should be extended from:

> Do not begin with implementation instead of outcome.

toward:

> **Do not assume that the initial input is already an accurate representation of the intended outcome.**

This is the smallest conceptual extension because the new insight is fundamentally about preserving orientation toward the outcome rather than prematurely accepting the framing supplied by the input.

---

# Finding 2 — Epistemic Integrity Provides the Mechanism

The new principle does not require a new epistemic category.

The existing methodology already distinguishes between what is:

- known,
- proposed,
- assumed,
- evidenced,
- and uncertain.

The input/interpretation distinction fits naturally into this structure.

A statement such as:

> "We need a mobile app."

can remain an authoritative record of what someone said while **not automatically becoming an authoritative statement of the outcome**.

This distinction is critical.

The methodology should preserve:

> **what was said**

separately from:

> **what we currently believe it means**

and from:

> **what outcome has been accepted as the basis for the Change**

Therefore Epistemic Integrity should explicitly cover the possibility that **the interpretation of an input is itself uncertain**.

---

# Finding 3 — The Control Loop Needs a Boundary, Not Necessarily a New Step

The current control loop begins:

> Intended Outcome → Current State → Consequential Gaps → ...

The stress test indicates that the loop itself remains valid.

The problem is that the methodology does not explain what happens **before an Intended Outcome has been established**.

Adding a mandatory new step such as:

> Input → Intent Extraction → Intended Outcome → ...

would risk turning a useful principle into a procedural ceremony.

Instead, the methodology should distinguish between:

### Establishing the Change framing

When input is sufficiently ambiguous, consequential, or solution-prescriptive, activities may be needed to establish the intended outcome.

### Operating within an established Change

Once the intended outcome is sufficiently established, the existing control loop applies unchanged.

This gives us:

```text
Input
  │
  ▼
Scrutinize sufficiently
  │
  ├── already clear ───────────────┐
  │                                │
  └── unclear / consequential       │
          │                         │
          ▼                         │
       Explore / clarify            │
          │                         │
          └──────────────┬──────────┘
                         ▼
                 Intended Outcome
                         │
                         ▼
              Existing TW control loop
```

The important word is **sufficiently**.

There is no universal amount of scrutiny required.

---

# Finding 4 — Proportional Assurance Prevents Over-Process

Input scrutiny should not become a mandatory heavyweight stage.

Consider two inputs:

> "Fix the typo in the heading."

and:

> "We need to replace our entire customer-support operation with an AI system."

The first may have an obvious intended outcome.

The second may contain:

- an outcome,
- a proposed implementation,
- assumptions,
- organizational consequences,
- unknowns,
- and potentially conflicting interests.

Treating both identically would violate proportionality.

Therefore the new capability should be governed by the existing principle of proportional assurance:

> **The amount of scrutiny required to establish an intended outcome should be proportionate to ambiguity, uncertainty, consequence, and the cost of acting on a mistaken interpretation.**

This allows TW to remain lightweight for simple work while becoming more rigorous when the framing itself is consequential.

---

# Finding 5 — Relationships Carry the Provenance

[ASSESSMENT-0005](ASSESSMENT-0005_stress-test-of-the-four-fundamental-concepts-with-chaotic-input-and-intent-extraction.md) demonstrated that no new primitive is needed to represent interpretation or candidate intent.

The methodology already has Relationships.

Therefore the provenance can be represented through relationships such as:

```text
Input
  └─ interpreted as → Candidate Interpretation
                           │
                           └─ supports → Candidate Outcome
                                           │
                                           └─ accepted as → Intended Outcome
```

The exact relationship vocabulary does not need to be prescribed by the methodology at this point.

The methodological requirement is simply that the distinction and provenance **remain visible when it matters**.

This is particularly important because otherwise an interpretation can silently replace its source.

---

# Finding 6 — Intent Evolution Is Already Covered by Reassessment

Once an intended outcome has been established, new evidence may reveal that the interpretation was incomplete or wrong.

For example:

```text
Initial input
    ↓
Interpretation A
    ↓
Intended Outcome A
    ↓
Activity
    ↓
New evidence
    ↓
Interpretation B
    ↓
Intended Outcome B
```

This should not require a separate "intent evolution" mechanism.

It is an ordinary consequence of:

- feedback,
- persistence,
- epistemic integrity,
- and reassessment.

The important methodological addition is therefore not:

> "Intent evolves."

but:

> **An established intended outcome remains revisable when new evidence changes the understanding of what is being pursued.**

---

# Candidate Minimal Change

The evidence supports a small set of changes to the canonical methodology.

## 1. Refine Outcome Orientation

Add the idea that:

> **An initial request or statement must not automatically be treated as the intended outcome. It may itself be an interpretation, assumption, constraint, problem statement, or proposed implementation.**

The practitioner should establish what outcome is actually being pursued before allowing the initial framing to constrain subsequent work, where the distinction is consequential.

## 2. Refine Epistemic Integrity

Add that:

> **Interpretations of input are themselves provisional knowledge and should remain distinguishable from the original input and from accepted intended outcomes.**

This prevents inferred meaning from silently becoming fact.

## 3. Add a Short Pre-Loop Clarification

Immediately before the control loop, explain that:

> **When the intended outcome is not already sufficiently clear, scrutinize the input and perform whatever clarification or exploration is necessary to establish a usable intended outcome.**

This is a methodological capability, not necessarily a mandatory workflow stage.

## 4. Add One Application Heuristic

A concise heuristic can make the principle operational:

> **When given a request, first ask what the request represents before deciding what to do about it.**

Useful follow-up questions include:

- What outcome is actually being pursued?
- Is this a proposed solution rather than the outcome?
- What assumptions are embedded in the request?
- What remains uncertain?
- What would make this interpretation wrong?

---

# Changes Explicitly Rejected

This assessment recommends **not** making the following changes.

### Do not add Intent as a fifth fundamental concept

The ontology stress test found no need for it.

### Do not introduce a mandatory Intent Extraction phase

This would unnecessarily proceduralize TW.

### Do not require every input to be decomposed into formal categories

Input classification can be useful, but making it mandatory would create process overhead without necessarily improving outcomes.

### Do not require tooling to understand domain semantics

The methodology should describe the structural requirement for scrutiny and provenance, not prescribe how domain understanding is obtained.

### Do not require a particular relationship vocabulary

The methodology should establish the need for provenance without prematurely constraining implementation.

---

# Resulting Methodological Model

The smallest coherent model appears to be:

```text
Human / external input
        │
        ▼
  What does this input represent?
        │
        ▼
Establish intended outcome
        │
        ▼
Intended Outcome
        │
        ▼
Current State
        │
        ▼
Consequential Gaps
        │
        ▼
What must be learned / decided / changed?
        │
        ▼
Activity
        │
        ▼
Updated Artifact State
        │
        ▼
Reassess
        │
        └──────────────► Intent / outcome may be reframed
```

The first part is **conditional and proportional**.

The second part is the existing TW control loop.

This preserves the current architecture while making an important previously implicit capability explicit.

---

# Deeper Finding

The investigation reveals something more fundamental about Threadwright.

TW does not merely help people execute against an intended outcome.

It helps establish **what the intended outcome should currently be understood to be**, and then continuously tests that understanding against experience and evidence.

Therefore the methodology operates on two coupled forms of evolution:

### Knowledge evolution

> What do we believe to be true?

### Intent evolution

> What are we trying to achieve, given what we now understand?

These interact continuously:

```text
Knowledge ───────────────► Intent
    ▲                         │
    │                         ▼
    └────── Feedback ◄──── Activity
```

This does not require new fundamental concepts.

It is a consequence of the existing TW control loop once input scrutiny and epistemic provenance are made explicit.

---

# Assessment

The smallest useful methodological change is **not an ontological expansion**.

It is a clarification that:

> **The intended outcome is established from input; it is not necessarily contained in the input itself.**

This clarification should primarily strengthen:

- Outcome Orientation,
- Epistemic Integrity,
- the transition into the control loop,
- and the application heuristics.

The resulting methodology remains:

> implementation-agnostic,
> artifact-centered,
> relationship-aware,
> outcome-oriented,
> epistemically explicit,
> and continuously reassessing.

No new fundamental concept is currently justified.

---

# Recommended Next Step

Now modify `methodology.md` itself.

The change should be deliberately small.

Before editing, identify the exact existing passages covering:

1. Outcome Orientation
2. Epistemic Integrity
3. the control loop
4. Application Heuristics
5. Proportional Assurance

Then produce the smallest textual delta that makes the conclusions of [ASSESSMENT-0003](ASSESSMENT-0003_input-scrunity-and-extraction.md) through ASSESSMENT-0006 true.

After that change, reassess the methodology as a whole rather than assuming the local edits are coherent.

The test is:

> **Can a practitioner read the methodology and understand that a request may need to be interpreted before it becomes the basis for an Intended Outcome, while still knowing that simple cases need no ceremony?**

If yes, the change is probably small enough.