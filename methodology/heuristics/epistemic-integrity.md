# Cross-Cutting Heuristic — Epistemic Integrity

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

This heuristic directly implements [I3 Epistemic Integrity](../threadwright.md#i3--epistemic-integrity). Tag evidence with its epistemic origin:

- **Manufactured**: reasoning, analysis, simulation, vendor claims, opinions
- **Experiential**: observation, experiment, deployment, measurement, prototype results

Manufactured knowledge carries assumptions that may not hold in reality; experiential knowledge is grounded but context-specific — see [threadwright.md §7](../threadwright.md#7-consequential-decisions-and-evidence).

## Related Heuristics

- [choose-knowledge-action.md](choose-knowledge-action.md) — Origin-aware action selection
- [address-consequential-gaps.md](address-consequential-gaps.md) — Gaps filtered by evidence quality

## Related Scenarios

- [Manufactured vs Experiential Knowledge in Artifacts](../scenarios/manufactured-vs-experiential-artifacts.md) — Full worked example with epistemic tagging
- [Optimization Invariant (I5) Stress Test](../scenarios/optimization-invariant-i5.md) — Model (manufactured) vs load test (experiential) evidence

## References

- [threadwright.md §5, §7, §8](../threadwright.md) — Artifact system, decisions/evidence, I3
- [ASSESSMENT-0008 §5, 6](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation) — Central formulation, knowledge-generating actions
- [ASSESSMENT-0009 §5](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge) — Manufactured vs evolved knowledge
