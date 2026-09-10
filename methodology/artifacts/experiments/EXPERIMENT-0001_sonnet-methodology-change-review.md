# EXPERIMENT-0001 — Sonnet Methodology Change Review

## Purpose

Evaluate Claude Sonnet 5 performing a Threadwright Methodology Change Review against the current methodology repository, while recording the actual cost and resource consumption of an agentic review.

This experiment establishes an empirical baseline for:

- the capability of Sonnet to perform a whole-methodology review;
- the ability of the review prompt to correctly establish its scope;
- the usefulness of the resulting review;
- the cost of performing such a review;
- the relationship between repository size, token consumption, and review cost.

The experiment is intentionally observational. It does not establish general conclusions about model selection or optimal workflow design.

## Experiment Context

The review was performed after a methodology change represented by commit:

`9c11d34`

The intended review scope was **the current Threadwright methodology branch relative to the main branch**, rather than only the changes introduced by the latest commit.

The repository contained uncommitted changes under `tmp/`. The prompt explicitly instructed the reviewer to omit `tmp/` from the review completely.

The review activity was itself part of the methodology change being reviewed.

At the time of the review, additional methodology changes were already being developed under `tmp/`, including:

- scenario ID-ing;
- scenario publishing workflow/activity refinement;
- refinement of the `Generate Broadly, Compress Deliberately` heuristic in relation to scenarios.

These changes were deliberately excluded from the review because they were not committed.

## Model and Execution

**Model:** Claude Sonnet 5
**Provider:** Anthropic
**Agent:** OpenCode 1.18.25
**Execution:** OpenCode agentic review
**Prompt caching:** Not enabled according to the Anthropic dashboard

## Input

The complete review prompt is preserved with this experiment.

The prompt instructed the model to:

1. understand the methodology change;
2. review the resulting methodology as a coherent whole;
3. review methodological coherence;
4. review epistemic integrity;
5. review interconnectedness;
6. review cognitive load and compactness;
7. review consequences;
8. review methodology boundaries;
9. integrate and compress where appropriate;
10. reassess the resulting methodology;
11. provide a structured review report.

The prompt also explicitly stated:

> review the commited changes versus the main branch, tmp/ has uncommited changes so omit them from the review completely

## Result

The model produced a structured Methodology Change Review and made changes to the repository.

It identified several coherence and integration issues, including:

- orphaned methodology documents;
- an epistemic-integrity problem in the formulation of a principle;
- duplication between principles and existing methodology;
- terminology ambiguity around `Activity` and `activities/`;
- an undocumented public/private boundary;
- a minor wording inconsistency in `conventions/git.md`.

It then modified four files and reported:

> Net diff: 4 files, +25/-24 lines — integration/compression, not restructuring.

The review concluded that the methodology change was coherent after the corrections and considered it ready to proceed, subject to a human decision concerning the public/private material boundary.

The complete model response is preserved with this experiment.

## Review Scope

A significant execution issue was discovered.

The requested review scope was the **committed branch state relative to main**, while the model's response appears to have treated the review primarily as a review of the **latest commit** (`9c11d34`).

This is visible immediately in the report heading:

> Methodology Change Review — methodology: add principles and review activity (9c11d34)

and in the framing:

> The commit under review adds two new top-level methodology documents

The resulting review therefore appears not to have systematically reviewed the complete accumulated branch diff against main as explicitly requested.

### Significance

This is consequential because the two scopes represent different activities.

A single-commit review asks:

> Is this change coherent with what already exists?

A branch-vs-main review asks:

> Is the resulting methodology on this branch coherent relative to main, considering all committed changes on the branch?

The latter can reveal interactions and accumulated inconsistencies that are invisible when reviewing only the final commit.

The review therefore **cannot be treated as evidence that the entire branch was successfully reviewed against main**.

The result remains valuable as a review of the latest methodology change and its surrounding context.

## Scope Boundary and `tmp/`

An important positive observation emerged when considering the review against the repository state.

The reviewer did not incorporate the already-developed but uncommitted work in `tmp/` into its findings.

This is significant because the excluded material represented real emerging methodology work:

- scenario ID-ing;
- scenario publishing and activity refinement;
- further development of `Generate Broadly, Compress Deliberately`.

The model therefore did not incorrectly treat future, uncommitted methodology as established repository knowledge.

It also recognized that the newly committed review activity existed while related future work did not yet exist in the committed methodology.

This demonstrates useful preservation of the distinction between:

- committed methodology;
- emerging work;
- future intent.

The overall scope execution was nevertheless incorrect because the requested **branch-vs-main** boundary was not reliably followed.

The evidence therefore suggests a nuanced result:

> The model failed to establish the requested review scope correctly, but within the material it did review, it appears not to have silently promoted excluded future work into established methodology.

## Unauthorized Repository Modification

The prompt requested a review, but the model **modified the repository directly**.

This was not merely incidental output generation. It made concrete changes to four files.

The changes were:

- small;
- local;
- relevant to the findings;
- apparently useful;
- consistent with the requested integration/compression behavior.

Therefore, the modifications should not be dismissed as random agent behavior.

However, they were still made without an explicit instruction from the user to permit repository modification.

### Methodology ambiguity

There is an important ambiguity in the activity definition itself.

The activity is framed as a **review**, which naturally suggests an advisory activity.

However, its step 8 explicitly states:

> Where the review identifies clear unnecessary complexity, duplication, misplaced knowledge, or misleading relationships, make the appropriate corrections directly.

The model may therefore have interpreted the activity definition as authorizing direct modification, despite the higher-level request framing the operation as a review.

This means the behavior is simultaneously:

- an instruction-following failure at the interaction level;
- potentially a reasonable interpretation of the activity definition itself.

This should be treated as evidence that the distinction between **reviewing** and **integrating review corrections** may need to be made more explicit in the methodology.

### Quality of the unauthorized changes

The changes themselves were useful.

This is important evidence for future workflow design, but it does not make the instruction-following failure acceptable.

The experiment therefore establishes two separate observations:

1. **Agent autonomy exceeded the requested operating mode.**
2. **The autonomous corrections had positive apparent value.**

Whether direct correction should be part of the activity is a future methodological/workflow decision.

## Findings

### 1. Orphaned files

The reviewer found that neither new methodology document was reachable from the main methodology navigation.

This was a strong finding.

The issue was not merely file organization. The new knowledge had been introduced without being integrated into the documented journey through the methodology.

The resulting correction was small and high-value:

- `methodology/README.md` was updated to register `principles.md` and `activities/`;
- the conceptual relationship diagram was updated accordingly.

### 2. Epistemic overstatement

The reviewer identified that `Optimize for the Objective` restated material from [ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization](../assessments/ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization.md) as a principle even though the assessment explicitly described the idea as an emerging hypothesis.

This was a particularly strong finding because the newly introduced methodology itself requires preservation of epistemic boundaries.

The reviewer therefore effectively applied the new epistemic principle to the new principle set itself.

The correction added provenance and explicitly retained the provisional status of the underlying hypothesis.

### 3. Conceptual duplication

The reviewer identified several overlaps between new principles and existing methodology, including:

- `Address Consequential Gaps` ↔ [HEURISTIC-0001](../../heuristics/HEURISTIC-0001_address-consequential-gaps.md);
- `Preserve Epistemic Boundaries` ↔ [INVARIANT-0003](../../invariants/INVARIANT-0003_epistemic-integrity.md) and [HEURISTIC-0008](../../heuristics/HEURISTIC-0008_epistemic-integrity.md);
- `Move Toward Reality...` ↔ existing forward-deployment material and [HEURISTIC-0006](../../heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md);
- `Let Experience Change the Method` / `Reassess After Change` ↔ recursive self-application, [INVARIANT-0004](../../invariants/INVARIANT-0004_feedback.md), and [HEURISTIC-0004](../../heuristics/HEURISTIC-0004_reassess.md).

It also identified two principles as substantially overlapping:

- `Prefer Existing Abstractions Before Inventing New Ones`;
- `Keep Complexity Proportional to Evidence`.

Rather than deleting one idea, it merged the two while preserving the underlying content.

This is a strong example of **compression without impoverishment**.

### 4. Relationship-oriented reasoning

The strongest findings were not isolated file-level observations.

The model repeatedly reasoned through:

**new concept → existing concept → relationship → cognitive consequence → correction**

This is particularly aligned with the Threadwright methodology.

For example, it recognized that silent duplication between a principle and an existing heuristic is problematic not simply because words are repeated, but because the reader may not know whether the two concepts are intended to be distinct.

This suggests the model was capable of reasoning about the methodology as a knowledge system rather than merely performing conventional document review.

### 5. Terminology ambiguity

The reviewer identified ambiguity between:

- `Activity` as a Threadwright concept representing an instance of work;
- `activities/` as a repository directory containing reusable activity definitions.

The distinction was real and the clarification was inexpensive.

However, classifying this as a **required correction** may have been stronger than the evidence warranted.

This illustrates a broader observation:

> Detecting a possible issue and establishing that it requires immediate correction are different judgments.

The model's ability to classify findings by severity therefore deserves further examination.

### 6. Public/private boundary

The reviewer identified that the new activity checks whether public material references, exposes, or implies private material, while the repository does not yet contain a formal convention defining the boundary.

This is a useful observation.

The model correctly **did not invent a missing convention** simply to make the review appear complete.

It instead left the question unresolved because deciding what constitutes permissible disclosure is a governance decision.

This demonstrates useful restraint around undocumented assumptions.

### 7. Positive boundary observation

The reviewer also observed that existing public material avoided directly exposing the private `product/` material.

This is useful supporting evidence, although less strong than a concrete violation because establishing the absence of boundary violations comprehensively is more difficult than identifying one.

## Changes Made

The model reported the following changes:

- `methodology/README.md`
  - registered `principles.md`;
  - registered `activities/`;
  - clarified the `Activity` / `activities/` distinction;
  - updated the conceptual relationship diagram.

- `methodology/principles.md`
  - added cross-references to overlapping existing concepts;
  - merged two overlapping principles;
  - added provenance and an explicit provisional-status caveat to `Optimize for the Objective`.

- `methodology/activities/methodology-change-review.md`
  - linked the activity to `Reassess After Change`;
  - connected it to recursive self-application;
  - linked relevant steps to existing epistemic and compactness concepts.

- `conventions/git.md`
  - corrected a minor singular/plural wording inconsistency.

The model characterized the resulting change as:

> Net diff: 4 files, +25/-24 lines — integration/compression, not restructuring.

The changes appear appropriately conservative and did not introduce speculative repository architecture.

## Relationships

### Added or strengthened

- [`principles.md`](../../principles.md) ↔ [`threadwright.md`](../../threadwright.md)
- [`principles.md`](../../principles.md) ↔ relevant heuristics
- [`principles.md`](../../principles.md) ↔ `methodology-change-review.md`
- [`principles.md`](../../principles.md) → [ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization](../assessments/ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization.md)
- `methodology/README.md` → [`principles.md`](../../principles.md)
- `methodology/README.md` → `activities/`

### Compressed

Two overlapping principles were combined rather than retained as separate concepts.

This reduced conceptual noise while preserving the underlying ideas.

### Deliberately not added

No relationship was added from the review activity to a public/private boundary convention because no such convention currently exists.

This restraint preserved epistemic accuracy rather than manufacturing structure.

## Cost and Resource Consumption

### Anthropic dashboard

| Metric | Value |
|---|---:|
| Total input tokens | 10,754,203 |
| Total output tokens | 38,414 |
| Total tokens | 10,792,617 |
| Organization credits remaining | $1.80 |
| Spend this month | $3.21 |
| Prompt caching | Not enabled |
| Tokens reused | 0 |

The experiment started with approximately **$5.00** of available credits and ended with approximately **$1.80** remaining.

Observed experiment cost:

**$3.21**

Approximately **64% of the initial experimental budget** was consumed by this single review.

The dashboard reports no prompt-cache reuse.

Prompt-caching behavior is deliberately **deferred from this experiment** and should be investigated separately.

## Cost Observations

The most striking resource observation is the ratio between input and output:

- approximately 10.75 million input tokens;
- approximately 38 thousand output tokens.

The final review is comparatively small while the agent consumed a very large amount of input context.

This suggests that repository-wide agentic review can become expensive primarily through context processing and repeated interaction rather than final response generation.

This remains preliminary. The experiment does not establish:

- how much input consisted of repository content;
- how much was repeated context;
- how much came from tool interaction;
- how much context was unnecessarily reprocessed;
- whether equivalent review quality could be achieved more cheaply.

Those questions require further experiments.

## What Worked

Several aspects of the experiment worked particularly well.

### Methodological reasoning

The model identified non-obvious coherence issues rather than merely commenting on changed files.

### Epistemic scrutiny

The identification of the provisional status of [ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization](../assessments/ASSESSMENT-0010_objective-and-proxy-in-knowledge-optimization.md) was strongly aligned with the requested epistemic-integrity criteria.

### Recursive self-application

The reviewer identified a problem in the newly introduced principles using the epistemic constraints introduced by those same principles.

This provides an early example of the methodology being useful for examining its own evolution.

### Integration and compression

The reviewer did not simply report duplication. It compressed overlapping concepts and established explicit relationships to existing methodology.

### Restraint

The model avoided inventing a public/private convention and avoided prematurely creating an index for the new `activities/` directory.

### Preservation of emerging intent boundaries

Despite the overall scope problem, the model did not treat the uncommitted scenario/publishing/heuristic work in `tmp/` as established methodology.

## What Did Not Work

### 1. Review scope was not reliably enforced

The most important execution failure was the apparent reduction of a branch-vs-main review to the latest commit.

### 2. Review mode was not reliably enforced

The model modified the repository even though the interaction requested a review.

The activity definition itself contains language that may reasonably have been interpreted as authorizing direct corrections, so this may expose ambiguity in the methodology rather than being purely an agent failure.

### 3. Finding severity may have been too assertive

Some observations were classified as required corrections even where the evidence appeared to support a weaker classification such as "worth monitoring."

This suggests future evaluation should distinguish:

- finding detection;
- finding significance;
- recommended action;
- urgency.

These are separate reasoning tasks.

## Deeper Observations

The experiment provides evidence that the model is capable of useful Threadwright-shaped reasoning.

Its strongest contributions were relationship-oriented rather than file-oriented:

> new concept → existing concept → relationship → cognitive consequence → correction

The model also demonstrated useful epistemic restraint around the boundary between committed methodology and emerging work.

At the same time, the experiment demonstrates that a capable model can produce a convincing and useful review while failing a consequential execution constraint.

This is particularly important because the failure was not obvious from the quality of the resulting prose.

The review **looked successful**.

Therefore, review quality alone is insufficient evidence that the requested workflow was executed correctly.

This is a strong argument for making consequential workflow boundaries independently verifiable.

## Unresolved Questions

1. Why did the model interpret the requested review scope as the latest commit rather than the branch diff against main?
2. Should review scope be supplied to the agent as explicit structured execution metadata rather than only prompt text?
3. Should the review workflow provide an explicit base commit, head commit, generated diff, and excluded paths?
4. Should the Methodology Change Review activity be advisory, or explicitly authorized to modify the methodology?
5. If direct modification is authorized, should human approval be required before changes are applied?
6. How should findings be distinguished between detection, significance, and required action?
7. How much of the 10.75M input tokens resulted from repository context, repeated context, and tool interaction?
8. Can equivalent review quality be achieved with substantially lower input-token consumption?
9. What is the appropriate model for this class of methodology review?
10. Should whole-branch methodology reviews use a different workflow from ordinary methodology-change reviews?
11. Why did the Anthropic dashboard report no prompt-cache reuse?
12. What cost controls should exist for future agentic reviews?

The prompt-caching question is deliberately separated from the primary conclusions of this experiment.

## Assessment

This was a **useful but expensive first experiment**.

It successfully demonstrated that Sonnet can perform meaningful methodological analysis and make targeted integration/compression changes. Several findings were substantive, and some corrections were directly useful.

The experiment also exposed two important workflow limitations:

1. **the requested branch-vs-main scope was not reliably maintained;**
2. **the agent modified the repository despite the review being presented as a review operation.**

The second issue is complicated by an ambiguity in the activity definition itself, which explicitly instructs the reviewer to make appropriate corrections directly. This should therefore be treated as evidence requiring methodological clarification rather than simply as model misbehavior.

The cost was **$3.21**, consuming approximately 64% of the initial $5 experimental budget.

The most valuable result is therefore not simply:

> Sonnet can review Threadwright.

It is:

> A high-capability agent can produce a convincing, relationship-aware methodology review and useful corrections while still failing an important scope constraint and consuming several dollars of inference budget.

The experiment also provides positive evidence that the methodology can support meaningful recursive self-application: the reviewer detected epistemic and structural problems in newly introduced methodology using principles represented by that same methodology.

The result is **useful but scope-limited evidence**, not validation of the entire branch.

**Experiment status:** completed
**Result:** useful, scope-limited
**Cost:** $3.21
**Primary lesson:** consequential execution scope should be explicit and independently verifiable
**Secondary lesson:** review and autonomous integration need an explicit boundary
**Follow-up:** preserve evidence and design the next experiment around scope-controlled review and controlled modification
