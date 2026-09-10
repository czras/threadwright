# HEURISTIC-0001 — Address Consequential Gaps

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

Only the final category warrants knowledge-generating action — see [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#7-consequential-uncertainty-remains-the-important-target).

## Selecting the Knowledge-Generating Action

Once a consequential gap is identified, choose the action that provides the greatest expected reduction in consequential uncertainty for the least total cost — see [HEURISTIC-0005_choose-knowledge-action](HEURISTIC-0005_choose-knowledge-action.md) and [INVARIANT-0005_optimization](../invariants/INVARIANT-0005_optimization.md).

The action may be:
- **Manufactured**: reason, research, analyse, model, calculate, simulate
- **Experiential**: prototype, experiment, test, interview, deploy, observe, measure

The dynamic boundary between these modes shifts as knowledge changes — see [HEURISTIC-0006_dynamic-think-experience-boundary](HEURISTIC-0006_dynamic-think-experience-boundary.md).

## Anti-Patterns

- **Gap inflation**: Treating every unknown as consequential
- **Gap neglect**: Ignoring gaps that could invalidate downstream work
- **Single-mode response**: Always researching, always prototyping, always analysing
- **Cost blindness**: Pursuing knowledge without considering total cost (time, risk, opportunity, irreversibility)
- **Action without gap**: Doing work that doesn't target a consequential gap

## Related Heuristics

- [HEURISTIC-0005_choose-knowledge-action](HEURISTIC-0005_choose-knowledge-action.md) — How to select the action
- [HEURISTIC-0006_dynamic-think-experience-boundary](HEURISTIC-0006_dynamic-think-experience-boundary.md) — Recognizing when to shift modes
- [HEURISTIC-0004_reassess](HEURISTIC-0004_reassess.md) — Re-evaluating gaps after evidence
- [HEURISTIC-0007_evolve-intent-from-messy-input](HEURISTIC-0007_evolve-intent-from-messy-input.md) — Gaps may reshape intent

## Related Scenarios

- [SCENARIO-0005_optimization-invariant-i5](../scenarios/SCENARIO-0005_optimization-invariant-i5.md) — Action selection in practice
- [SCENARIO-0004_dynamic-think-experience-boundary](../scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md) — Boundary shifts during gap resolution
- [SCENARIO-0006_manufactured-vs-experiential-artifacts](../scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md) — Epistemic origin in gap evidence

## References

- [ASSESSMENT-0008_manufactured-vs-evolved §4, 5](../artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#4-consequential-gaps) — Consequential gaps, central formulation
- [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §7](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#7-consequential-uncertainty-remains-the-important-target) — Consequential uncertainty progression
- [threadwright.md §6, 8](../threadwright.md) — Consequential gaps, I5 Optimization invariant