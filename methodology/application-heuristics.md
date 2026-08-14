# Threadwright Application Heuristics

> These heuristics describe how humans can practically apply the Threadwright methodology. They are guidance, not additional methodology primitives.


## 1. Purpose

The methodology defines what must remain true during product development. These heuristics describe how humans can practically apply it.

They are guidance, not additional methodology primitives.

They do not prescribe a lifecycle, phase sequence, organizational structure, or tooling.

A competent team should be able to apply them using ordinary judgment and whatever artifacts and working practices are appropriate to its context.

---

## 2. The Four Operational Heuristics

### H1 — Address consequential gaps

**Compare the current state with the desired outcome and prioritize gaps that could materially affect the outcome, invalidate downstream work, or make further progress irresponsible.**

Do not treat every unknown or imperfection as equally important.

A consequential gap might concern:

- customer value
- a critical constraint
- a major technical uncertainty
- security
- compliance
- a dependency
- a missing decision
- inadequate evidence
- an implementation blocker
- a likely source of expensive rework

The question is not:

> What is missing?

It is:

> What missing or unresolved thing matters enough to affect what we should do?

---

### H2 — Frame uncertainty around decisions

**When uncertainty matters, relate it to the decision or action it affects and investigate only as far as necessary to act responsibly.**

Instead of:

> Research the market.

ask:

> What decision are we trying to make, and what do we need to know to make it responsibly?

Instead of:

> Investigate the architecture.

ask:

> What architectural decision is currently uncertain, what consequences does it have, and what evidence would materially improve that decision?

This prevents both:

- premature commitment
- investigation without a useful decision endpoint

Perfect certainty is not required.

The relevant question is whether the remaining uncertainty is acceptable for the decision's consequences.

---

### H3 — Choose useful work

**Prefer activities that produce the most valuable change in knowledge, decisions, implementation, evidence, or outcome relative to their cost and dependencies.**

Useful work is not synonymous with:

- the easiest task
- the most visible task
- the next item in a predetermined backlog
- the task with the most detailed specification
- implementation work

Sometimes the highest-value activity is:

- a customer interview
- a benchmark
- a prototype
- an architecture experiment
- resolving a requirement conflict
- making a decision
- writing a missing specification
- implementing a feature
- validating a result

Consider:

- consequence
- uncertainty
- expected information or progress
- downstream rework
- dependencies
- reversibility
- cost
- available capacity

There is no required scoring formula.

---

### H4 — Reassess

**After meaningful work or material change, reassess the current state rather than assuming previous plans, assumptions, decisions, or conclusions remain valid.**

Reassessment should consider affected:

- artifacts
- relationships
- assumptions
- decisions
- dependencies
- Changes
- intended outcomes

This is what makes the methodology iterative.

It permits:

- changing direction
- abandoning work
- revising scope
- superseding decisions
- discovering new problems
- reacting to production evidence
- exploiting unexpected opportunities

A plan is a useful artifact, not a commitment to ignore reality.

---

## 3. Cross-Cutting Principle: Epistemic Integrity

**Do not represent a claim, decision, or result as more certain, supported, applicable, authoritative, or achieved than the available basis justifies.**

This principle applies to every heuristic and every artifact.

### Practical implications

#### Distinguish observation from interpretation

```text
Observation:
    Beta users completed the workflow only 18% of the time.

Interpretation:
    The workflow may be too difficult.

Hypothesis:
    Reducing the number of required steps will improve completion.
```

Do not collapse these into a single unsupported statement.

#### Distinguish proposal from decision

```text
Proposal:
    Use architecture A.

Decision:
    Architecture A is approved for this Change.
```

AI-generated or human-generated proposals do not become decisions merely because they are written down.

#### Distinguish implementation from outcome

```text
Implementation:
    SSO integration is deployed.

Outcome:
    Target customers can successfully authenticate using SSO
    and the intended business outcome is achieved.
```

The first does not prove the second.

#### Preserve evidence limitations

Evidence should not be generalized beyond the population, conditions, time period, or circumstances for which it is applicable.

#### Preserve material uncertainty

Uncertainty can be accepted.

It should not be disguised as certainty.

#### Preserve consequential disagreement

When stakeholders or artifacts materially disagree, represent the disagreement until it is resolved, superseded, or otherwise appropriately accounted for.

---

## 4. Applying the Heuristics Together

The heuristics work as a loop rather than a checklist.

```text
Current state
    ↓
H1: What consequential gaps exist?
    ↓
H2: What decision or action does the uncertainty affect?
    ↓
H3: What activity would most usefully address it?
    ↓
Perform activity
    ↓
H4: Reassess
    ↓
Repeat
```

Epistemic integrity applies throughout.

---

## 5. Common Failure Modes

### Starting with implementation

> "What should we code?"

before determining:

> "What outcome are we trying to achieve, and what consequential gap currently prevents it?"

Use H1.

### Research without a decision

> "Let's investigate this more."

without knowing why.

Use H2.

### Following the plan blindly

> "It's in the plan, so we must do it."

even though the state has changed.

Use H4.

### Polishing low-impact work

> "Let's finish the documentation."

while a major customer-value uncertainty remains unresolved.

Use H1 and H3.

### Treating activity completion as success

> "The feature is implemented, therefore the Change is complete."

Use epistemic integrity and H4.

### Treating AI output as authority

> "The agent generated the requirement, so it must be the requirement."

Use epistemic integrity.

### Demanding certainty everywhere

> "We can't proceed until we know for sure."

Use H2.

The appropriate question is whether the basis is sufficient for the consequences of the decision.

### Overengineering the process

> "Every small change needs a full specification, review board, experiment, and formal validation."

Use H3 and proportional assurance.

---

## 6. Human Judgment Remains Central

The heuristics intentionally do not provide deterministic answers.

For example, two teams may identify the same gaps and rationally choose different activities because they have different:

- resources
- constraints
- risk tolerance
- expertise
- deadlines
- strategic objectives
- available evidence

The methodology should make that judgment explicit and inspectable, not eliminate it.

---

## 7. Practical Questions for a Team

At any point, a team can ask:

1. **What outcome are we trying to achieve?**
2. **What is currently true?**
3. **What consequential gaps remain?**
4. **Which gap matters most right now?**
5. **What decision or action does it affect?**
6. **What would we need to know or change to act responsibly?**
7. **What activity would be most useful given its cost and dependencies?**
8. **What did that activity actually establish?**
9. **What changed in the artifact state?**
10. **What needs to be reassessed now?**

These questions are a practical application of the methodology, not additional methodology rules.

---

## 8. The Minimal Human Operating Model

A team that remembers only this can still apply the methodology:

> **What are we trying to achieve?**
>
> **What prevents us from achieving it?**
>
> **What matters most among those gaps?**
>
> **What do we need to learn, decide, or change?**
>
> **What is the most useful thing we can do next?**
>
> **What did we learn or change?**
>
> **What is different now?**

Repeat.

Throughout:

> **Represent what we know no more strongly than the evidence justifies.**
