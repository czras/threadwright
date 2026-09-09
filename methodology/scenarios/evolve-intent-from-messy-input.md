# Scenario — Evolving Intent from Messy Input

## Situation

A stakeholder sends: "Our dashboard is too slow. We need a caching layer. Can you estimate when it'll be done?"

This input contains: a problem statement (slow), a proposed solution (caching layer), and a request (estimate).

## Application

**Step 1 — Capture raw input**
```
Artifact: Stakeholder request (verbatim)
```

**Step 2 — Decompose into components**
| Component | Extracted |
|-----------|-----------|
| Outcome | "Dashboard is faster" |
| Problem | "Dashboard load time unacceptable" |
| Assumption | "Caching will solve it" |
| Proposed Implementation | "Add caching layer" |
| Constraint | "Need estimate for planning" |

**Step 3 — Identify consequential ambiguities**
- *What is "too slow"?* (If 8s → 2s matters, but 8s → 7s doesn't)
- *Is caching the right solution?* (Maybe query optimization, pagination, or materialized views are better)
- *What's the cost of wrong solution?* (Weeks of engineering on wrong approach)

**Step 4 — Formulate candidate intents**
- Intent A: Reduce dashboard p95 load time from 8s to <2s
- Intent B: Reduce dashboard infrastructure cost by 50%
- Intent C: Enable real-time dashboard for ops team

**Step 5 — Identify gaps for each candidate**
| Intent | Consequential Gaps |
|--------|-------------------|
| A | Which queries are slowest? What are their execution plans? |
| B | What is current query cost breakdown? |
| C | What latency threshold feels "real-time" to ops? |

**Step 6 — Select knowledge-generating actions (I5 Optimization)**
```
Gap: "Which queries are slowest?"
    ↓
Options:
  - Analyse query logs (manufactured, 2 hours, high uncertainty reduction)
  - Add tracing and wait (experiential, 1 week, high uncertainty reduction)
    ↓
Choice: Analyse query logs first (cheaper, same info)
```

**Step 7 — Execute, capture evidence, evolve intent**
```
Action: Query log analysis
    ↓
Evidence: 3 queries account for 80% of latency; all missing indexes
    ↓
Reassess:
  - Intent A sharpens: "Add missing indexes on 3 queries"
  - Proposed "caching layer" deprioritized (not the bottleneck)
  - New gap: "Will indexes alone achieve <2s p95?"
```

**Step 8 — Continue loop**
```
Gap: "Will indexes alone achieve <2s?"
    ↓
Action: Add indexes in staging, measure (experiential)
    ↓
Evidence: p95 drops to 1.8s
    ↓
Intent A satisfied. Stakeholder estimate: "Done this sprint."
```

## Demonstrates

- Threadwright does not treat the proposed solution (caching) as the intent
- Messy input is decomposed; consequential ambiguities are scrutinized
- Multiple candidate intents preserved until evidence favors one
- I5 Optimization selects cheapest knowledge-generating action (log analysis vs. building caching)
- Intent evolves from "caching layer" → "reduce query latency via indexes"
- The trail from messy input to final intent is preserved in artifacts

## Tests

- [ ] Raw input captured verbatim before interpretation
- [ ] Input decomposed into outcome/problem/assumption/implementation/constraint
- [ ] Consequential ambiguities identified and prioritized
- [ ] Multiple candidate intents formulated
- [ ] Gaps identified for each candidate
- [ ] Action selection uses I5 Optimization (manufactured vs experiential compared)
- [ ] Intent evolution recorded with evidence trail
- [ ] Final intent differs from proposed solution in input

## References

- [threadwright.md §3, 4, 6, 8](../threadwright.md) — Intent, control loop, consequential gaps, I5
- [evolve-intent-from-messy-input.md](../heuristics/evolve-intent-from-messy-input.md)
- [choose-knowledge-action.md](../heuristics/choose-knowledge-action.md)
- [ASSESSMENT-0009 §4](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent)
- [ASSESSMENT-0003](artifacts/ASSESSMENT-0003_input-scrutiny-and-extraction.md)