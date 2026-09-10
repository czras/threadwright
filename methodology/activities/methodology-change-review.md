# Methodology Change Review

## Purpose

Review a change to the Threadwright methodology and determine whether the resulting methodology remains coherent, useful, and consistent with its principles.

The activity exists to detect unintended consequences of methodological change, including conceptual inconsistency, unnecessary complexity, broken relationships, and loss of useful knowledge.

This activity is the operationalization of [Reassess After Change](../principles.md#reassess-after-change) for changes to the methodology itself, and a concrete instance of Threadwright's [recursive self-application](../threadwright.md#recursive-self-application): the methodology reviewing its own evolution.

## Inputs

The activity operates on a committed methodology change.

The commit provides:

- the change itself through its diff;
- the immediate context through its commit message;
- references to related artifacts where provided.

Referenced artifacts provide the evidence, reasoning, provenance, and prior state necessary to understand the change.

The reviewer should consider the resulting methodology as a whole rather than limiting the review to changed files.

## Activity

### 1. Establish the Review Scope

Determine precisely what evidence is in scope before evaluating the methodology.

- Identify the current branch and its target/main branch.
- Establish the complete set of **committed changes on the current branch relative to main**.
- Treat the complete branch delta as the review subject, rather than only the latest commit.
- Explicitly identify uncommitted changes and exclude them from the review.
- Verify that the resulting evidence set matches the requested review scope before proceeding.

Do not infer that the latest commit represents the complete change under review.

### 2. Understand the Change

Determine:

- what changed;
- why it changed;
- what problem, gap, or evidence motivated the change;
- what methodological knowledge the change introduces, modifies, removes, or reorganizes.

Do not assume that the implementation of a change fully represents its intended meaning. Use the related artifacts and commit context to reconstruct that meaning.

Do not evaluate individual files in isolation. Establish the intended conceptual change and its relationship to the existing methodology.

### 3. Identify the Impact

Determine which parts of the methodology are affected, including:

- concepts;
- invariants;
- principles;
- heuristics;
- activities;
- scenarios;
- relationships;
- terminology;
- reading and navigation paths;
- artifact structure.

Consider both direct and indirect effects.

### 4. Review Methodological Coherence

Determine whether the resulting methodology remains internally coherent.

Look for:

- contradictions;
- inconsistent terminology;
- overlapping or ambiguous concepts;
- broken distinctions;
- principles that conflict with other methodological knowledge;
- artifacts whose meaning is no longer consistent with the methodology;
- relationships that have become incorrect or misleading.

### 5. Review Epistemic Integrity

Apply [INVARIANT-0003 — Epistemic Integrity](../threadwright.md#invarient-0003--epistemic-integrity) and [HEURISTIC-0008 — Epistemic Integrity](../heuristics/HEURISTIC-0008_epistemic-integrity.md) to the change itself. Determine whether it preserves appropriate distinctions between:

- observation and interpretation;
- evidence and conclusion;
- hypothesis and established knowledge;
- proposal and decision;
- implementation and outcome;
- confidence and correctness.

Check whether generated, inferred, or assumed knowledge has unintentionally acquired undue authority.

Preserve provenance where it materially contributes to understanding.

### 6. Review Interconnectedness

Determine which relationships created or affected by the change are useful.

Preserve relationships that materially improve:

- understanding;
- context;
- evidence;
- navigation;
- application.

Remove relationships that merely demonstrate relatedness or create cognitive noise.

Do not optimize for the number of relationships exposed to the reader.

Consider the reader's journey through the methodology, not merely whether the relevant files exist.

### 7. Review Cognitive Load and Compactness

Review the resulting methodology from the reader's perspective.

Look for:

- unnecessary duplication;
- excessive cross-references;
- repeated explanations;
- unnecessary terminology;
- excessive nesting;
- long lists of related artifacts;
- references that interrupt the main argument;
- concepts introduced before they are needed;
- structures that require unnecessary repository archaeology.

Compress deliberately where possible, per [Generate Broadly, Compress Deliberately](../principles.md#generate-broadly-compress-deliberately).

Compactness does not mean minimizing the amount of information. Preserve useful knowledge, relationships, and context when removing them would reduce comprehension or utility.

### 8. Review Consequences

Consider consequences that are not immediately visible in the changed files.

Ask:

- What becomes possible because of this change?
- What becomes harder?
- What assumptions does it introduce?
- What future changes does it make easier or harder?
- Does it create unnecessary complexity?
- Does it solve a demonstrated problem or a hypothetical one?
- Does it create a new proxy that could be mistaken for the intended objective?
- Does it preserve the implementation-agnostic nature of Threadwright?

Do not introduce solutions for hypothetical future complexity without evidence that the complexity exists.

### 9. Review Boundaries

Verify that the change preserves methodological boundaries.

In particular:

- methodology remains distinct from its applications;
- methodological knowledge remains distinct from implementation choices;
- public material does not reference, expose, or imply private material;
- implementation mechanisms do not become accidental methodological requirements.

### 10. Compress and Integrate

Where the review identifies unnecessary complexity, improve the resulting methodology rather than merely reporting the problem.

Integration may include:

- consolidating duplicated explanations;
- removing unnecessary references;
- relocating knowledge to a more appropriate artifact;
- simplifying terminology;
- restructuring relationships;
- preserving only the connections useful to the reader.

Do not compress mechanically. The objective is a coherent and useful methodology, not a smaller repository.

### 11. Reassess the Result

After review and any resulting changes, reassess the methodology as a whole.

Determine whether the resulting state is:

- more coherent;
- conceptually sound;
- epistemically precise;
- appropriately interconnected;
- sufficiently compact;
- understandable to its intended reader;
- consistent with Threadwright's principles.

## Report

Produce a concise report containing:

### Change Understanding

What the reviewed change introduces and why it matters.

### Findings

The significant issues, strengths, relationships, and consequences discovered.

### Changes Made

Corrections made during the review and their rationale.

### Relationships

Important relationships between the new material and existing methodology.

### Unresolved Questions

Questions for which the available evidence does not yet justify a methodological decision.

### Assessment

An overall assessment of the change and whether it is ready to proceed.

The assessment should distinguish between:

- issues requiring correction;
- observations worth monitoring;
- unresolved questions that do not currently block the change.

## Scope Boundary

The review must distinguish between the evidence being reviewed and other work present in the repository.

Committed changes within the established branch delta are in scope.

Uncommitted changes are out of scope unless explicitly included in the review request.

The reviewer must establish and verify this boundary before reasoning about the change.

## Completion Criteria

The activity is complete when:

1. the change and its intended purpose are understood;
2. affected methodological knowledge has been considered;
3. the resulting methodology has been reviewed as a whole;
4. consequential inconsistencies or unintended consequences have been addressed or explicitly reported;
5. useful relationships have been preserved;
6. unnecessary cognitive complexity has been compressed where appropriate;
7. epistemic and public/private boundaries remain intact;
8. unresolved consequential uncertainty is explicitly identified;
9. the resulting state has been reassessed.

The activity does not require that every uncertainty be resolved.

Its purpose is to determine whether the methodology has evolved into a state that is sufficiently coherent and useful to proceed.

## Implementation Independence

This activity defines **what review is to accomplish**, not how the review is performed.

It may be implemented by:

- a human using a review manual;
- an agent using a skill;
- a software system using automated checks;
- a combination of human and automated activities;
- another implementation appropriate to the context.

An implementation may introduce additional checks or procedures, provided they do not change the purpose or completion criteria of the activity.
