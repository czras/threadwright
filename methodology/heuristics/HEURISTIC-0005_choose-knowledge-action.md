# HEURISTIC-0005 — Choose Knowledge-Generating Action

> Given a consequential gap, select the action that provides the greatest expected reduction in consequential uncertainty for the least total cost.

## When to Use

- Facing a consequential gap (see [HEURISTIC-0001_address-consequential-gaps](HEURISTIC-0001_address-consequential-gaps.md))
- Deciding what to do next in the control loop
- Choosing between analysis and experimentation
- Evaluating whether to invest in more manufactured knowledge or move to experiential knowledge

## The Optimization Principle

```
Expected Value = Consequential Uncertainty Reduced / Total Cost of Obtaining Knowledge
```

This is not a literal calculation. It is a thinking frame for comparing options.

## Cost of Learning (Total Cost)

Consider all dimensions, not just financial:

| Dimension | Examples |
|-----------|----------|
| Time | Calendar time, engineering hours |
| Money | Direct costs, budget |
| Opportunity Cost | What else could be done |
| Cognitive Effort | Mental load, complexity |
| Operational Disruption | Impact on running systems |
| Physical Resources | Materials, equipment |
| Risk | Safety, security, compliance |
| Irreversibility | Can this be undone? |
| Ethical Cost | Harm to people, trust |
| Reputational Cost | Customer trust, brand |

## Manufactured Knowledge Actions

| Action | Typical Cost Profile | Best When |
|--------|---------------------|-----------|
| Reason / Analyse | Low time, low risk | Uncertainty is logical/conceptual |
| Research / Literature | Low-medium time | Existing knowledge likely exists |
| Model / Calculate | Medium time, low risk | System amenable to formalization |
| Simulate | Medium-high time, low risk | Reality is expensive/dangerous |
| Consult Experts | Low-medium time | Tacit knowledge exists elsewhere |
| Construct Hypotheses | Low time | Need to structure uncertainty |

## Experiential Knowledge Actions

| Action | Typical Cost Profile | Best When |
|--------|---------------------|-----------|
| Prototype | Medium time, medium risk | Need tangible feedback on approach |
| Experiment | Medium-high time, variable risk | Causal relationships unclear |
| Test | Medium time, medium risk | Validating specific behavior |
| Interview / Observe | Low-medium time | Human behavior/context is key uncertainty |
| Deploy (limited) | High time, higher risk | System behavior in real context unknown |
| Operate | High time, operational risk | Long-term behavior matters |
| Measure | Low-medium time | Quantitative evidence needed |

## Decision Process

1. **Identify the consequential gap** — What specific uncertainty blocks progress?
2. **List candidate actions** — Both manufactured and experiential options
3. **Estimate for each**:
   - Expected consequential uncertainty reduction (rough: high/medium/low)
   - Total cost across all dimensions
   - Risk/irreversibility
4. **Compare** — Which gives best uncertainty reduction per cost?
5. **Check boundary conditions**:
   - Is experiential action premature? (further analysis cheaper)
   - Is manufactured action over-engineering? (reality would answer cheaper)
   - Are we preserving alternatives when evidence is weak? (see preserve-alternatives.md — future heuristic)
6. **Decide and record** — Document the choice and reasoning in artifacts

## Anti-Patterns to Avoid

- **Over-manufacturing**: Excessive analysis when a cheap prototype would answer the question
- **Premature exposure**: Deploying to production when simulation would catch the issue
- **Single-mode bias**: Always defaulting to "more research" or "just build it"
- **Ignoring irreversibility**: Treating a one-way door as a two-way door
- **Cost myopia**: Counting only engineering hours, not opportunity cost or risk

## Related Heuristics

- [HEURISTIC-0006_dynamic-think-experience-boundary](HEURISTIC-0006_dynamic-think-experience-boundary.md) — Recognizing when the boundary shifts
- [HEURISTIC-0001_address-consequential-gaps](HEURISTIC-0001_address-consequential-gaps.md) — Identifying what gaps matter
- [HEURISTIC-0004_reassess](HEURISTIC-0004_reassess.md) — Re-evaluating after action produces evidence

## Related Scenarios

- [SCENARIO-0005_optimization-invariant-i5](../scenarios/SCENARIO-0005_optimization-invariant-i5.md) — Full worked example of action sequencing
- [SCENARIO-0004_dynamic-think-experience-boundary](../scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md) — Boundary shifts across phases
- [SCENARIO-0006_manufactured-vs-experiential-artifacts](../scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md) — Origin-aware action selection
- [SCENARIO-0007_evolve-intent-from-messy-input](../scenarios/SCENARIO-0007_evolve-intent-from-messy-input.md) — Log analysis (manufactured) vs building (experiential)

## References

- [ASSESSMENT-0008_manufactured-vs-evolved §5-7](../artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation) — Central formulation, knowledge-generating actions, cost of learning
- [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §5, 8](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge) — Manufactured vs experiential, cost of learning
- [threadwright.md §2, 6, 8](../threadwright.md) — Core model, consequential gaps, I5 Optimization invariant