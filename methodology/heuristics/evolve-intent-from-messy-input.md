# Heuristic: Evolve Intent from Messy Input

> Initial requests rarely express clear intent. Turn messy input into increasingly useful intent while simultaneously evolving the knowledge required to pursue it.

## The Problem

Input comes in many forms — see [ASSESSMENT-0009 §4](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent):

- An observation ("users complain about slowness")
- An anomaly ("conversion dropped 15% last week")
- A curiosity ("what if we used Rust?")
- A contradiction ("sales wants feature X, engineering says it's impossible")
- An unexpected result ("the A/B test showed no difference")
- A poorly formulated question ("how do we fix the dashboard?")
- An intuition ("something feels wrong about this architecture")
- A proposed solution ("we need a microservices rewrite")
- A constraint ("we must launch by Q3")
- A mixture of the above

None of these are intent. They are **starting material** for intent evolution.

## The Progression

```
Messy Input
    ↓
Scrutinize & Formulate
    ↓
Identify Consequential Gaps
    ↓
Select Knowledge-Generating Action
    ↓
Evidence
    ↓
Updated Intent
    ↓
Updated Gaps → Repeat
```

This is the Threadwright control loop — see [threadwright.md §4](../threadwright.md#4-control-loop) and [ASSESSMENT-0009 §4](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent).

## Scrutiny Proportionality

The degree of scrutiny should be proportional to:

- **Ambiguity** — How many interpretations are possible?
- **Uncertainty** — How much is unknown about the domain?
- **Consequence** — What happens if we act on a mistaken interpretation?
- **Reversibility** — Can we undo the commitment?
- **Cost of error** — Time, money, trust, opportunity

Low proportionality → lightweight clarification. High proportionality → structured scrutiny (see [ASSESSMENT-0003](artifacts/ASSESSMENT-0003_input-scrutiny-and-extraction.md)).

## Practical Steps

### 1. Capture the Raw Input

Record the input verbatim as an artifact. Don't interpret yet.

### 2. Decompose Into Components

Separate the input into:
- **Outcomes** — What result is desired?
- **Problems** — What pain or gap is described?
- **Assumptions** — What is taken for granted?
- **Constraints** — What boundaries exist?
- **Proposed implementations** — What solution is suggested?
- **Interpretations** — What meaning is assigned?

### 3. Identify the Consequential Ambiguities

For each component, ask: *If we're wrong about this, does it matter?*

Focus scrutiny on ambiguities that are consequential — see [address-consequential-gaps.md](address-consequential-gaps.md).

### 4. Formulate Candidate Intents

Generate multiple candidate intent statements. Keep them explicit and distinct.

Example from "we need a faster dashboard":
- Intent A: Reduce dashboard load time from 8s to <2s for 95th percentile
- Intent B: Enable real-time data visibility for ops team during incidents
- Intent C: Reduce infrastructure cost of dashboard queries by 50%
- Intent D: All of the above (but priority order matters)

### 5. Identify Gaps for Each Candidate

For each candidate intent, what consequential gaps exist?
- Intent A gap: Don't know which queries are slowest
- Intent B gap: Don't know what "real-time" means for ops workflows
- Intent C gap: Don't know current query cost breakdown

### 6. Select Knowledge-Generating Actions

Use [choose-knowledge-action.md](choose-knowledge-action.md) to pick actions that reduce the most consequential gaps per cost.

### 7. Update Intent from Evidence

As evidence arrives, intent evolves:
- Gaps close → intent sharpens
- New gaps emerge → intent expands or shifts
- Evidence contradicts → intent revises

**Record each evolution** — the trail from messy input to current intent is valuable knowledge.

## Key Principles

### Intent Is Not Fixed at the Start

> The ability to turn messy input into a useful hypothesis is itself an acquired capability.

Don't demand perfect intent upfront. Demand **explicit, evolving intent**.

### Multiple Interpretations Can Coexist

When evidence is weak and consequences of being wrong are high, preserve alternative intent candidates — see [ASSESSMENT-0009 §4](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent) and [RESEARCH-0000 §7](artifacts/RESEARCH-0000_evolutionary-computation.md#7-diversity-and-premature-convergence).

### Scrutiny Is Not Analysis Paralysis

Scrutiny targets *consequential* ambiguity. It stops when further clarification costs more than acting on the best current interpretation.

### The Input May Be the Solution, Not the Problem

"Build a caching layer" → scrutiny reveals: the real problem is "database queries are slow" → intent becomes "reduce query latency" → gaps include "which queries?" and "why are they slow?" → action: profile queries.

The proposed solution (caching) becomes *one candidate action* among others.

## Anti-Patterns

- **Premature intent fixation**: Locking in the first interpretation without scrutiny
- **Solution-first thinking**: Treating the proposed implementation as the intent
- **Scrutiny theater**: Doing analysis that doesn't target consequential ambiguities
- **Intent drift without trace**: Intent changes but no record of why or what evidence drove it
- **Ignoring the mixture**: Focusing on one component (e.g., the proposed solution) and missing the constraint or problem

## Related Heuristics

- [address-consequential-gaps.md](address-consequential-gaps.md) — Identifying what gaps matter for intent
- [choose-knowledge-action.md](choose-knowledge-action.md) — Selecting actions to evolve intent
- [reassess.md](reassess.md) — Re-evaluating intent after evidence

## Related Scenarios

- [Evolving Intent from Messy Input](../scenarios/evolve-intent-from-messy-input.md) — Full worked example
- [When the Request Is Not the Intent](../scenarios/when-request-is-not-intent.md) — Related scenario
- [Greenfield Product Idea](../scenarios/greenfield-product-idea.md) — Starting from idea

## References

- [ASSESSMENT-0009 §4](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent) — Messy input and evolving intent
- [ASSESSMENT-0003](artifacts/ASSESSMENT-0003_input-scrutiny-and-extraction.md) — Input scrutiny framework
- [ASSESSMENT-0004](artifacts/ASSESSMENT-0004_establishing-intent-from-input.md) — Establishing intent from input
- [threadwright.md §3, 4](../threadwright.md) — Intent, control loop