# Threadwright Methodology Validation Scenarios

> These scenarios demonstrate and challenge the Threadwright methodology; they are examples of application, not prescribed workflows.


## 1. Purpose

This document records scenarios used to challenge and validate the product development methodology.

The scenarios serve two purposes:

1. test whether the methodology can handle realistic product-development situations without adding unnecessary concepts;
2. demonstrate the intended coarse-grained use of the methodology.

These are examples, not prescribed workflows.

The methodology remains implementation-agnostic and usable by human teams without AI or specialized tooling.

---

# 2. Greenfield Product Idea

## Situation

A person or team has a completely new product idea.

At the beginning, there may be little more than:

> "There may be an opportunity for an AI-assisted product."

The intended Change might initially be:

> Determine whether this opportunity is worth pursuing.

Later, the Change could become:

> Produce a prototype for personal dogfooding.

or:

> Create a beta for beta testers.

or:

> Create a commercially viable MVP.

These are different outcomes and therefore different Changes.

## Application

The team creates and maintains artifacts such as:

- problem hypotheses
- customer hypotheses
- market evidence
- constraints
- business assumptions
- proposed product concepts
- decisions
- experiments
- results

The control loop becomes:

```text
Opportunity hypothesis
    ↓
Identify consequential unknowns
    ↓
Determine decisions affected
    ↓
Choose useful investigation
    ↓
Capture evidence
    ↓
Reassess
```

If evidence weakens the original opportunity, the team may:

- modify the idea
- target a different segment
- change the intended outcome
- create a different Change
- abandon the opportunity

## What this demonstrates

The methodology does not require a pre-existing product, requirements document, architecture, or roadmap.

It can begin with an idea.

It also does not force the idea into a prototype/beta/MVP lifecycle. Those are possible desired outcomes chosen by humans.

## Important boundary

The methodology cannot determine whether the idea is actually valuable.

It structures how the team investigates and decides.

---

# 3. SSO / Enterprise Authentication

## Situation

A product needs enterprise SSO.

Different concerns emerge:

- customers want broad identity-provider support
- security has requirements
- engineering has architectural constraints
- sales has commercial commitments
- customers may already have specific infrastructure

The Change might be:

> Enable target enterprise customers to authenticate using supported enterprise identity providers while satisfying applicable security and product constraints.

## Application

Artifacts may include:

- customer requirements
- security requirements
- constraints
- architecture proposals
- threat-model findings
- implementation plans
- decisions
- test evidence
- deployment evidence

Suppose engineering proposes architecture A.

Security raises a concern.

Sales says limiting support to A will make the product commercially unacceptable.

The artifact graph may contain:

```text
Security requirement
        │
        ├── constrains → Architecture
        │
Customer requirement
        │
        └── constrains → Architecture
```

The conflict becomes a consequential gap.

The team identifies the decision:

> Which architecture and supported scope should be accepted?

Investigation is performed only to the extent necessary to make that decision responsibly.

The resulting decision is recorded with its basis and authority.

## What this demonstrates

- competing stakeholder concerns can coexist without creating new primitives;
- contradictions can be represented through artifacts and relationships;
- decisions do not require certainty;
- organizational authority remains a human concern;
- implementation is not automatically equivalent to outcome achievement.

---

# 4. Urgent Production Change

## Situation

A production incident is causing customer impact.

There is no time to construct a comprehensive specification before acting.

## Application

The team creates a minimal incident artifact:

- observed behavior
- affected systems
- known impact
- current hypothesis
- mitigation decision
- result

The loop becomes:

```text
Observed incident
    ↓
Consequential gap
    ↓
Hypothesis / decision
    ↓
Mitigation activity
    ↓
Observed result
    ↓
Reassess
```

The team may act under uncertainty.

The methodology does not require complete certainty before action.

It requires that uncertainty and the basis for consequential decisions be represented appropriately.

## What this demonstrates

The methodology is not a documentation-before-action process.

Persistence means that meaningful work leaves its relevant result in artifacts. It does not require exhaustive paperwork before urgent action.

---

# 5. Multi-Change Interaction

## Situation

Two teams work on:

**Change A**

> Add enterprise SSO.

**Change B**

> Add fine-grained authorization.

Initially they appear independent.

A modification to the identity model for Change A affects assumptions in Change B.

## Application

Relationships expose the dependency:

```text
Change A
   ↓
Identity model
   ↓
affects
   ↓
Authorization design
   ↓
Change B
```

The material change triggers reassessment.

The authorization design is discovered to contain a now-invalid assumption.

A new consequential gap is created.

The team chooses the appropriate activity.

## What this demonstrates

The methodology does not require a global sequential workflow.

Relationships and reassessment allow concurrent Changes to interact.

The implementation challenge at scale is discovering relevant affected artifacts efficiently. That is an implementation concern, not a methodological primitive.

---

# 6. Resource Scarcity

## Situation

A team has:

- 20 consequential gaps
- 5 possible activities
- one engineer
- two days of available capacity

Not everything can be addressed.

## Application

The team considers:

- consequence
- uncertainty
- ability to block progress
- downstream rework
- dependencies
- cost
- reversibility
- available capacity

Example:

```text
Gap A:
    high probability of invalidating the product

Gap B:
    moderate UX uncertainty

Gap C:
    architecture uncertainty

Gap D:
    documentation gap

Gap E:
    minor performance concern
```

The team chooses the activity that appears most useful given the actual context.

No mandatory priority formula is required.

## What this demonstrates

The methodology structures prioritization without pretending to compute the optimal answer.

This is human judgment.

---

# 7. Irreducible Uncertainty

## Situation

A team must decide whether to invest heavily in a new product.

Research has reduced uncertainty, but cannot eliminate it.

Further investigation is expensive and unlikely to materially improve the decision.

## Application

The team asks:

> Is the current basis sufficient for this decision?

If yes, the responsible authority may decide:

> Proceed despite the remaining uncertainty.

The decision records the uncertainty and its accepted consequences.

Alternatively:

> The remaining downside is unacceptable.

The team abandons or changes the Change.

## What this demonstrates

The methodology does not require certainty.

It requires appropriate representation of uncertainty and an adequate basis for consequential decisions.

Important principle:

> **Uncertainty is not itself a failure state. Unacknowledged or misrepresented uncertainty is.**

---

# 8. Unexpected Solution / Change of Direction

## Situation

A team starts building an automated workflow product.

Customer research reveals that customers do not primarily want automation. They want visibility into workflow bottlenecks.

## Application

Evidence weakens the original hypothesis.

The team reassesses and may create:

```text
Change A
    ↓
evidence
    ↓
hypothesis weakened
    ↓
Change B
```

Change B may target workflow visibility instead.

Change A may be superseded or abandoned.

Historical artifacts remain available to explain why the direction changed.

## What this demonstrates

The methodology does not treat the original plan as sacred.

New evidence can legitimately change the intended Change itself.

---

# 9. Long-Running Product

## Situation

A mature product contains:

- thousands of artifacts
- hundreds of Changes
- years of decisions
- multiple teams
- architecture history
- production evidence
- technical debt
- regulatory constraints

A new Change is introduced:

> Add support for a new payment provider.

## Application

The relevant current state may include:

- payment requirements
- applicable constraints
- existing architecture
- security decisions
- provider dependencies
- relevant production evidence
- affected Changes

The team does not need to reason over the entire artifact graph manually.

It identifies the relevant connected state, then applies the normal loop:

```text
Change
    ↓
Relevant current state
    ↓
Consequential gaps
    ↓
Activities
    ↓
Updated artifacts
    ↓
Reassess
```

## What this demonstrates

The methodology scales conceptually without requiring a new lifecycle.

Efficient discovery, retrieval, impact analysis, summarization, and graph traversal are implementation problems.

---

# 10. Compliance Constraint

## Situation

A product must legally log every transaction.

The constraint is represented as an authoritative artifact.

A proposed design does not log every transaction.

## Application

The artifact graph contains:

```text
Compliance constraint
        │
        └── constrains → Design
```

The conflict becomes a consequential gap.

The team cannot legitimately treat the design as compatible without resolving or otherwise appropriately accounting for the constraint.

The methodology does not itself know what the law requires. That knowledge must enter the artifact state from an appropriate authority.

## What this demonstrates

The methodology can reason with external constraints without pretending to generate domain truth.

---

# 11. Bad Decision Despite a Good Methodology

## Situation

A team wants to increase revenue.

They identify conversion rate as a major gap.

They run experiments.

Conversion increases by 20%.

Revenue falls because the additional customers are unprofitable.

## Result

The methodology may have been followed correctly.

The team chose a poor or incomplete desired outcome.

This is not necessarily a methodology failure.

## What this demonstrates

The methodology cannot guarantee that humans choose the correct:

- strategy
- market
- architecture
- objective
- risk tolerance
- business opportunity

It provides disciplined progression and representation.

It does not replace judgment.

---

# 12. Methodology Failure vs Judgment Failure vs Organizational Failure

This distinction is important when interpreting all scenarios.

## Methodology failure

The process violates the methodology.

Examples:

- meaningful work is lost
- implementation is represented as outcome achievement
- evidence is overstated
- material contradictions are hidden
- new evidence is ignored
- the current state is not reassessed

## Judgment failure

The methodology is followed, but humans make a bad decision.

Examples:

- wrong market selected
- wrong architecture chosen
- wrong feature prioritized
- customer needs misunderstood
- excessive risk accepted

## Organizational / external failure

The methodology encounters conditions it cannot solve.

Examples:

- no person has authority to decide
- insufficient resources
- organizational conflict
- missing expertise
- legal ambiguity
- unexpected market conditions

The methodology can represent these problems and make them visible.

It cannot eliminate them.

---

# 13. What the Scenarios Demonstrate Collectively

Across the scenarios, the methodology consistently works without introducing additional fundamental concepts.

The four primitives remain sufficient:

```text
Change
Artifact
Activity
Relationship
```

The control loop remains sufficient:

```text
Assess
    ↓
Identify consequential gaps
    ↓
Determine what must be learned,
decided, or changed
    ↓
Choose and perform activity
    ↓
Update artifacts
    ↓
Reassess
```

The four invariants remain sufficient:

```text
Persistence
Outcome orientation
Epistemic integrity
Feedback
```

The scenarios therefore support an important conclusion:

> **The methodology is deliberately small enough to cover materially different product-development situations without turning each situation into another methodology rule.**

The scenarios are examples of application, not additional rules.
