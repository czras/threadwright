# Scenario — Long-Running Product

## Situation

A mature product contains thousands of artifacts, hundreds of Changes, years of decisions, multiple teams, architecture history, production evidence, technical debt, and regulatory constraints.

A new Change is introduced: add support for a new payment provider.

## Application

The relevant current state may include payment requirements, applicable constraints, existing architecture, security decisions, provider dependencies, production evidence, and affected Changes.

The team identifies the relevant connected state rather than reasoning manually over the entire artifact system.

```text
Change
   ↓
Relevant current state
   ↓
Consequential gaps
   ↓
Activities
   ↓
Updated artifacts
   ↓
Reassess
```

## Demonstrates

The methodology scales conceptually without a new lifecycle. Efficient discovery, retrieval, impact analysis, summarization, and graph traversal are implementation problems.
