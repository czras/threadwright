# H9 — Generate Broadly, Compress Deliberately

Operationalizes [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately).

> **When generation is cheap, generate broadly; then deliberately compress the result against compactness.**

When the cost of generating alternatives, connections, hypotheses, or candidate material is low, prematurely constraining generation can unnecessarily limit the solution space.

Instead:

1. Generate broadly.
2. Preserve the resulting possibility space long enough to evaluate it.
3. Review the result against compactness.
4. Remove, merge, or simplify elements that do not provide sufficient value.
5. Retain the elements that materially improve the intended outcome.

The goal is not minimalism.

**Compactness is the optimization target.**

Compactness balances the value provided by the generated material against the complexity and cognitive cost it introduces.

## Compactness

As [the principle states](../principles.md#generate-broadly-compress-deliberately): "Compactness is not minimalism. The objective is not the smallest possible result, but the greatest useful value and comprehension for the cognitive cost."

Compactness is not equivalent to having fewer elements.

A compact result may contain many elements when those elements provide meaningful structure or interconnectedness.

A useful approximation is:

> **Maximize useful value, structure, and comprehension while minimizing unnecessary complexity.**

For interconnected knowledge, this means that a relationship should generally be retained when making it explicit materially improves the reader's ability to understand, navigate, or use the knowledge.

A technically relevant connection that provides little reader value may therefore be less desirable than a smaller set of highly useful connections.

## Why Separate Generation and Compression?

Generation and selection have different economics.

When generation is expensive, constraints during generation may be necessary.

When generation is cheap, the cost of preventing unnecessary candidates can exceed the cost of generating and subsequently removing them.

This suggests:

> **Place constraints where they are cheapest to enforce.**

Rather than spending substantial effort preventing every weak candidate from being generated, allow inexpensive generation to explore broadly and move the optimization effort into selection and compression.

```text
Cheap generation
       ↓
Broad exploration
       ↓
Rich candidate set
       ↓
Deliberate evaluation
       ↓
Compression against compactness
       ↓
Useful result
```

## Relation to Interconnectedness

Interconnectedness — one of the [creator's foundational traits](../foundations.md) and a property Threadwright deliberately cultivates — creates a particularly strong case for broad generation.

Relationships between pieces of knowledge may not be obvious in advance. A human or agent may discover useful relationships only when considering the knowledge corpus as a whole.

Therefore, specifying in advance exactly which relationships should exist can prevent useful connections from being discovered.

Broad generation allows latent relationships to surface.

Compression then determines which relationships deserve to become part of the reader-facing structure.

This creates a useful tension:

> **Generate connections broadly; expose connections selectively.**

Too little interconnectedness fragments knowledge.

Too much interconnectedness creates noise.

Compactness is the mechanism for balancing the two.

## Operational Heuristic

When considering whether to constrain generation:

**If generation is cheap and evaluation is comparatively cheap:**
- generate broadly;
- tolerate redundancy;
- allow unexpected alternatives and connections;
- defer detailed optimization;
- compress during review.

**If generation is expensive or dangerous:**
- constrain earlier;
- use prior knowledge to narrow the search;
- avoid generating costly or irreversible candidates unnecessarily.

The heuristic therefore depends on the relative cost of:

- generation;
- evaluation;
- compression;
- consequences of exploring poor candidates.

It is not a universal instruction to generate everything.

## Review Questions

When compressing generated material, ask:

1. Does this element materially contribute to the intended outcome?
2. Does this connection improve understanding or navigation?
3. Does it reveal useful structure that would otherwise remain implicit?
4. Is the information redundant with something already present?
5. Does keeping it increase cognitive load more than it increases value?
6. Can several elements be merged without losing useful meaning?
7. Is the result becoming more interconnected **and** more comprehensible, or merely more interconnected?
8. Would removing this element make the knowledge meaningfully harder to use?

## Emerging Hypothesis

The heuristic suggests a broader pattern for agentic work:

> **As the marginal cost of generation approaches zero, optimization shifts from generation toward selection and compression.**

This may change how knowledge work should be structured.

Rather than requiring the generation process itself to produce a highly polished result, it may be more effective to separate:

**exploration** from **compression**.

This separation can allow agents to exploit their low generation cost while reserving human and higher-reasoning effort for judgment.

This cost-shift hypothesis is itself emerging and should be tested across different domains before being promoted to a stronger methodological claim.

## Related Scenarios

- [Cheap Generation, Expensive Evaluation](../scenarios/cheap-generation-expensive-evaluation.md) — Total cost, irreversible evaluation, expensive generation
- [Engineering Design](../scenarios/engineering-design.md) — Multiple candidate designs and implementations
- [Knowledge Connections](../scenarios/knowledge-connections.md) — Latent relationship discovery
- [Ambiguous Interpretation](../scenarios/ambiguous-interpretation.md) — Premature convergence prevention
- [Over-Compression](../scenarios/over-compression.md) — Compactness as proxy trap

## References

- [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately) — The principle this heuristic operationalizes
- [threadwright.md §6](../threadwright.md#6-consequential-gaps-and-useful-activity) — Cost of learning framework
- [threadwright.md §8 I5](../threadwright.md#i5--optimization) — Optimization invariant
- [Optimize for the Objective](../principles.md#optimize-for-the-objective) — Compactness as optimization target relates to objective/proxy distinction
- [Keep Complexity Proportional to Evidence](../principles.md#keep-complexity-proportional-to-evidence) — Compression against unnecessary complexity
- [Epistemic Integrity](epistemic-integrity.md) — Distinguishing generated hypotheses from established knowledge