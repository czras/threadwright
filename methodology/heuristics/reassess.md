# H4 — Reassess

> **After meaningful work or material change, reassess the current state rather than assuming previous plans, assumptions, decisions, or conclusions remain valid.**

Reassessment should consider affected artifacts, relationships, assumptions, decisions, dependencies, Changes, and intended outcomes.

Reassessment permits changing direction, abandoning work, revising scope, superseding decisions, discovering new problems, reacting to production evidence, and exploiting unexpected opportunities.

A plan is a useful artifact, not a commitment to ignore reality.

## Reassessment in the Adaptive Control Loop

Threadwright's control loop is explicitly adaptive — the optimal next action depends on the current epistemic state — see [threadwright.md §4](../threadwright.md#4-control-loop) and [ASSESSMENT-0009 §10](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#10-adaptive).

Reassessment is where adaptation happens:

```
Evidence from Action
       ↓
Reassess: What changed?
       ↓
- Knowledge state?
- Consequential gaps?
- Intent?
- Think/experience boundary?
       ↓
Select next knowledge-generating action
```

## What to Reassess

| Dimension | Questions |
|-----------|-----------|
| **Knowledge** | What new manufactured/experiential knowledge do we have? What assumptions were validated/invalidated? |
| **Gaps** | Which consequential gaps closed? Which new ones opened? Which shifted priority? |
| **Intent** | Does the evidence change what we're trying to achieve? (See [evolve-intent-from-messy-input.md](evolve-intent-from-messy-input.md)) |
| **Boundary** | Did the think/experience boundary shift? Should next action be manufactured or experiential? (See [dynamic-think-experience-boundary.md](dynamic-think-experience-boundary.md)) |
| **Decisions** | Do any consequential decisions need revision or supersession? |
| **Relationships** | Do artifact relationships need updating? (supports, derived from, contradicts, supersedes) |

## When to Reassess

- After any knowledge-generating action produces evidence
- After material change in context (market, technology, team, constraints)
- When a consequential decision is made or reversed
- When a Change is completed, abandoned, or superseded
- At regular intervals for long-running work (cadence proportional to volatility)

## Anti-Patterns

- **Plan persistence**: Continuing a plan because "we already decided" despite contrary evidence
- **Reassessment theater**: Going through motions without genuinely questioning assumptions
- **Scope creep reassessment**: Using reassessment to add work without closing gaps
- **Boundary rigidity**: Reassessing gaps but not the think/experience boundary
- **Intent freezing**: Updating knowledge but not letting intent evolve

## Recording Reassessment

Document in artifacts:
- What triggered the reassessment?
- What was the previous state?
- What evidence or change prompted it?
- What changed in knowledge, gaps, intent, boundary?
- What is the new selected action and why?

This builds the recursive knowledge that lets Threadwright improve its own practice — see [ASSESSMENT-0008 §11](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#11-threadwrights-recursive-property) and [ASSESSMENT-0009 §14](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#14-recursive-self-application).

## Related Heuristics

- [address-consequential-gaps.md](address-consequential-gaps.md) — Identifying gaps to reassess
- [choose-knowledge-action.md](choose-knowledge-action.md) — Selecting the next action after reassessment
- [dynamic-think-experience-boundary.md](dynamic-think-experience-boundary.md) — Checking boundary shift
- [evolve-intent-from-messy-input.md](evolve-intent-from-messy-input.md) — Intent may evolve from evidence

## Related Scenarios

- [Recursive Self-Application](../scenarios/recursive-self-application.md) — Reassessment driving methodology evolution
- [Dynamic Think/Experience Boundary Shift](../scenarios/dynamic-think-experience-boundary.md) — Boundary check in reassessment
- [Optimization Invariant (I5) Stress Test](../scenarios/optimization-invariant-i5.md) — Reassessment after each action

## References

- [ASSESSMENT-0008 §14](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#14-emerging-core-loop) — Core loop with reassessment
- [ASSESSMENT-0009 §10, 14](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#10-adaptive) — Adaptive character, recursive self-application
- [threadwright.md §4, 8, 11](../threadwright.md) — Control loop, I4 Feedback invariant, recursive self-application
