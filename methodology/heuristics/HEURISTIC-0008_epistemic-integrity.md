# HEURISTIC-0008 — Epistemic Integrity

> **Do not represent a claim, decision, or result as more certain, supported, applicable, authoritative, or achieved than the available basis justifies.**

Distinguish:

- observation from interpretation;
- input from interpretation;
- proposal from decision;
- implementation from outcome;
- evidence from conclusions beyond its applicability;
- accepted uncertainty from hidden uncertainty;
- consequential disagreement from apparent consensus;
- **manufactured knowledge from experiential knowledge**.

For example:

```text
Input:
    We need a mobile app.

Interpretation:
    The requester appears to believe a mobile app is an
    appropriate means of solving the problem.

Candidate outcome:
    Field workers need to access and update information
    while away from their desks.
```

The interpretation and candidate outcome are not automatically authoritative.

AI-generated or human-generated proposals do not become decisions merely because they are written down.

Successful implementation does not prove that the intended outcome has been achieved.

## Manufactured vs Experiential Knowledge

This heuristic directly implements [INVARIANT-0003_epistemic-integrity](../invariants/INVARIANT-0003_epistemic-integrity.md). Tag evidence with its epistemic origin:

- **Manufactured**: reasoning, analysis, simulation, vendor claims, opinions
- **Experiential**: observation, experiment, deployment, measurement, prototype results

Manufactured knowledge carries assumptions that may not hold in reality; experiential knowledge is grounded but context-specific — see [threadwright.md §7](../threadwright.md#7-consequential-decisions-and-evidence).

## Related Heuristics

- [HEURISTIC-0005_choose-knowledge-action](HEURISTIC-0005_choose-knowledge-action.md) — Origin-aware action selection
- [HEURISTIC-0001_address-consequential-gaps](HEURISTIC-0001_address-consequential-gaps.md) — Gaps filtered by evidence quality

## Related Scenarios

- [SCENARIO-0006_manufactured-vs-experiential-artifacts](../scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md) — Full worked example with epistemic tagging
- [SCENARIO-0005_optimization-invariant-i5](../scenarios/SCENARIO-0005_optimization-invariant-i5.md) — Model (manufactured) vs load test (experiential) evidence

## References

- [threadwright.md §5, §7, §8](../threadwright.md) — Artifact system, decisions/evidence, I3
- [ASSESSMENT-0008_manufactured-vs-evolved §5, 6](../artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation) — Central formulation, knowledge-generating actions
- [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §5](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge) — Manufactured vs evolved knowledge