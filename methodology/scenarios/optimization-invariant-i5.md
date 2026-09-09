# Scenario — Optimization Invariant (I5) Stress Test

## Situation

A team faces a consequential gap: "Will the new payment integration handle 10x Black Friday traffic?"

Three candidate actions emerge:
1. **Load test in staging** (experiential) — 2 days, $500, realistic but limited scale
2. **Queuing theory model** (manufactured) — 4 hours, $0, analytical but assumes arrival patterns
3. **Chaos experiment in production** (experiential) — 2 hours, risk of real failures, highest fidelity

## Application

**Step 1 — Frame the optimization**

```
Consequential Gap: "Will payment integration handle 10x traffic?"
Consequence of being wrong: Revenue loss, customer trust, SLA breach
```

**Step 2 — Estimate for each candidate**

| Action | Cost | Expected Uncertainty Reduction | Risk | Irreversibility |
|--------|------|-------------------------------|------|-----------------|
| Load test staging | 2 days, $500 | Medium (staging ≠ prod) | Low | Reversible |
| Queuing model | 4 hours, $0 | Low-Medium (assumptions) | None | Reversible |
| Chaos prod | 2 hours, $0 | High (real traffic) | High (real failures) | Partially irreversible |

**Step 3 — Apply I5 Optimization**

*Iteration 1: Queuing model first*
- Cheapest (4 hours, $0, no risk)
- If model shows clear margin >10x, gap may close without further action
- If model shows tight margin or high sensitivity to assumptions → remaining uncertainty high

```
Action: Build queuing model
    ↓
Evidence: Model shows 8x capacity at current config; highly sensitive to arrival burstiness
    ↓
Reassess: Gap not closed. Remaining uncertainty: "Real burst patterns?"
```

*Iteration 2: Load test staging*
- Now model has narrowed uncertainty to burst pattern behavior
- Load test can simulate burst patterns
- Cost justified because model couldn't resolve burst uncertainty

```
Action: Load test with burst simulation
    ↓
Evidence: System handles 12x with burst patterns; degrades gracefully at 15x
    ↓
Reassess: Gap closed. Chaos experiment not needed.
```

**Step 4 — Record decision rationale**

Artifacts capture:
- Why queuing model first (I5: lowest cost for initial uncertainty reduction)
- Why load test second (model revealed specific uncertainty it couldn't resolve)
- Why chaos experiment skipped (gap closed at lower cost/risk)

## Demonstrates

- I5 Optimization is a thinking frame, not a calculation
- Actions are sequenced by cost-effectiveness, not dogma
- Manufactured knowledge (model) used first because cheapest
- Experiential knowledge (load test) used when manufactured knowledge hits diminishing returns
- High-cost/high-risk action (chaos) avoided because cheaper actions sufficed
- Decision rationale preserved for future meta-learning

## Tests

- [ ] Consequential gap explicitly stated with consequence of being wrong
- [ ] Multiple candidate actions generated (both manufactured and experiential)
- [ ] Cost estimated across dimensions (time, money, risk, irreversibility, opportunity)
- [ ] Expected uncertainty reduction estimated for each
- [ ] Actions sequenced by optimization logic, not habit
- [ ] Reassessment after each action updates the optimization
- [ ] High-risk action avoided when cheaper actions suffice
- [ ] Decision rationale recorded in artifacts

## Anti-Patterns This Scenario Guards Against

- **Default to load test**: "We always load test" → wastes 2 days when 4-hour model might suffice
- **Default to chaos**: "Test in production" → unnecessary risk when staging + model work
- **Analysis paralysis**: Endless modeling when a quick experiment would answer
- **Single-mode**: Only manufactured OR only experiential actions considered

## References

- [threadwright.md §6, 8](../threadwright.md) — Consequential gaps, I5 Optimization
- [choose-knowledge-action.md](../heuristics/choose-knowledge-action.md)
- [address-consequential-gaps.md](../heuristics/address-consequential-gaps.md)
- [ASSESSMENT-0008 §5, 7, 8](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation)
- [ASSESSMENT-0009 §5, 8](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge)