# SCENARIO-0006 — Manufactured vs Experiential Knowledge in Artifacts

## Situation

A team is evaluating a new database technology. They generate multiple knowledge artifacts and must track epistemic origin to avoid overconfidence in manufactured knowledge.

## Application

**Knowledge artifacts created during evaluation:**

| Artifact | Content | Epistemic Origin | Confidence |
|----------|---------|------------------|------------|
| Vendor benchmark doc | "10x faster than Postgres" | Manufactured (vendor claim) | Low — marketing |
| Internal benchmark script | "3x faster on our query pattern" | Experiential (our test) | High — our data |
| Architecture analysis | "Requires significant query rewrite" | Manufactured (analysis) | Medium — theoretical |
| Prototype migration | "2-week effort for 80% of queries" | Experiential (prototype) | High — built it |
| Team Slack discussion | "Seems risky for transactions" | Manufactured (opinion) | Low — anecdotal |
| Jepsen test report | "No data loss under partition" | Experiential (third-party test) | High — rigorous test |

**Step 1 — Tag all artifacts with epistemic origin**

Each artifact gets: `epistemic-origin: manufactured` or `epistemic-origin: experiential`

**Step 2 — Apply epistemic integrity (INVARIANT-0003) during reassessment**

```
Reassessment question: "Should we adopt this database?"
    ↓
Evidence review:
  Manufactured knowledge:
    - Vendor claims (low confidence)
    - Architecture analysis (medium confidence)
    - Team opinions (low confidence)
  Experiential knowledge:
    - Internal benchmarks (high confidence)
    - Prototype migration (high confidence)
    - Jepsen report (high confidence)
    ↓
Conclusion: Experiential evidence supports adoption for read-heavy workloads;
manufactured concerns about transactions remain unresolved.
Decision: Adopt for analytics workload; keep Postgres for transactional.
```

**Step 3 — Identify remaining consequential gaps by origin**

```
Manufactured gaps (need analysis/simulation):
- "What is the exact transaction isolation behavior?"
- "How does it interact with our ORM?"

Experiential gaps (need testing/deployment):
- "What is write latency under our production load?"
- "How does failover behave in our network topology?"
```

**Step 4 — Select next actions by origin-appropriate method**

```
Gap: "Transaction isolation behavior"
    ↓
Options:
  - Read Jepsen reports (manufactured, 2 hours)
  - Design formal verification (manufactured, 2 weeks)
  - Run chaos test on prototype (experiential, 3 days)
    ↓
INVARIANT-0005 choice: Jepsen reports first (cheapest manufactured knowledge)
```

```
Gap: "Write latency under production load"
    ↓
Options:
  - Model with queuing theory (manufactured, 4 hours)
  - Load test with production-like data (experiential, 2 days)
  - Canary deploy 1% traffic (experiential, 1 week)
    ↓
INVARIANT-0005 choice: Load test first (manufactured model won't capture real contention)
```

## Demonstrates

- Artifacts explicitly tagged with epistemic origin (manufactured vs experiential)
- INVARIANT-0003 Epistemic Integrity prevents treating vendor claims as equivalent to prototype evidence
- Reassessment weighs evidence by origin and confidence
- Remaining gaps categorized by which mode can resolve them
- INVARIANT-0005 Optimization selects origin-appropriate next actions
- Prevents "manufactured knowledge masquerading as experiential certainty"

## Tests

- [ ] All knowledge artifacts tagged with epistemic origin
- [ ] Confidence levels assigned and justified
- [ ] Reassessment separates manufactured vs experiential evidence
- [ ] Conclusions distinguish what manufactured vs experiential evidence supports
- [ ] Remaining gaps categorized by origin-appropriate resolution method
- [ ] Next actions selected using INVARIANT-0005 with origin awareness
- [ ] No manufactured knowledge treated as experiential certainty

## Anti-Patterns This Guards Against

- **Vendor-driven adoption**: Treating marketing benchmarks as proof
- **Opinion-as-fact**: Team preferences given same weight as benchmark data
- **Analysis substitution**: Modeling write latency instead of measuring it
- **Prototype overconfidence**: Assuming prototype success = production readiness

## References

- [threadwright.md §5, 7, 8](../threadwright.md) — Artifact system, decisions/evidence, INVARIANT-0003 Epistemic Integrity
- [HEURISTIC-0005_choose-knowledge-action](../heuristics/HEURISTIC-0005_choose-knowledge-action.md)
- [ASSESSMENT-0008_manufactured-vs-evolved §5, 6](../artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation)
- [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §5](../artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge)