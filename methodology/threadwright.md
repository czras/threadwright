# Threadwright 🧵

> **Threadwright is infrastructure and methodology for the evolution of intent and knowledge.**

## 1. Purpose

Threadwright provides a minimal, implementation-agnostic way to maintain and evolve the knowledge and reasoning surrounding product development and other forms of change.

It treats development as an evolving system of knowledge, intent, decisions, and change rather than as a sequence of implementation tasks.

Its practical question is:

> Given what we are trying to achieve and what we currently know, what should we do next?

Threadwright does not prescribe how a product should be implemented. It provides structure around the reasoning and knowledge that surround implementation.

## 2. Core model

Threadwright has four fundamental concepts:

- **Change** — an intended transformation or outcome.
- **Artifact** — persistent knowledge or state.
- **Activity** — work performed to learn, decide, create, or change.
- **Relationship** — a semantic connection between artifacts, activities, and Changes.

These concepts are intentionally small. More specific concepts can emerge where useful without becoming fundamental elements of the methodology.

## 3. Intent

Intent is an evolving property of a Change: what is currently understood to be pursued, given the knowledge available at that point.

An initial request or statement does not necessarily establish intent. It may express an outcome, problem, assumption, constraint, proposed implementation, interpretation, experience, or a mixture of these.

Where ambiguity or consequences warrant it, the input should be scrutinized sufficiently to establish the outcome actually being pursued. The degree of scrutiny should be proportional to ambiguity, uncertainty, consequence, reversibility, and the cost of acting on a mistaken interpretation.

Interpretations remain explicit and subject to human judgment.

## 4. Control loop

Threadwright operates through continuous reassessment:

```text
Intended Outcome
      ↓
Current State
      ↓
Consequential Gaps
      ↓
What must be learned, decided, or changed?
      ↓
Activity
      ↓
Updated Artifact State
      ↓
Reassess
      ↺
```

The loop is open-ended. Reassessment may reveal that the intended outcome should change, the current understanding was incomplete, a different activity is required, an assumption was wrong, or no further action is justified.

## 5. Artifact system

Artifacts are the persistent units through which Threadwright maintains knowledge and reasoning.

They may represent requirements, decisions, assessments, observations, constraints, assumptions, interpretations, designs, specifications, research findings, evidence, implementation, validation results, or other relevant knowledge and state.

Relationships provide semantic structure and traceability. Examples include `supports`, `derived from`, `satisfies`, `implements`, `verifies`, `depends on`, `affects`, `contradicts`, and `supersedes`.

The exact artifact taxonomy and relationship vocabulary are allowed to evolve as Threadwright is applied.

## 6. Consequential gaps and useful activity

A gap is consequential when it can materially affect the intended outcome, invalidate downstream work, create unacceptable consequences, block progress, create significant rework, or undermine a consequential decision.

Not every gap requires research, and not every activity needs to be formalized. The appropriate activity depends on the current state, consequences, uncertainty, dependencies, cost, reversibility, and available capacity.

Useful activities may include research, interviewing, analysis, design, implementation, prototyping, testing, validation, review, investigation, or decision-making.

## 7. Consequential decisions and evidence

Consequential decisions should remain represented when their consequences are part of the development state.

The methodology does not require certainty. When uncertainty remains, the responsible humans determine whether further work can materially improve the basis, whether the remaining uncertainty is acceptable, and whether to proceed, modify, defer, supersede, or abandon the Change.

Evidence should support the claims or decisions for which it is used and should not be generalized beyond its applicability.

## 8. Four invariants

### I1 — Persistence

Meaningful development work must leave its relevant results in persistent artifacts.

### I2 — Outcome orientation

A Change must establish an intended transformation against which its current state and results can be assessed.

### I3 — Epistemic integrity

The artifact state must not represent consequential knowledge, decisions, evidence, or results as more authoritative, certain, supported, applicable, or achieved than their basis justifies.

This includes distinguishing input from interpretation, hypothesis from fact, proposal from decision, implementation from outcome achievement, and accepted uncertainty from hidden uncertainty.

### I4 — Feedback

After meaningful work or material change, the current state must be reassessed and subsequent work must respond to what that reassessment reveals.

## 9. Human judgment

Threadwright provides a structure for reasoning; it does not replace human judgment.

It can identify consequential gaps, preserve evidence, and make relationships visible. It cannot determine whether a strategy, market, architecture, objective, risk tolerance, or interpretation is correct.

> **The methodology structures human judgment; it does not replace it.**

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

## 11. Threadwright as infrastructure

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

## 12. Summary

Threadwright can be summarized as:

> **Maintain a persistent, connected representation of what we are trying to achieve and what we currently know; where necessary, scrutinize the initial input to establish what outcome is actually being pursued; identify consequential gaps; choose and perform useful activities; preserve the resulting knowledge and decisions; and continually reassess the state as it changes.**
