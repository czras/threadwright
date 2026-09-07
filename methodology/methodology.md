# Threadwright Methodology

> **Threadwright is an implementation-agnostic methodology for developing and evolving products through persistent artifacts, explicit relationships, consequential-gap identification, useful activity, and continuous reassessment.**

## 1. Purpose

This methodology provides a minimal, implementation-agnostic way to guide product development from an initial idea or requirement through product realization and subsequent evolution.

It is designed to be usable by humans without specialized tooling. AI-native tooling, agents, workflows, and document systems are implementation choices made separately from the methodology.

The methodology is deliberately iterative rather than phase-driven. It does not prescribe a lifecycle such as prototype → beta → MVP, nor does it prescribe Agile, Waterfall, Scrum, or any particular organizational process.

Its purpose is to help people continuously answer:

> Given what we are trying to achieve and what we currently know, what should we do next?

---

## 2. Core Model

The methodology has four fundamental concepts:

- **Change**
- **Artifact**
- **Activity**
- **Relationship**

No additional fundamental concepts are required.

### 2.1 Change

A Change represents an intended transformation.

It establishes what is being changed and the intended outcome against which progress and results can be assessed.

A Change may be large or small:

- a new product
- a commercially viable MVP
- a beta release
- a prototype for dogfooding
- a new capability
- a customer-requested modification
- a production remediation
- a strategic change of direction

A Change does not imply a particular lifecycle or implementation sequence.

A Change may be modified, superseded, abandoned, or completed.

### 2.2 Artifact

An Artifact is persistent knowledge or state relevant to development.

Examples include:

- requirements
- constraints
- hypotheses
- assumptions
- decisions
- designs
- specifications
- research findings
- evidence
- plans
- test results
- implementation
- documentation
- infrastructure definitions
- operational observations
- incident records
- validation results

Artifacts may have different roles and states, including exploratory, proposed, accepted, superseded, or otherwise authoritative.

Creation of an artifact does not by itself establish authority.

### 2.3 Activity

An Activity is work performed to change the state of the development effort.

Examples include:

- research
- interviewing
- analysis
- design
- implementation
- prototyping
- testing
- validation
- review
- deployment
- measurement
- investigation
- decision-making

Activities are not prescribed by phase. The appropriate activity is determined from the current state and the needs of the Change.

A meaningful Activity must leave its relevant result in persistent artifacts.

### 2.4 Relationship

A Relationship connects artifacts, activities, and Changes.

Examples include:

- supports
- derived from
- satisfies
- implements
- verifies
- depends on
- affects
- contradicts
- supersedes
- based on

Relationships provide semantic structure and traceability without requiring separate fundamental concepts for every relationship type.

---

## 3. Desired Outcome and Scope

Every Change establishes an intended transformation and an intended outcome.

An initial request, statement, or requirement does not necessarily establish that intended outcome accurately. Input may express:

- an intended outcome
- a problem
- an assumption
- a constraint
- a proposed implementation
- an interpretation
- an experience
- or a mixture of these

Where the meaning of the input is ambiguous or consequential, it should be scrutinized sufficiently to establish what outcome is actually being pursued before the Change is framed around it.

The required degree of scrutiny should be proportionate to factors such as:

- ambiguity
- uncertainty
- consequence
- reversibility
- cost of acting on a mistaken interpretation

An interpretation of input is itself knowledge about what the input appears to mean. It should remain distinguishable from the original input and should not be treated as authoritative merely because it has been recorded.

The purpose is not to have the methodology determine what a person "really meant." Human judgment remains responsible for confirming, rejecting, or refining the interpretation.

The Change may also define scope and other relevant properties.

For example:

> Produce a prototype for personal dogfooding.

> Create a beta suitable for external beta testers.

> Create a commercially viable MVP.

These are different intended outcomes for potentially similar underlying ideas.

Scope therefore describes **what the current Change is trying to accomplish**, rather than defining a universal product-development lifecycle.

A Change can also be constrained by its context.

Examples of constraints include:

- the product must be profitable
- an existing customer has Microsoft SQL Server deployed
- legislation requires every transaction to be logged
- all developers are Java developers
- an existing site must support 100,000 requests per second

Constraints are part of the relevant artifact state. They do not need to become a separate methodological subsystem.

---

## 4. Development as a Control Loop

Development proceeds through continuous reassessment of the current state.

The fundamental loop is:

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

The loop assumes that the Change has an established intended outcome. When an initial input does not yet establish that outcome sufficiently, scrutiny and clarification are part of the useful work required to establish the Change.

### 4.1 Assess the current state

Determine what is currently known, decided, implemented, validated, unresolved, constrained, and uncertain.

The relevant state is the state necessary to reason about the Change. It does not require reading or maintaining every artifact in a large product.

### 4.2 Compare with the intended outcome

Ask what still prevents or threatens achievement of the intended outcome.

### 4.3 Identify consequential gaps

A gap is consequential when it can materially:

- affect the intended outcome
- invalidate downstream work
- create unacceptable consequences
- block progress
- create significant rework
- undermine a consequential decision

A gap may be a missing fact, unresolved decision, contradiction, inadequate evidence, missing implementation, failed validation, unacceptable risk, or other material difference between the current state and what is required.

### 4.4 Determine what needs to be learned, decided, or changed

Not every gap requires research.

The team determines what kind of work is actually needed.

Examples:

- learn whether customers value the capability
- decide whether to pursue the opportunity
- resolve a design conflict
- implement a capability
- validate a performance requirement
- determine whether an assumption remains valid
- clarify an ambiguous or consequential input
- determine whether a proposed solution actually addresses the intended outcome

### 4.5 Choose and perform activity

Select the activity or activities that most usefully address the consequential gaps, taking account of consequences, uncertainty, cost, dependencies, and available capacity.

Independent activities may be performed concurrently.

The methodology does not prescribe an optimization formula or activity-selection algorithm.

### 4.6 Update the artifact state

The results of meaningful work become persistent artifacts or changes to existing artifacts.

This may include new knowledge, decisions, designs, implementations, evidence, validation results, or changed relationships.

### 4.7 Reassess

After meaningful work or material change, reassess the resulting state.

Previous plans, assumptions, decisions, and conclusions must not be treated as automatically valid merely because they existed before.

---

## 5. Consequential Decisions

A consequential decision is a decision whose consequences materially affect the Change.

Consequential decisions should be represented as artifacts when their consequences need to remain part of the development state.

A decision should have a basis appropriate to its consequences.

The methodology does not require certainty before making a decision.

When uncertainty remains:

1. determine whether more work can materially improve the basis;
2. determine whether the remaining uncertainty is acceptable;
3. if appropriate, explicitly accept the uncertainty through the responsible authority;
4. otherwise continue work or change/abandon the Change.

A decision may also conclude that a Change should be:

- pursued
- modified
- deferred
- superseded
- abandoned

A decision is not required to produce implementation.

---

## 6. Evidence, Knowledge, and Authority

The methodology distinguishes between what is:

- observed
- hypothesized
- proposed
- decided
- accepted
- validated
- otherwise authoritative

The exact labels are implementation choices.

The important property is that artifacts relied upon as authoritative can be distinguished from exploratory or proposed artifacts.

Evidence should support the claims or decisions for which it is being used.

Evidence does not automatically justify conclusions beyond its applicability.

For example:

> Ten interviews with early adopters may support a hypothesis about early adopters without proving demand across the entire market.

Similarly:

> Successful implementation of a feature does not prove that the intended product outcome has been achieved.

Interpretations of input are also subject to this distinction. An interpretation may be useful and well-supported without being the same thing as the original input or an established intended outcome.

---

## 7. Assurance and Proportionality

Investigation, validation, verification, testing, and other assurance activities should be proportionate to:

- uncertainty
- risk
- consequences
- reversibility
- the decision or action being supported

The methodology does not require maximum rigor everywhere.

A low-consequence reversible decision may require little investigation.

A high-consequence irreversible decision may require substantial evidence and assurance.

The same proportionality applies when scrutinizing an initial input. Not every statement requires formal interpretation or clarification. Greater scrutiny is justified when ambiguity or uncertainty could materially change the Change or make acting on the wrong interpretation costly.

The relevant question is:

> Is the available basis sufficient for the decision or action we are about to take?

Not:

> Have we eliminated all uncertainty?

---

## 8. Iteration and Change of Direction

The methodology does not assume that the original plan or hypothesis is correct.

New evidence may cause the team to:

- modify scope
- change the intended outcome
- change an approach
- create a new Change
- supersede an existing Change
- abandon a Change

Historical artifacts remain valuable because they preserve why earlier conclusions were reached.

A changed direction should therefore normally be represented rather than silently rewriting history.

This applies to understanding the intended outcome as well as to knowledge about the product. As understanding changes, what the team is trying to achieve may itself change.

---

## 9. Multiple Changes and Interactions

A product may contain many concurrent Changes.

A material change to one part of the artifact state may affect other Changes through Relationships.

Therefore reassessment should consider affected:

- artifacts
- relationships
- decisions
- assumptions
- dependencies
- Changes

The methodology permits parallel work where dependencies allow it.

It does not require all work to occur in a single global sequence.

---

## 10. The Four Invariants

### I1 — Persistence

**Meaningful development work must leave its relevant results in persistent artifacts.**

### I2 — Outcome orientation

**A Change must establish an intended transformation against which its current state and results can be assessed.**

The intended outcome should not be assumed to be accurately established merely because an initial request or statement has been provided. Where necessary, the input should be scrutinized sufficiently to establish what outcome is actually being pursued.

### I3 — Epistemic integrity

**The artifact state must not represent consequential knowledge, decisions, evidence, or results as more authoritative, certain, supported, applicable, or achieved than their basis justifies.**

This includes avoiding:

- treating hypotheses as facts
- treating proposals as authoritative decisions
- treating interpretations as if they were the original input
- treating an inferred intent as confirmed intent
- overstating evidence
- generalizing evidence beyond its applicability
- representing implementation as outcome achievement
- concealing material uncertainty
- silently ignoring material contradictory evidence

### I4 — Feedback

**After meaningful work or material change, the current state must be reassessed and subsequent work must respond to what that reassessment reveals.**

---

## 11. What the Methodology Can and Cannot Guarantee

The methodology provides disciplined progression and representation. It does not replace human judgment.

### Methodology failures

These are failures to maintain the methodology itself, such as:

- losing meaningful work or its results
- losing connection to the intended outcome
- overstating knowledge or evidence
- hiding material contradictions
- treating an interpretation as established without sufficient basis
- failing to reassess after meaningful change

### Judgment failures

A team can follow the methodology and still make a bad decision.

Examples:

- selecting the wrong market
- misunderstanding customers
- choosing the wrong architecture
- prioritizing the wrong opportunity
- accepting an inappropriate business risk
- incorrectly interpreting an ambiguous request

The methodology improves the basis for judgment; it cannot guarantee that judgment is correct.

### Organizational and external failures

The methodology does not solve:

- lack of decision authority
- insufficient resources
- organizational conflict
- missing expertise
- legal interpretation
- external market conditions
- incompatible strategic objectives

The methodology can represent these conditions and make their consequences visible, but it cannot eliminate them.

### Core boundary

> **The methodology structures human judgment; it does not replace it.**

---

## 12. Methodology Boundaries

The methodology deliberately does not prescribe:

- a specific product lifecycle
- phases
- Agile, Scrum, Kanban, Waterfall, or another management framework
- organizational roles
- project-management tooling
- document formats
- specific specification languages
- architecture methods
- programming languages
- AI tools
- agent architectures
- approval workflows
- estimation formulas
- prioritization formulas

These may be selected by an implementation or organization as appropriate.

The methodology also does not require AI.

It must remain usable by humans without AI.

---

## 13. Summary

The methodology can be summarized as:

> **Maintain a persistent, connected representation of what we are trying to achieve and what we currently know; where necessary, scrutinize the initial input to establish what outcome is actually being pursued; identify the consequential gaps between the current state and the intended outcome; choose and perform useful activities to address those gaps; preserve the resulting knowledge and decisions; and continually reassess the state as it changes.**

The methodology remains deliberately small:

```text
Four primitives:
    Change
    Artifact
    Activity
    Relationship

Control loop:
    Assess
    Identify gaps
    Determine what is needed
    Act
    Update
    Reassess

Four invariants:
    Persistence
    Outcome orientation
    Epistemic integrity
    Feedback
```