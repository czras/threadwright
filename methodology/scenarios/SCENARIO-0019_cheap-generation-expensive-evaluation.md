# SCENARIO-0019 — Cheap Generation, Expensive Evaluation

**Heuristic:** [HEURISTIC-0009 — Generate Broadly, Compress Deliberately](../heuristics/HEURISTIC-0009_generate-broadly-compress-deliberately.md)

## Context

An agent can generate a very large number of candidates at negligible cost.

However, evaluating each candidate requires substantial expert reasoning. The bottleneck is not generation but evaluation, compression, and selection.

Examples include:

- reviewing thousands of technical designs;
- manually validating generated hypotheses;
- expert assessment of complex alternatives;
- testing candidates against expensive datasets.

## Generation

Generate broadly enough to explore the relevant solution space.

Do not require the generation phase to converge. Allow redundancy, unexpected alternatives, and weak candidates to coexist with strong ones.

## Observation

Cheap generation does not make unlimited generation optimal.

The evaluation and compression stages may become the actual bottleneck. A large candidate set can overwhelm expert judgment, making the total cost of the generate-evaluate-compress cycle higher than a more constrained approach.

## Compression

Before expensive expert evaluation, reduce the candidate set where possible:

- cluster equivalent candidates;
- deduplicate;
- screen using inexpensive criteria;
- rank by cheap proxies;
- evaluate hierarchically (screen broadly, evaluate deeply only for survivors).

## Evaluation

Compare different generation widths against total cost and resulting knowledge.

Consider:

- generation cost;
- screening cost;
- expert evaluation cost;
- compression cost;
- knowledge gained;
- quality of final selection.

## Question

> Does cheap generation still justify broad exploration when evaluation is expensive?

## Boundary Conditions

### When generation itself is expensive

The heuristic depends on the relative cost of generation, evaluation, and compression. When generation is expensive — requiring substantial resources, scarce expert time, or significant infrastructure — the optimal balance shifts toward earlier constraint.

Cheap generation is a **condition** of the heuristic, not an incidental detail. When that condition does not hold, the heuristic adapts: use prior knowledge to narrow the search, avoid generating costly candidates unnecessarily, and constrain earlier.

> **Place constraints where they are cheapest to enforce.**

### When evaluation is irreversible or dangerous

Some candidate actions have significant consequences if actually executed. The distinction between **generating a candidate** and **executing a candidate** becomes important.

Broad generation can be explored cognitively or computationally while exposing reality only to a small, carefully selected subset. Apply stronger selection before irreversible action, considering:

- consequence severity;
- reversibility;
- safety;
- ethical constraints.

> **Where generation is cheap, preserve exploration; apply stronger constraints before costly or irreversible evaluation.**

## References

- [HEURISTIC-0009_generate-broadly-compress-deliberately](../heuristics/HEURISTIC-0009_generate-broadly-compress-deliberately.md) — The heuristic this scenario tests
- [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately) — The underlying principle
- [threadwright.md §6](../threadwright.md#6-consequential-gaps-and-useful-activity) — Cost of learning framework