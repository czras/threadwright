# Knowledge Connections

**Heuristic:** H9 — Generate Broadly, Compress Deliberately

## Context

A body of knowledge contains concepts, observations, decisions, and artifacts that may relate to one another. Some relationships are obvious, while others may only become visible when the corpus is considered as a whole.

This applies to methodological cross-references, codebase relationships, research literatures, and any domain where the connections between pieces of knowledge are not fully known in advance.

## Generation

Ask an agent to identify potentially useful relationships between the elements of the knowledge base.

Do not prescribe the number or type of relationships to find. Allow the agent to identify:

- supporting relationships;
- causal relationships;
- dependencies;
- contradictions;
- shared concepts;
- evidence relationships;
- derivations;
- alternative interpretations;
- cross-references between artifacts.

## Observation

Broad generation may reveal relationships that were not anticipated during the original construction of the knowledge.

It may also produce:

- redundant relationships;
- technically valid but unhelpful relationships;
- weak associations;
- excessive cross-linking.

The challenge is distinguishing useful latent relationships from noise.

## Compression

Review each relationship against compactness.

Retain relationships that materially improve:

- comprehension;
- navigation;
- context;
- traceability;
- discovery of supporting knowledge.

Remove relationships whose cognitive cost exceeds their value. A technically relevant connection that provides little reader value may be less desirable than a smaller set of highly useful connections.

## Evaluation

Compare the resulting knowledge structure with one where relationships were manually selected during construction.

Evaluate:

- useful relationships discovered;
- navigation;
- comprehension;
- structural clarity;
- cognitive load;
- relationship density.

## Question

> Can broad generation reveal useful latent relationships that would be missed by constraining interconnectedness during construction, while deliberate compression prevents the resulting structure from becoming noisy?

## References

- [H9 — Generate Broadly, Compress Deliberately](../heuristics/generate-broadly-compress-deliberately.md) — The heuristic this scenario tests
- [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately) — The underlying principle
- [threadwright.md §5](../threadwright.md#5-artifact-system) — Artifact relationships
