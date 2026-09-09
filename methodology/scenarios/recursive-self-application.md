# Scenario — Recursive Self-Application

## Situation

A team has been applying Threadwright for 3 months across multiple Changes. They notice patterns in their practice and want to evolve their Threadwright usage.

## Application

**Phase 1 — Apply Threadwright (generates experience)**

The team applies Threadwright to several Changes:
- Change A: Greenfield product exploration
- Change B: Legacy system migration
- Change C: Performance optimization

During application, they capture experiences as artifacts:
```
Experience artifacts:
- "Consequential gap identification worked well for Change A"
- "Dynamic boundary heuristic unclear — team defaulted to 'always prototype'"
- "I5 Optimization invariant rarely used explicitly"
- "Messy input decomposition saved 2 weeks on Change C"
- "Artifact relationships became cluttered; hard to find relevant gaps"
```

**Phase 2 — Identify consequential gaps in Threadwright practice**

```
Gap 1: "Team doesn't consistently apply dynamic boundary heuristic"
Gap 2: "I5 Optimization not operationalized — no shared mental model"
Gap 3: "Artifact clutter reduces reassessment effectiveness"
```

**Phase 3 — Select knowledge-generating actions for methodology evolution**

For Gap 1:
```
Options:
- Add explicit boundary check to reassessment template (manufactured)
- Run workshop with boundary shift examples (experiential)
- Create decision log template forcing manufactured/experiential choice (manufactured)
    ↓
I5 choice: Add boundary check to template (lowest cost, directly addresses gap)
```

For Gap 2:
```
Options:
- Write internal guide with worked examples (manufactured)
- Pair on next 3 Changes using I5 explicitly (experiential)
- Build simple calculator tool (manufactured + tooling)
    ↓
I5 choice: Pair on next 3 Changes (experiential learning sticks better than docs)
```

For Gap 3:
```
Options:
- Prune relationships manually (experiential)
- Add "gap relevance" tag to relationships (manufactured + tooling)
- Archive completed Changes (manufactured)
    ↓
I5 choice: Add "gap relevance" tag + archive (manufactured, scalable)
```

**Phase 4 — Execute, capture evidence, update Threadwright practice**

```
Action: Implement template change, pairing, tagging
    ↓
Evidence (after 2 Changes):
- Boundary shifts now explicit in 80% of reassessments
- I5 language used naturally in standups
- Artifact queries 3x faster
    ↓
Threadwright practice updated:
- Reassessment template now includes "Boundary check: manufactured or experiential next?"
- I5 Optimization added to team's working agreements
- Artifact hygiene: "gap relevance" tag required on new relationships
```

**Phase 5 — Repeat**

The updated practice is now the "current Threadwright" for the team. New experiences will trigger the next evolution cycle.

## Demonstrates

- Threadwright is **both instrument and object** of knowledge evolution
- The same methodology (gaps → optimization → action → evidence → reassess) applies to improving Threadwright itself
- Experiences from application become structured knowledge about the methodology
- I5 Optimization used to choose *how to improve the methodology*
- Changes to practice are treated as Changes with their own gaps, actions, evidence
- The recursive loop is explicit and intentional

## Tests

- [ ] Experiences from Threadwright application captured as artifacts
- [ ] Gaps in Threadwright practice identified (not just product gaps)
- [ ] I5 Optimization used to select methodology improvement actions
- [ ] Improvements implemented as Changes with their own tracking
- [ ] Evidence from improvements evaluated
- [ ] Threadwright practice explicitly updated based on evidence
- [ ] Cycle documented: apply → experience → learn → evolve → apply

## Meta-Test: Can Threadwright Improve Itself?

This scenario is itself a test of the recursive property. If the team can successfully run this scenario, it demonstrates:
- Threadwright's concepts apply to methodology evolution
- The optimization framing works for meta-decisions
- The heuristics are usable for self-improvement
- The artifact system supports tracking methodology changes

## References

- [threadwright.md §11](../threadwright.md) — Recursive self-application
- [reassess.md](../heuristics/reassess.md) — Reassessment drives evolution
- [ASSESSMENT-0008 §11](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#11-threadwrights-recursive-property)
- [ASSESSMENT-0009 §14](artifacts/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#14-recursive-self-application)
- [ASSESSMENT-0008 §13](artifacts/ASSESSMENT-0008_manufactured-vs-evolved.md#13-recursive-learning-about-learning)