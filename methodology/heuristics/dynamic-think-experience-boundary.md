# Heuristic: Dynamic Think/Experience Boundary

> The boundary between manufactured and experiential knowledge is not fixed. It moves within the same project as knowledge changes. Recognize when to shift.

## The Core Insight

The question is not "are we a thinking organization or an experimental organization?" The question is: **what is the best way to reduce this particular consequential uncertainty right now?**

The optimal next action changes as the epistemic state changes — see [ASSESSMENT-0008 §3](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#3-the-dynamic-thinklearn-boundary) and [ASSESSMENT-0009 §6](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#6-the-thinkexperience-boundary-is-dynamic).

## Typical Boundary Trajectory

```
Research → Prototype → Observe → Analyse → Simulate → Experiment → Deploy → Observe → Rethink
```

At each step, the remaining uncertainty shifts, and with it the optimal knowledge-generating mechanism.

## Signals the Boundary Should Shift Toward Experience (Manufactured → Experiential)

| Signal | Example |
|--------|---------|
| Analysis producing diminishing returns | Third architecture diagram doesn't clarify the real constraint |
| Assumptions piling up unvalidated | "We assume users want X" — but no one has asked |
| Simulation fidelity insufficient | Model can't capture the emergent behavior that matters |
| Cost of being wrong in reality is now acceptable | Early prototype risk is low; production risk was high |
| Consequential gap is about human behavior | No amount of reasoning reveals what users actually do |
| Feedback loop too long | "Let's think more" has become procrastination |

**Heuristic**: When abstraction stops producing useful knowledge, move closer to reality.

## Signals the Boundary Should Shift Toward Manufacture (Experiential → Manufactured)

| Signal | Example |
|--------|---------|
| Experiments repeating same failure | Prototype keeps breaking at same point — need root cause analysis |
| Cost of next experiment is very high | Next test requires production deployment |
| Risk of experiential action is unacceptable | Safety, compliance, or ethical boundary |
| Uncertainty shifted to architecture/scalability | "It works for 10 users, will it work for 10M?" |
| Need to generalize from observations | Raw experimental data needs synthesis into principles |
| Multiple competing experiential results | Need analysis to reconcile contradictory evidence |

**Heuristic**: When experience produces noise instead of signal, step back and manufacture understanding.

## Practical Check: The Boundary Question

Before each action in the control loop, ask:

> **Given what we now know, is the cheapest way to learn the next thing manufactured or experiential?**

If the answer changed since last time, the boundary moved. This is normal and expected.

## Anti-Patterns

- **Fixed boundary**: "We're an agile team, we always prototype first" or "We're safety-critical, we always simulate first"
- **Boundary denial**: Continuing analysis when a 2-hour prototype would answer the question, or building when a 30-minute calculation would reveal the flaw
- **Boundary thrashing**: Rapidly switching without letting either mode produce useful knowledge
- **Sunk-cost boundary**: Staying in current mode because "we've already invested so much in this analysis/prototype"

## Recording Boundary Decisions

Document in artifacts:
- What was the consequential gap?
- What was the current epistemic state?
- Which mode was chosen and why?
- What was the outcome?
- Did the boundary shift afterward?

This builds organizational meta-knowledge about **which methods work under which conditions** — see [ASSESSMENT-0008 §13](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#13-recursive-learning-about-learning).

## Related Heuristics

- [choose-knowledge-action.md](choose-knowledge-action.md) — The broader action selection framework
- [forward-deployment.md](forward-deployment.md) — Moving closer to reality as a specific mechanism (future heuristic)
- [reassess.md](reassess.md) — Re-evaluating after evidence arrives

## Related Scenarios

- [Dynamic Think/Experience Boundary Shift](../scenarios/dynamic-think-experience-boundary.md) — Full 4-phase trajectory
- [Optimization Invariant (I5) Stress Test](../scenarios/optimization-invariant-i5.md) — Model → load test boundary shift
- [Evolving Intent from Messy Input](../scenarios/evolve-intent-from-messy-input.md) — Analysis → prototype boundary shift

## References

- [ASSESSMENT-0008 §3, 9, 14](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#3-the-dynamic-thinklearn-boundary) — Dynamic boundary, forward deployment, core loop
- [ASSESSMENT-0009 §6, 9](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#6-the-thinkexperience-boundary-is-dynamic) — Dynamic boundary, forward deployment as special case
- [threadwright.md §2, 4, 6](../threadwright.md) — Core model, control loop, consequential gaps