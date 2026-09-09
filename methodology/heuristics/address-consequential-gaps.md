# H1 — Address Consequential Gaps

> **Compare the current state with the desired outcome and prioritize gaps that could materially affect the outcome, invalidate downstream work, or make further progress irresponsible.**

Do not treat every unknown or imperfection as equally important.

A consequential gap might concern customer value, a critical constraint, a major technical uncertainty, security, compliance, a dependency, a missing decision, inadequate evidence, an implementation blocker, or a likely source of expensive rework.

The useful question is not:

> What is missing?

It is:

> What missing or unresolved thing matters enough to affect what we should do?

## The Uncertainty Progression

Not all uncertainty is consequential. Filter through:

```
Unknown → Relevant Unknown → Consequential Uncertainty
```

Only the final category warrants knowledge-generating action — see [ASSESSMENT-0009 §7](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#7-consequential-uncertainty-remains-the-important-target).

## Selecting the Knowledge-Generating Action

Once a consequential gap is identified, choose the action that provides the greatest expected reduction in consequential uncertainty for the least total cost — see [choose-knowledge-action.md](choose-knowledge-action.md) and [I5 Optimization](../threadwright.md#i5--optimization).

The action may be:
- **Manufactured**: reason, research, analyse, model, calculate, simulate
- **Experiential**: prototype, experiment, test, interview, deploy, observe, measure

The dynamic boundary between these modes shifts as knowledge changes — see [dynamic-think-experience-boundary.md](dynamic-think-experience-boundary.md).

## Anti-Patterns

- **Gap inflation**: Treeting every unknown as consequential
- **Gap neglect**: Ignoring gaps that could invalidate downstream work
- **Single-mode response**: Always researching, always prototyping, always analysing
- **Cost blindness**: Pursuing knowledge without considering total cost (time, risk, opportunity, irreversibility)
- **Action without gap**: Doing work that doesn't target a consequential gap

## Related Heuristics

- [choose-knowledge-action.md](choose-knowledge-action.md) — How to select the action
- [dynamic-think-experience-boundary.md](dynamic-think-experience-boundary.md) — Recognizing when to shift modes
- [reassess.md](reassess.md) — Re-evaluating gaps after evidence
- [evolve-intent-from-messy-input.md](evolve-intent-from-messy-input.md) — Gaps may reshape intent

## Related Scenarios

- [Optimization Invariant (I5) Stress Test](../scenarios/optimization-invariant-i5.md) — Action selection in practice
- [Dynamic Think/Experience Boundary Shift](../scenarios/dynamic-think-experience-boundary.md) — Boundary shifts during gap resolution
- [Manufactured vs Experiential Knowledge in Artifacts](../scenarios/manufactured-vs-experiential-artifacts.md) — Epistemic origin in gap evidence

## References

- [ASSESSMENT-0008 §4, 5](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#4-consequential-gaps) — Consequential gaps, central formulation
- [ASSESSMENT-0009 §7](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#7-consequential-uncertainty-remains-the-important-target) — Consequential uncertainty progression
- [threadwright.md §6, 8](../threadwright.md) — Consequential gaps, I5 Optimization invariant
