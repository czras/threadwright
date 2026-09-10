# SCENARIO-0004 — Dynamic Think/Experience Boundary Shift

## Situation

A team is building a real-time collaboration feature. Initial consequential gap: "Will users adopt real-time editing?"

## Application

**Phase 1 — Manufactured knowledge (Research/Analysis)**
```
Gap: "Will users adopt real-time editing?"
    ↓
Action: User research, competitive analysis, survey
    ↓
Evidence: Users say "yes, very important" in surveys
    ↓
Reassess: Gap shifts to "Can we build it with acceptable latency?"
```

**Phase 2 — Boundary shifts toward experience (Prototype)**
```
Gap: "Can we build it with acceptable latency?"
    ↓
Action: Build minimal prototype (operational transform / CRDT)
    ↓
Evidence: Prototype achieves 50ms latency locally, 200ms cross-region
    ↓
Reassess: Gap shifts to "Does 200ms cross-region feel real-time to users?"
```

**Phase 3 — Boundary shifts back toward manufacture (Simulation/Analysis)**
```
Gap: "Does 200ms cross-region feel real-time?"
    ↓
Action: Simulated user study with injected latency, literature review on perception thresholds
    ↓
Evidence: Research shows 150ms threshold for "perceived simultaneity"; 200ms feels laggy
    ↓
Reassess: Gap shifts to "Can we reduce cross-region latency to <150ms?"
```

**Phase 4 — Boundary shifts to experience again (Deployment experiment)**
```
Gap: "Can we reduce cross-region latency to <150ms?"
    ↓
Action: Deploy edge workers in 3 regions, measure real user latency
    ↓
Evidence: 95th percentile 120ms cross-region
    ↓
Reassess: Gap closed. Move to rollout.
```

## Demonstrates

- The think/experience boundary is **dynamic**, not a fixed methodology choice
- Each reassessment asks: "Given current knowledge, what's the cheapest way to learn the next thing?"
- Manufactured knowledge (research, simulation) and experiential knowledge (prototype, deployment) interleave
- The boundary shift is recorded in artifacts, building meta-knowledge about which methods work when
- INVARIANT-0005 Optimization invariant guides each choice: maximize consequential uncertainty reduction per cost

## Tests

- [ ] Team explicitly identifies the consequential gap at each phase
- [ ] Team evaluates both manufactured and experiential options before choosing
- [ ] Team records why the boundary shifted (what changed in epistemic state)
- [ ] Team avoids over-manufacturing (e.g., more surveys when prototype would answer)
- [ ] Team avoids premature exposure (e.g., full deployment when simulation sufficed)
- [ ] Artifacts distinguish manufactured vs experiential knowledge origin

## References

- [threadwright.md §2, 6, 8](../threadwright.md) — Core model, consequential gaps, INVARIANT-0005 Optimization
- [HEURISTIC-0006_dynamic-think-experience-boundary](../heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md)
- [HEURISTIC-0005_choose-knowledge-action](../heuristics/HEURISTIC-0005_choose-knowledge-action.md)
- [ASSESSMENT-0008_manufactured-vs-evolved §3](../artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#3-the-dynamic-thinklearn-boundary)
- [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §6](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#6-the-thinkexperience-boundary-is-dynamic)