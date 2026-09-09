# Engineering Design

**Heuristic:** H9 — Generate Broadly, Compress Deliberately

## Context

An implementation task has several plausible designs. The cost of generating candidate designs is low compared with the cost of implementing, testing, and maintaining the resulting system.

This applies to code architecture, API design, data structures, system decomposition, document structure, and other design decisions where multiple structural approaches are viable.

## Generation

Generate multiple candidate designs or implementations.

Candidates may differ in:

- architecture;
- algorithms;
- abstractions;
- dependency choices;
- data structures;
- interfaces;
- document structure and explanation approach;
- implementation complexity.

Do not require the generation phase to converge immediately on one solution. Allow alternative architectures, unconventional approaches, and different levels of abstraction to surface.

## Observation

The candidate set may contain:

- genuinely different approaches;
- equivalent implementations;
- over-engineered solutions;
- simple solutions that are surprisingly effective;
- unexpected approaches that expose previously unnoticed trade-offs;
- complementary formulations that can be combined.

## Compression

Evaluate candidates against:

- correctness;
- requirements;
- complexity;
- maintainability;
- performance;
- dependencies;
- implementation cost;
- reversibility;
- operational risk;
- for communication artifacts: comprehension, reader value, structural clarity.

Discard or merge candidates that do not provide sufficient additional value.

Retain the smallest useful set of genuinely distinct alternatives. Several candidates may be merged without losing useful meaning.

## Evaluation

Compare with directly asking for the simplest or most likely implementation.

Evaluate:

- quality of the selected solution;
- useful alternatives discovered during generation;
- review effort;
- implementation effort;
- defects;
- maintainability;
- for writing: clarity, completeness, revision effort.

## Question

> When design generation is cheap, does generating multiple candidate implementations before selecting one produce better outcomes than constraining generation upfront?

## References

- [H9 — Generate Broadly, Compress Deliberately](../heuristics/generate-broadly-compress-deliberately.md) — The heuristic this scenario tests
- [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately) — The underlying principle
- [threadwright.md §6](../threadwright.md#6-consequential-gaps-and-useful-activity) — Cost of learning framework
