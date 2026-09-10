# Threadwright 🧵

> **Threadwright is infrastructure and methodology for the evolution of intent and knowledge.**

## Foundations & Provenance

Threadwright emerges from the synthesis of two distinct sources:

- **The creator's lens** — a relatively stable way of engaging with reality characterized by preferences for simplicity, explicitness, adaptability, economy, interconnectedness, and learning through observation
- **Homo Sapiens Agenticus (HSA)** — a thesis on human–agent cognitive partnership exploring complementary capabilities

Threadwright is the synthesis of these two into a practical methodology. The three layers (lens, HSA, Threadwright) remain distinct and evolve through practice and observation. Provenance is separated from prescription — practitioners need not share the creator's lens or adopt HSA.

See [`foundations.md`](foundations.md) for the complete provenance, evolutionary relationship, and non-goals.

## Central Formulation

Threadwright optimizes for reducing consequential uncertainty by selecting knowledge-generating actions that balance expected uncertainty reduction against total cost of obtaining the knowledge.

> **Given a consequential knowledge gap, choose the action that provides the greatest expected reduction in consequential uncertainty for the least total cost.**

This formulation emerged from practice and was validated through [ASSESSMENT-0008_manufactured-vs-evolved](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md). The methodology does not prescribe a particular mechanism for learning; it provides structure for choosing among them.

## 1. Purpose

Threadwright provides a minimal, implementation-agnostic way to maintain and evolve the knowledge and reasoning surrounding product development and other forms of change.

It treats development as an evolving system of knowledge, intent, decisions, and change rather than as a sequence of implementation tasks.

Its practical question is:

> Given what we are trying to achieve and what we currently know, what is the most effective way to learn what we need to know next?

Threadwright does not prescribe how a product should be implemented. It provides structure around the reasoning and knowledge that surround implementation.

## 2. Core Model

Threadwright has five fundamental concepts:

- **Change** — an intended transformation or outcome.
- **Artifact** — persistent knowledge or state.
- **Activity** — work performed to learn, decide, create, or change.
- **Relationship** — a semantic connection between artifacts, activities, and Changes.
- **Consequential Gap** — uncertainty that can materially affect a decision, outcome, commitment, risk, investment, or implementation.

These concepts are intentionally small. More specific concepts can emerge where useful without becoming fundamental elements of the methodology.

For practical application of these concepts, see the [heuristics](heuristics/README.md): [HEURISTIC-0001 — Address Consequential Gaps](heuristics/HEURISTIC-0001_address-consequential-gaps.md), [HEURISTIC-0002 — Frame Uncertainty Around Decisions](heuristics/HEURISTIC-0002_frame-uncertainty-around-decisions.md), [HEURISTIC-0003 — Choose Useful Work](heuristics/HEURISTIC-0003_choose-useful-work.md), [HEURISTIC-0004 — Reassess](heuristics/HEURISTIC-0004_reassess.md), and the cross-cutting [HEURISTIC-0008 — Epistemic Integrity](heuristics/HEURISTIC-0008_epistemic-integrity.md).

### Knowledge-Generating Actions

Threadwright does not prescribe a particular mechanism for learning. The choice of mechanism is itself part of the optimization problem.

**Manufactured knowledge** — constructed through reasoning, abstraction, modelling, calculation, analysis, synthesis of existing knowledge, research, simulation, or hypothesis construction.

**Experiential knowledge** — generated through interaction with reality: prototyping, experimentation, testing, deployment, observation, measurement, customer interaction, or operational experience.

The dynamic boundary between manufactured and experiential knowledge is determined by the current uncertainty, available options, costs, risks, and expected knowledge gain.

## 3. Intent

Intent is an evolving property of a Change: what is currently understood to be pursued, given the knowledge available at that point.

An initial request or statement does not necessarily establish intent. It may express an outcome, problem, assumption, constraint, proposed implementation, interpretation, experience, or a mixture of these — what [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md) calls "messy input."

Where ambiguity or consequences warrant it, the input should be scrutinized sufficiently to establish the outcome actually being pursued. The degree of scrutiny should be proportional to ambiguity, uncertainty, consequence, reversibility, and the cost of acting on a mistaken interpretation.

The process moves from messy input → formulation → consequential gaps → knowledge-generating action → evidence → updated intent. This progression is detailed in [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §4](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#4-messy-input-and-evolving-intent).

For practical guidance on evolving intent from messy input, see [HEURISTIC-0007 — Evolve Intent from Messy Input](heuristics/HEURISTIC-0007_evolve-intent-from-messy-input.md) and the scenario [SCENARIO-0007 — Evolving Intent from Messy Input](scenarios/SCENARIO-0007_evolve-intent-from-messy-input.md).

Interpretations remain explicit and subject to human judgment.

## 4. Control Loop

Threadwright operates through continuous adaptive reassessment:

```text
Messy Input / Initial Intent
       ↓
Formulate & Scrutinize Intent
       ↓
Identify Consequential Gaps
       ↓
Select Knowledge-Generating Action
       ↓
Execute → Evidence
       ↓
Update Knowledge & Intent
       ↓
Reassess Gaps → Repeat
```

The loop is open-ended and **adaptive**: the optimal next action depends on the current epistemic state. Reassessment may reveal that the intended outcome should change, the current understanding was incomplete, a different knowledge-generating action is required, an assumption was wrong, or no further action is justified.

This adaptive character is a structural consequence of the optimization formulation — see [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §10](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#10-adaptive).

For practical application, see [HEURISTIC-0004 — Reassess](heuristics/HEURISTIC-0004_reassess.md) and the scenario [SCENARIO-0004 — Dynamic Think/Experience Boundary Shift](scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md).

## 5. Artifact System

Artifacts are the persistent units through which Threadwright maintains knowledge and reasoning.

They may represent requirements, decisions, assessments, observations, constraints, assumptions, interpretations, designs, specifications, research findings, evidence, implementation, validation results, or other relevant knowledge and state.

Artifacts should distinguish between **manufactured knowledge** (constructed through reasoning, analysis, simulation) and **experiential knowledge** (generated through interaction with reality), as their epistemic warrant differs — see [ASSESSMENT-0008_manufactured-vs-evolved §6](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#6-knowledge-generating-actions).

For guidance on maintaining epistemic integrity in artifacts, see [HEURISTIC-0008 — Epistemic Integrity](heuristics/HEURISTIC-0008_epistemic-integrity.md) and the scenario [SCENARIO-0006 — Manufactured vs Experiential Knowledge in Artifacts](scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md).

Relationships provide semantic structure and traceability. Examples include `supports`, `derived from`, `satisfies`, `implements`, `verifies`, `depends on`, `affects`, `contradicts`, and `supersedes`.

The exact artifact taxonomy and relationship vocabulary are allowed to evolve as Threadwright is applied.

## 6. Consequential Gaps and Useful Activity

A gap is consequential when it can materially affect the intended outcome, invalidate downstream work, create unacceptable consequences, block progress, create significant rework, or undermine a consequential decision.

Not every uncertainty deserves equal attention. The relevant progression is: *unknown → relevant unknown → consequential uncertainty* — see [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §7](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#7-consequential-uncertainty-remains-the-important-target).

The objective is not to know everything. It is to know **what needs to be known next**.

For practical guidance on identifying and addressing consequential gaps, see [HEURISTIC-0001 — Address Consequential Gaps](heuristics/HEURISTIC-0001_address-consequential-gaps.md) and [HEURISTIC-0002 — Frame Uncertainty Around Decisions](heuristics/HEURISTIC-0002_frame-uncertainty-around-decisions.md).

### Cost of Learning

"Least cost" should not be interpreted as merely financial cost. The cost of reducing uncertainty can include:

- money, engineering effort, time, opportunity cost
- cognitive effort, operational disruption, physical resources
- risk, irreversibility, ethical cost, reputational cost

Likewise, the value of an action is not simply the amount of information it produces. The relevant quantity is **consequential knowledge**: knowledge that meaningfully changes what can be decided or done — see [ASSESSMENT-0008_manufactured-vs-evolved §7](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#7-the-cost-of-learning).

A useful conceptual relationship:

> **Knowledge acquisition value ≈ consequential uncertainty reduced / total cost of obtaining the knowledge**

### Selecting Knowledge-Generating Actions

Given a consequential gap, choose the action that provides the greatest expected reduction in consequential uncertainty for the least total cost. The action may be any knowledge-generating mechanism:

**Manufactured knowledge actions:**
- reason, research, analyse, model, calculate, simulate
- inspect existing knowledge, consult experts, construct hypotheses

**Experiential knowledge actions:**
- prototype, experiment, test, interview, deploy
- observe, measure, interact with users, operate the system
- expose an idea to reality

The dynamic boundary between manufactured and experiential knowledge is not merely a property of a domain — it moves within the same project as knowledge changes — see [ASSESSMENT-0008_manufactured-vs-evolved §3](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#3-the-dynamic-thinklearn-boundary) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §6](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#6-the-thinkexperience-boundary-is-dynamic).

A useful heuristic:

> **When abstraction stops producing useful knowledge, move closer to reality.**

This is the principle of **forward deployment** — see [ASSESSMENT-0008_manufactured-vs-evolved §9](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#9-forward-deployment) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §9](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#9-forward-deployment-as-a-special-case).

For detailed guidance on selecting actions, see [HEURISTIC-0005 — Choose Knowledge-Generating Action](heuristics/HEURISTIC-0005_choose-knowledge-action.md) and [HEURISTIC-0006 — Dynamic Think/Experience Boundary](heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md). For a worked example, see the scenario [SCENARIO-0005 — Optimization Invariant (I5) Stress Test](scenarios/SCENARIO-0005_optimization-invariant-i5.md).

## 7. Consequential Decisions and Evidence

Consequential decisions should remain represented when their consequences are part of the development state.

The methodology does not require certainty. When uncertainty remains, the responsible humans determine whether further work can materially improve the basis, whether the remaining uncertainty is acceptable, and whether to proceed, modify, defer, supersede, or abandon the Change.

Evidence should support the claims or decisions for which it is used and should not be generalized beyond its applicability.

Evidence should be tagged with its epistemic origin: manufactured (reasoning, analysis, simulation) or experiential (observation, experiment, deployment). This distinction matters because manufactured knowledge carries assumptions that may not hold in reality, while experiential knowledge is grounded but may be context-specific — see [ASSESSMENT-0008_manufactured-vs-evolved §5](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#5-emerging-central-formulation) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §5](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#5-manufactured-and-evolved-knowledge).

For maintaining epistemic integrity in decisions and evidence, see [HEURISTIC-0008 — Epistemic Integrity](heuristics/HEURISTIC-0008_epistemic-integrity.md) and the scenario [SCENARIO-0006 — Manufactured vs Experiential Knowledge in Artifacts](scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md).

## 8. Five Invariants

### INVARIANT-0001 — Persistence

Meaningful development work must leave its relevant results in persistent artifacts.

### INVARIANT-0002 — Outcome Orientation

A Change must establish an intended transformation against which its current state and results can be assessed.

### INVARIANT-0003 — Epistemic Integrity

The artifact state must not represent consequential knowledge, decisions, evidence, or results as more authoritative, certain, supported, applicable, or achieved than their basis justifies.

This includes distinguishing input from interpretation, hypothesis from fact, proposal from decision, implementation from outcome achievement, accepted uncertainty from hidden uncertainty, and **manufactured knowledge from experiential knowledge**.

For practical guidance, see [HEURISTIC-0008 — Epistemic Integrity](heuristics/HEURISTIC-0008_epistemic-integrity.md).

### INVARIANT-0004 — Feedback

After meaningful work or material change, the current state must be reassessed and subsequent work must respond to what that reassessment reveals.

For practical guidance, see [HEURISTIC-0004 — Reassess](heuristics/HEURISTIC-0004_reassess.md).

### INVARIANT-0005 — Optimization

Given a consequential knowledge gap, the next action should be selected to maximize expected consequential uncertainty reduction per total cost of obtaining that knowledge.

This invariant operationalizes the central formulation. It prevents both over-manufacturing (excessive analysis when reality could answer cheaply) and premature exposure to reality (learning through consequences when cheaper knowledge-generation was available) — see [ASSESSMENT-0008_manufactured-vs-evolved §8](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#8-why-the-boundary-matters).

For practical application, see [HEURISTIC-0005 — Choose Knowledge-Generating Action](heuristics/HEURISTIC-0005_choose-knowledge-action.md), [HEURISTIC-0006 — Dynamic Think/Experience Boundary](heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md), and the scenario [SCENARIO-0005 — Optimization Invariant (I5) Stress Test](scenarios/SCENARIO-0005_optimization-invariant-i5.md).

## 9. Human Judgment

Threadwright provides a structure for reasoning; it does not replace human judgment.

It can identify consequential gaps, preserve evidence, and make relationships visible. It cannot determine whether a strategy, market, architecture, objective, risk tolerance, or interpretation is correct.

> **The methodology structures human judgment; it does not replace it.**

### Autonomy vs. Automation

Threadwright may be **autonomous** in the sense that, given an intent, it can determine and pursue intermediate knowledge-generating actions without requiring an external actor to prescribe every step.

This does **not** imply that:
- humans disappear
- all actions are automated
- agents perform every action
- human judgment is removed

Humans remain active participants in the machinery. Automation concerns *who or what performs a prescribed action*; autonomy concerns *who or what determines what should happen next in pursuit of the intent* — see [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §11](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#11-autonomous-does-not-mean-automated).

The human judgment principle applies across all heuristics — see [HEURISTIC-0001](heuristics/HEURISTIC-0001_address-consequential-gaps.md), [HEURISTIC-0002](heuristics/HEURISTIC-0002_frame-uncertainty-around-decisions.md), [HEURISTIC-0003](heuristics/HEURISTIC-0003_choose-useful-work.md), [HEURISTIC-0004](heuristics/HEURISTIC-0004_reassess.md), and [HEURISTIC-0008](heuristics/HEURISTIC-0008_epistemic-integrity.md).

## 10. Boundaries

Threadwright deliberately does not prescribe:

- a specific product lifecycle;
- phases;
- Agile, Scrum, Kanban, Waterfall, or another management framework;
- organizational roles;
- project-management tooling;
- document formats;
- specification languages;
- architecture methods;
- programming languages;
- AI tools or agent architectures;
- approval workflows;
- estimation or prioritization formulas.

The methodology must remain usable by humans without AI or specialized tooling.

### Relationship to Homo Sapiens Agenticus (HSA)

**HSA concerns how humans and agents can complement each other to expand human agency.** **Threadwright concerns how intent and knowledge can evolve toward outcomes.**

The concepts are orthogonal. Threadwright may provide machinery through which aspects of HSA can be realized, but Threadwright does not exist to fulfill the HSA vision, nor is it reducible to HSA — see [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §12](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#12-relationship-to-homo-sapiens-agenticus) and [`homo-sapiens-agenticus.md`](homo-sapiens-agenticus.md).

For the foundational separation of layers, see [`foundations.md`](foundations.md).

## 11. Threadwright as Infrastructure

The methodology points toward infrastructure that can make persistent, connected knowledge and intent practical at scale without embedding domain-specific product knowledge into the infrastructure itself.

Such infrastructure can support:

- persistent artifacts;
- explicit relationships;
- provenance and historical evolution;
- discovery of relevant connected state;
- impact analysis;
- reassessment;
- human and agent collaboration.

Domain knowledge may come from humans, specialized agents, or domain-specific systems. Threadwright's concern is the structure and evolution surrounding that knowledge and intent.

### Recursive Self-Application

A particularly important property is that **Threadwright learns from its own use** — see [ASSESSMENT-0008_manufactured-vs-evolved §11](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#11-threadwrights-recursive-property) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §14](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#14-recursive-self-application).

Applying Threadwright creates experiences about which artifacts are useful, which practices create value or friction, which heuristics work, and which assumptions fail. Those experiences become knowledge that can change Threadwright itself.

The resulting loop:

> **Apply Threadwright → experience → learn → evolve Threadwright → apply again**

Therefore Threadwright is not merely a methodology for managing an external evolutionary process. It can itself evolve through the process it enables.

> **Threadwright is both an instrument for knowledge evolution and an object of knowledge evolution.**

For a worked example of recursive self-application, see the scenario [SCENARIO-0008 — Recursive Self-Application](scenarios/SCENARIO-0008_recursive-self-application.md) and [HEURISTIC-0004 — Reassess](heuristics/HEURISTIC-0004_reassess.md#recording-reassessment).

## 12. Summary

Threadwright can be summarized as:

> **Maintain a persistent, connected representation of what we are trying to achieve and what we currently know; where necessary, scrutinize the initial input to establish what outcome is actually being pursued; identify consequential gaps; select knowledge-generating actions that maximize consequential uncertainty reduction per cost; preserve the resulting knowledge and decisions; and continually reassess the state as it changes.**

Threadwright is adaptive — the machinery changes its strategy as the epistemic state changes. It is potentially autonomous — given intent, it can determine intermediate actions without requiring every step to be externally prescribed, while humans remain participants in the process. And it is recursive — it learns from its own application.

The current strongest formulation remains an **emerging hypothesis** to be tested through continued application — see [ASSESSMENT-0008_manufactured-vs-evolved §15](artifacts/assessments/ASSESSMENT-0008_manufactured-vs-evolved.md#15-emerging-hypothesis) and [ASSESSMENT-0009_assessment-of-ASSESSMENT-0008 §15](artifacts/assessments/ASSESSMENT-0009_assessment-of-ASSESSMENT-0008.md#15-revised-central-formulation).

### Quick Reference

| Concept | Methodology | Heuristic | Scenario |
|---------|-------------|-----------|----------|
| Consequential Gaps | [§6](#6-consequential-gaps-and-useful-activity) | [HEURISTIC-0001](heuristics/HEURISTIC-0001_address-consequential-gaps.md), [HEURISTIC-0002](heuristics/HEURISTIC-0002_frame-uncertainty-around-decisions.md) | [SCENARIO-0005](scenarios/SCENARIO-0005_optimization-invariant-i5.md) |
| Knowledge Actions | [§6](#6-consequential-gaps-and-useful-activity) | [HEURISTIC-0005](heuristics/HEURISTIC-0005_choose-knowledge-action.md) | [SCENARIO-0004](scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md) |
| Think/Experience Boundary | [§6](#6-consequential-gaps-and-useful-activity) | [HEURISTIC-0006](heuristics/HEURISTIC-0006_dynamic-think-experience-boundary.md) | [SCENARIO-0004](scenarios/SCENARIO-0004_dynamic-think-experience-boundary.md) |
| Intent Evolution | [§3](#3-intent) | [HEURISTIC-0007](heuristics/HEURISTIC-0007_evolve-intent-from-messy-input.md) | [SCENARIO-0007](scenarios/SCENARIO-0007_evolve-intent-from-messy-input.md) |
| Reassessment | [§4](#4-control-loop) | [HEURISTIC-0004](heuristics/HEURISTIC-0004_reassess.md) | [SCENARIO-0008](scenarios/SCENARIO-0008_recursive-self-application.md) |
| Epistemic Integrity | [§5](#5-artifact-system), [§7](#7-consequential-decisions-and-evidence) | [HEURISTIC-0008](heuristics/HEURISTIC-0008_epistemic-integrity.md) | [SCENARIO-0006](scenarios/SCENARIO-0006_manufactured-vs-experiential-artifacts.md) |
| I5 Optimization | [§8](#8-five-invariants) | [HEURISTIC-0005](heuristics/HEURISTIC-0005_choose-knowledge-action.md) | [SCENARIO-0005](scenarios/SCENARIO-0005_optimization-invariant-i5.md) |
| Recursive Self-Application | [§11](#11-threadwright-as-infrastructure) | [HEURISTIC-0004](heuristics/HEURISTIC-0004_reassess.md#recording-reassessment) | [SCENARIO-0008](scenarios/SCENARIO-0008_recursive-self-application.md) |
