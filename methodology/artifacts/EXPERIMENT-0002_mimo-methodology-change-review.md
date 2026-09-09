# Experiment 0002 — MiMo Methodology Change Review

## Purpose

Evaluate the effectiveness of the Threadwright `Methodology Change Review` activity and its revised review prompt by having an independent agent review a new set of committed methodology changes.

This experiment follows Experiment 0001, which used Claude Sonnet for the same general task. The present experiment deliberately uses a fresh session and a lower-cost model to gather an independent data point without carrying forward the previous review's conversational context.

The experiment also tests two changes made in response to Experiment 0001:

- the activity now explicitly establishes and verifies the complete review scope before substantive reasoning;
- the prompt explicitly defines the review subject as the entire committed current branch delta relative to main, rather than leaving "committed changes" open to interpretation.

## Experiment Context

The reviewed branch introduces:

1. A new `Generate Broadly, Compress Deliberately` heuristic and 12 supporting scenarios.
2. A substantial rewrite of `methodology-change-review.md`, including the new scope-establishment step and a more compact activity structure.

The branch was reviewed before proceeding with the next planned methodology changes.

Uncommitted work under `tmp/` existed during the experiment and was explicitly excluded from the review.

## Experimental Conditions

### Model

MiMo V2.5 Free, provided through OpenCode Zen.

### Session

Fresh OpenCode session.

The session contained no prior conversational context from Experiment 0001 or the subsequent discussion of its findings.

### Prompt

The revised Methodology Change Review prompt.

The substantive review criteria were kept essentially unchanged from Experiment 0001. The principal prompt change was an explicit definition of the review scope:

> The review subject is the entire committed change set of the current branch relative to its main branch.

The prompt also required the agent to establish and verify that scope before beginning the substantive review.

### Activity

The revised `methodology/activities/methodology-change-review.md`.

The significant change relevant to this experiment was the introduction of an explicit **Establish the review scope** step requiring the reviewer to:

- identify the current branch;
- identify the target/main branch;
- establish the branch comparison/merge-base;
- determine the complete committed change set;
- exclude uncommitted changes;
- verify the resulting evidence set before proceeding.

### Repository State

The review covered the complete committed branch delta relative to main.

Uncommitted changes, including `tmp/`, were out of scope.

### Execution Measurements

- Context: **64,904 tokens**
- Context utilization: **32%**
- Duration: **5m 41s**
- Cost: **$0.00**
- Tool usage: **not captured; OpenCode did not provide convenient execution-level tool usage telemetry**

## Result

MiMo produced a structured methodology review and made **no repository changes**.

The review assessed the branch as **not ready to proceed as-is**.

It identified four primary integration problems:

1. **Epistemic status mismatch**
   - The established `Generate Broadly, Compress Deliberately` principle is elaborated by a heuristic marked as emerging.
   - MiMo identified the tension between the status of the principle and the status of its operational elaboration.

2. **H9 numbering inconsistency**
   - Ten scenarios referenced the heuristic as H9 while two did not.
   - MiMo also identified the absence of H5–H8 and the lack of an index entry.

3. **Missing relationships and navigation**
   - The heuristic did not explicitly link upward to its principle.
   - The heuristic and scenarios were not integrated into the relevant README/index structures.
   - Scenario references to related methodology artifacts were missing.

4. **Competing conceptual formulations**
   - `compactness` and `interconnectedness` were introduced or defined without sufficiently connecting them to existing formulations.
   - MiMo identified this as a potential integration problem rather than treating the new definitions as isolated concepts.

Additional findings included:

- redundancy among the 12 scenarios;
- the possibility that the rewritten methodology-change-review activity had become too sparse;
- loss of completion criteria and implementation-independence guidance;
- ambiguity between "integrate and compress" and "do not invent missing rules";
- an implicit rather than explicit principle–heuristic relationship.

MiMo regarded the underlying knowledge as useful and characterized the problems primarily as **integration failures rather than conceptual failures**.

## Scope Verification Result

The revised scope instruction appears to have worked.

MiMo reviewed both major areas of the committed branch:

- the new heuristic and its scenarios;
- the rewritten `methodology-change-review.md`.

This is significant because Experiment 0001 exposed a scope failure in which the reviewer appeared to focus on the latest commit rather than the complete committed branch delta.

In this experiment, the review output demonstrates awareness of changes beyond a single latest commit.

The experiment therefore provides initial evidence that making the review boundary explicit in both the activity and prompt improves scope adherence.

## Activity Self-Application

The experiment also exercised the newly introduced scope-establishment step in the `Methodology Change Review` activity itself.

The activity was changed specifically to address a failure observed during Experiment 0001. The subsequent MiMo run successfully operated across the intended branch scope.

This provides a small but direct example of the methodology-change-review activity being improved through experience and then tested through another application of the activity.

It does not yet establish that the new scope procedure is universally sufficient; it establishes that it worked in this experiment.

## Changes Made

**None.**

MiMo explicitly identified several issues but did not make unilateral corrections.

This differs from Experiment 0001, where the reviewer directly modified the repository during the review.

The absence of modifications in this experiment means the review output represents the agent's assessment without an agent-applied correction pass.

## Relationships

The review identified the following important relationships:

- heuristic → `Generate Broadly, Compress Deliberately` principle;
- heuristic → existing invariants;
- heuristic → `threadwright.md` §6;
- principle → heuristic;
- heuristic → scenarios;
- scenarios → heuristic;
- scenarios → `threadwright.md`;
- scenarios → assessment artifacts;
- `heuristics/README.md` → heuristic;
- `scenarios/README.md` → scenarios;
- compactness in heuristic ↔ compactness in principle;
- interconnectedness in heuristic ↔ interconnectedness in foundations.

These findings reinforce that the review was operating primarily at the level of **relationships between pieces of methodology**, rather than merely checking individual files.

## What Worked

### Explicit review scope

The revised activity and prompt successfully made the whole-branch review boundary substantially clearer.

The reviewer considered both major parts of the committed branch rather than apparently restricting itself to the latest commit.

### Fresh session

The experiment was conducted without prior conversational context.

This provides an independent observation rather than allowing the model to inherit the findings or interpretations of Experiment 0001.

### Independent findings

MiMo identified several meaningful methodological issues without being given the findings from Experiment 0001.

The findings include relationship, integration, epistemic, terminology, and compactness concerns.

### Restraint on repository modification

MiMo did not modify the repository despite identifying problems.

This makes the result easier to distinguish from the effects of an autonomous correction pass.

### Cost efficiency

The complete review cost **$0.00** through OpenCode Zen's free MiMo offering, with a reported context usage of 64,904 tokens and a duration of 5m 41s.

This makes MiMo a useful candidate for inexpensive repeated methodology-review experiments.

## What Did Not Work / Limitations

### Tool telemetry

Tool usage could not be conveniently captured.

The experiment therefore lacks a detailed execution profile describing which tools were used, how many calls were made, and which repository operations occurred.

### Scope verification is observed, not fully measured

The review output demonstrates behavior consistent with the intended whole-branch scope, but the experiment does not provide a complete independent record of the commands or repository state used to establish that scope.

### Scenario density remains unresolved

MiMo questioned whether all 12 scenarios are sufficiently distinct.

This is a useful observation but does not by itself establish that consolidation is desirable.

### Activity compression remains unresolved

MiMo raised the possibility that the rewritten methodology-change-review activity lost useful guidance while becoming more compact.

This is an important trade-off that requires further evidence rather than immediate correction.

## Deeper Observations

The experiment provides evidence that **scope establishment should be part of the activity itself**, not merely an instruction supplied externally in a prompt.

The revised activity makes the review boundary an explicit methodological operation:

> establish the evidence set before reasoning about it.

The experiment also demonstrates the value of separating the review task from the reviewer's previous conversational context. A fresh session makes the result substantially more useful as an independent experimental observation.

MiMo's review also reinforces an emerging pattern from Experiment 0001: strong methodology review is less about checking whether individual artifacts are locally reasonable and more about examining **relationships between new and existing knowledge**.

## Relation to Experiment 0001

This experiment should not yet be treated as a formal comparison or combined assessment.

It provides an independent observation under modified experimental conditions:

| Dimension | Experiment 0001 | Experiment 0002 |
|---|---|---|
| Model | Claude Sonnet | MiMo V2.5 Free |
| Session | Fresh | Fresh |
| Activity | Original | Revised |
| Prompt | Original | Revised scope wording |
| Review subject | Intended whole branch, but scope execution was incomplete | Whole committed branch appears to have been reviewed |
| `tmp/` | Explicitly excluded | Explicitly excluded |
| Repository modifications | Yes | No |
| Cost | ~$3.21 | $0.00 |
| Duration | 9m 45s | 5m 41s |
| Context | 10.75M total input tokens reported | 64,904 context tokens reported |

The experiments should be compared formally only after both records are established independently.

## Unresolved Questions

1. Does the explicit scope-establishment step reliably prevent partial-branch reviews across different tasks and agents?

2. How much of the successful scope adherence came from the revised activity versus the stronger prompt wording?

3. Is MiMo sufficiently capable for routine Threadwright methodology-change reviews, or are there classes of reviews where a stronger model provides materially better value?

4. Which of MiMo's findings correspond to genuine methodological problems versus reasonable but nonessential improvements?

5. Are the 12 scenarios sufficiently differentiated to justify their individual existence?

6. Did compression of `methodology-change-review.md` remove useful operational guidance, or did it successfully eliminate unnecessary detail?

7. How should epistemic status be represented when an established principle is elaborated by a newer operational heuristic containing both established and emerging material?

## Assessment

This experiment produced useful independent evidence at negligible monetary cost.

The revised scope discipline appears to have addressed the specific scope failure observed in Experiment 0001. The fresh-session condition also successfully isolated the review from prior discussion.

MiMo identified multiple substantive integration issues in the new branch while making no repository modifications. The findings are sufficiently specific to provide useful material for subsequent methodology work, but they should be treated as review evidence rather than automatically accepted corrections.

The strongest immediate evidence from this experiment is therefore not that every finding is correct. It is that:

> **A cheaper model, given a clean session and a more explicit review boundary, can perform a useful whole-branch methodology review and identify meaningful relationship and integration problems.**

Further experiments and subsequent methodology changes should be used to determine which observations survive contact with practice.

## Experimental Principle

Do not immediately convert observations from this experiment into methodology.

Preserve the evidence, make the planned changes one at a time, and continue observing.

A later comparative assessment of Experiment 0001 and Experiment 0002 can then evaluate:

- model capability;
- prompt effectiveness;
- activity effectiveness;
- scope adherence;
- finding convergence;
- correction behavior;
- execution cost;
- and the appropriate level of model capability for different Threadwright activities.