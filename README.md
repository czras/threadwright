# Threadwright 🧵

**Threadwright is an implementation-agnostic methodology for developing and evolving products through persistent artifacts, explicit relationships, consequential-gap identification, useful activity, and continuous reassessment.**

## Overview

Threadwright treats product development as an evolving system of knowledge, intent, decisions, and change rather than as a sequence of implementation tasks.

A key implication is that an initial request or statement does not necessarily establish the intended outcome. Input may express an outcome, problem, assumption, constraint, proposed implementation, interpretation, experience, or a mixture of these.

> **Input is evidence about intent, not necessarily intent itself.**

Where ambiguity or the consequences of misunderstanding warrant it, the input should be scrutinized sufficiently to establish the outcome actually being pursued. The degree of scrutiny should be proportional to factors such as ambiguity, uncertainty, consequence, reversibility, and the cost of a mistaken interpretation.

This does not introduce a separate intent-extraction phase. Scrutiny and clarification are simply useful activities within the methodology, performed when needed.

Threadwright does not prescribe how a product should be implemented. It provides a way to maintain and evolve the knowledge and reasoning that surround implementation.

## Core Model

Threadwright has four fundamental concepts:

| Concept | Meaning |
|---|---|
| **Change** | An intended transformation or outcome |
| **Artifact** | Persistent knowledge or state |
| **Activity** | Work performed to learn, decide, create, or change |
| **Relationship** | A semantic connection between artifacts, activities, and Changes |

These concepts are intentionally small. More specific concepts can emerge where useful without becoming fundamental elements of the methodology.

Artifacts may represent many kinds of knowledge, including requirements, decisions, assessments, observations, constraints, assumptions, or interpretations.

### Intent

Intent is **not** a fifth fundamental concept.

Intent is an evolving property of a Change: what is currently understood to be pursued, given the knowledge available at that point.

As knowledge and experience change, the understanding of what should be achieved may also change. Threadwright therefore supports evolution of both:

- **What do we believe to be true?**
- **What are we trying to achieve, given what we now understand?**

Interpretations of input should remain explicit and subject to human judgment rather than being silently treated as established intent.

## Control Loop

Threadwright operates through a continuous control loop:

> **Intended Outcome → Current State → Consequential Gaps → What must be learned/decided/changed? → Activity → Updated Artifact State → Reassess**

The loop assumes that a usable intended outcome has been established for the Change being assessed.

When an initial input does not yet establish that outcome, scrutinizing and clarifying the input is simply useful activity within the methodology rather than a separate phase.

The loop is deliberately open-ended. Reassessment may reveal:

- that the intended outcome should change,
- that the current understanding was incomplete,
- that a different activity is required,
- that an assumption was wrong,
- or that no further action is justified.

## Invariants

### I1 — Persistence

Knowledge and meaningful state must persist as artifacts rather than existing only in transient activity.

### I2 — Outcome Orientation

Activities and decisions must remain connected to an intended transformation or outcome.

An initial request or statement does not necessarily establish that outcome accurately. Where consequential ambiguity exists, it must be scrutinized rather than silently treated as established intent.

### I3 — Epistemic Integrity

Artifacts must not claim more certainty than the available evidence supports.

Input, interpretation, assumption, observation, decision, and accepted outcome should remain distinguishable where that distinction matters.

### I4 — Feedback

The result of activity must be capable of changing the state of the system and influencing subsequent decisions.

No artifact, decision, or intended outcome is permanently authoritative merely because it exists.

## Artifact System

Artifacts are the persistent units through which Threadwright maintains knowledge and reasoning.

The artifact system defines conventions for:

- artifact identity,
- artifact types,
- storage,
- linking,
- and relationships between artifacts.

See [`conventions/artifact-system.md`](conventions/artifact-system.md).

A typical chain might look like:

> **ASSESSMENT → DECISION → CHANGE → ACTIVITY → updated ARTIFACT STATE**

The exact artifact types and relationships are allowed to evolve as the methodology is applied.

## Methodology vs. Judgment

Threadwright provides a structure for reasoning; it does not replace human judgment.

The methodology can identify that a consequential gap exists, but determining what the gap means and what should be done about it may require human judgment.

In particular, Threadwright does not assume that:

- an input is equivalent to intent,
- an interpretation is automatically correct,
- a proposed implementation is the right solution,
- every gap requires action,
- or every activity needs to be formalized as an artifact.

## Boundaries

Threadwright intentionally does **not** prescribe:

- a particular development methodology,
- a project-management system,
- a software architecture,
- an implementation technology,
- a mandatory intent-extraction phase,
- a fixed artifact taxonomy,
- a fixed vocabulary of relationships,
- or a particular tooling implementation.

The methodology should remain usable whether the surrounding work is performed manually, with conventional development tools, or with agentic tooling.

## Key Distinctions

### Input vs. Interpretation vs. Intended Outcome

| Concept | Meaning |
|---|---|
| **Input** | What a human or other source provides |
| **Interpretation** | A representation of what the input appears to mean |
| **Intended Outcome** | The currently accepted representation of what a Change intends to achieve |

For example:

> **Input:** “We need a mobile app.”

This may be a proposed implementation rather than the actual outcome.

An interpretation might be:

> “The person believes a mobile application is needed to achieve something.”

The methodology then allows the underlying outcome to be established before implementation is treated as the direction of the Change.

### Methodology vs. Judgment vs. Organizational Failure

| Situation | Character |
|---|---|
| The methodology provides a loop for identifying consequential gaps | **Methodology** |
| A person decides what evidence is sufficient to act | **Judgment** |
| An important gap is recognized but repeatedly ignored | **Organizational failure** |
| Input is taken at face value despite consequential ambiguity | **Methodological/judgment failure** |

## Minimal Human Operating Model

A person applying Threadwright can repeatedly ask:

1. **What are we trying to achieve?**
2. **What do we currently know?**
3. **What consequential gap prevents progress?**
4. **What must be learned, decided, or changed?**
5. **What activity will address that gap?**
6. **What artifact state changed as a result?**
7. **What does that change imply when we reassess?**
8. **Does the input actually establish the intended outcome, or do we need to clarify what it represents?**

This is not a required workflow. It is a compact way of operating the control loop.

## What's Coming

The methodology also points toward tooling that can make it practical to use without embedding domain-specific product knowledge into the tooling itself.

Two tooling directions have already emerged from applying and examining the methodology:

- **Implementation design tooling** — tooling that helps humans and agents apply Threadwright to a concrete implementation context, maintaining the artifacts, relationships, reasoning, and activities involved in evolving that implementation.
- **Artifact system exploration tooling** — tooling for exploring artifacts, their relationships, and the evolving state of a Threadwright-managed body of work.

These are **tooling ideas, not a committed roadmap**. They are included here to make visible the kinds of capabilities that appear necessary or useful for applying the methodology in practice.

The specific form, architecture, and implementation of such tooling remain open.

## Repository Structure

The repository currently contains:

| Path | Purpose |
|---|---|
| `methodology/` | The Threadwright methodology |
| `conventions/` | Conventions for working with the methodology and repository |
| `meta/` | Project and brand context |

The methodology itself is primarily expressed through:

- `methodology/methodology.md`
- `methodology/scenarios.md`
- `methodology/application-heuristics.md`

Repository conventions include:

- `conventions/artifact-system.md`
- `conventions/git.md`

## License

Threadwright contains content under different licensing terms:

- **Methodology** (content of the [`methodology`](methodology) folder) is licensed under [**CC BY-NC-SA 4.0**](https://creativecommons.org/licenses/by-nc-sa/4.0/). You're free to use, adapt, and share it — attributed, noncommercial, and any derivative must carry the same license. See [LICENSE-METHODOLOGY](LICENSE-METHODOLOGY).

- **Tooling** is licensed under [**AGPLv3**](https://www.gnu.org/licenses/agpl-3.0.html). Commercial use is permitted, but modifications — including running a modified version as a network service — must have their source made available under the same license. See [LICENSE](LICENSE).

- **Brand and other reserved content** is not covered by the above licenses unless explicitly stated otherwise. In particular, [`meta/brand.md`](meta/brand.md) is **All Rights Reserved**.
