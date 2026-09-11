# RESEARCH-0006/005_pursuit+knowledge+intent.md

## 1. Status

Research artifact within RESEARCH-0006 — Human-Agent Interaction Corpus Reconstruction and Adversarial Review.

This artifact investigates the hypothesis that:

> **Pursuing an intent can generate knowledge that changes the intent being pursued.**

The purpose is to determine whether this phenomenon is already described in existing research under other terminology, particularly:

- objective co-construction;
- problem framing and reframing;
- sensemaking;
- epistemic action;
- reflective practice;
- exploratory inquiry;
- preference elicitation;
- interactive problem solving.

No conclusion in this document is Threadwright doctrine.

---

# 2. Research Question

The initial hypothesis is:

```text
INTENT
   ↓
PURSUIT
   ↓
ACTIVITY
   ↓
OBSERVATION
   ↓
KNOWLEDGE
   ↓
REVISED INTENT
   ↓
NEW PURSUIT
```

The research question is:

> **Does existing research already model pursuit as a process that generates knowledge capable of changing the intent or objective governing the pursuit?**

A secondary question is:

> **If this phenomenon is already established, what distinction, if any, remains between existing formulations and the model emerging in RESEARCH-0005?**

---

# 3. Immediate Finding

The hypothesis is **substantially covered by existing research**.

The strongest prior art identified in this excavation is **Dutta et al. (2025), Problem Solving Through Human–AI Preference-based Cooperation**, which proposes HAI-Co².

The framework explicitly includes:

1. human and AI jointly constructing a solution;
2. human and AI jointly constructing the objective;
3. iterative refinement of requirements as the collaborators understand the problem better;
4. revision of initial assumptions during the process.

This is a direct hit.

The authors explicitly state that in complex expert-domain problems, the exact goal is often underspecified initially, so cooperation involves constructing both the solution and the precise objective.

Therefore:

> **The broad proposition that human-agent pursuit can change the objective as participants learn more about the problem is already established prior art.**

---

# 4. HAI-Co² Is Particularly Close

HAI-Co² is not merely a system that detects a changed goal.

Its conceptual model is:

```text
initial problem
      ↓
co-construct solution
      ↓
understand problem better
      ↓
revise assumptions
      ↓
change/refine requirements
      ↓
co-construct objective
      ↓
continue solution construction
```

The authors explicitly describe objective co-construction as occurring alongside solution co-construction. They formalize the objective through interactive preference learning, with the preference model changing as collaborators provide information about which candidate solutions are better or worse.

This means that the following claim is already dead:

> "Human-agent interaction can cause the objective itself to evolve."

It exists explicitly.

---

# 5. The Stronger Hit: Understanding the Problem Changes the Objective

The most damaging sentence for the hypothesis is not merely that objectives can change.

It is the causal relationship:

```text
understand the details of the complex problem better
                    ↓
             revise assumptions
                    ↓
          change/refine requirements
```

That is almost exactly the causal structure being investigated here.

Therefore the original formulation:

> pursuit → knowledge → changed intent

cannot be claimed as a new conceptual discovery.

A closely related formulation already exists:

> solution construction → improved understanding → revised assumptions → changed/refined requirements → objective co-construction.

---

# 6. But There Is an Important Difference

HAI-Co² conceptualizes the process primarily through **objective co-construction and preference learning**.

Its formal mechanism is roughly:

```text
human preferences
        +
agent preferences
        ↓
preference model
        ↓
utility over candidate solutions
        ↓
search
        ↓
candidate solution
        ↓
feedback
        ↓
updated preferences
```

The framework treats objective co-construction as refinement of the utility/preference representation over a construction space.

The present research hypothesis is framed differently.

It asks whether:

```text
pursuit itself
      ↓
produces epistemically consequential observations
      ↓
changes understanding
      ↓
changes what should be pursued
```

The distinction is therefore no longer:

> **"Can objectives change?"**

They can.

It becomes:

> **What role does the pursuit itself play in generating the knowledge that justifies changing the objective?**

That is narrower.

---

# 7. Epistemic Action Predates Human-Agent Research

The underlying mechanism is not new to AI.

Kirsh and Maglio's 1994 work on **epistemic actions** distinguishes actions performed to change the world in order to make information easier to obtain from ordinary pragmatic actions performed to move toward a goal.

The core distinction is:

```text
pragmatic action
    ↓
move toward goal

epistemic action
    ↓
obtain information
    ↓
improve cognition
```

Thus the basic proposition:

> **acting can be a way of acquiring knowledge**

has decades of prior art.

This is important because it eliminates another possible novelty claim.

The phenomenon does not begin with human-agent collaboration.

---

# 8. Epistemic Action Creates a More Interesting Loop

Combining epistemic action with the changing-objective problem produces:

```text
        GOAL
          ↓
       ACTION
          ↓
   INFORMATION
          ↓
    BETTER MODEL
          ↓
    GOAL REASSESSMENT
          ↓
     NEW ACTION
```

The existence of this loop is therefore not itself novel.

What remains interesting is its application to human-agent collaboration and the **allocation of epistemic work** between human and agent.

That is a different question.

---

# 9. Reflective Practice Provides Another Prior-Art Hit

Design research provides an even older conceptual lineage.

Schön's reflective practice treats professional activity as an ongoing conversation with a situation: the practitioner frames a problem, acts, encounters consequences, and revises understanding.

Empirical research on multidisciplinary design teams has described this as an iterative process involving:

1. sensemaking;
2. future framing;
3. surprise;
4. reframing;
5. learning and innovation.

This is extremely close to:

```text
frame
 ↓
act
 ↓
consequence
 ↓
understand
 ↓
reframe
 ↓
act again
```

Therefore:

> **Human pursuit generating knowledge that changes how the pursuit is framed is established in reflective-practice and design research.**

---

# 10. Problem Framing Is Already Dynamic

Problem framing research explicitly rejects the assumption that a practitioner simply receives a fully specified problem and then solves it.

Schön's framing concept concerns deciding what aspects of a problematic situation deserve attention and imposing a structure that guides subsequent action.

Team-framing research extends this to collaborative situations and investigates how teams negotiate shifts in frames during design.

Thus:

```text
problem
  ↓
frame
  ↓
action
  ↓
new understanding
  ↓
frame shift
  ↓
new action
```

is well-established.

---

# 11. Surprise as a Trigger for Reframing

Research on multidisciplinary design teams provides a particularly useful causal mechanism.

Stompff et al. describe **surprises** as triggers for reframing. The team encounters something outside its expectations, performs sensemaking, and constructs a new frame for subsequent activity. The authors connect these reframing processes to team learning and innovation.

This provides a concrete mechanism:

```text
pursuit
   ↓
unexpected observation
   ↓
surprise
   ↓
sensemaking
   ↓
reframing
   ↓
new pursuit
```

That is extremely close to the emerging Threadwright intuition.

Again:

> **The mechanism is not novel.**

---

# 12. Human-AI Sensemaking Now Explicitly Contains Objective Revision

The contemporary AI literature makes the connection even tighter.

The 2026 *Sensemaking AI* research agenda argues that AI systems should support participatory formation and **revision of objectives**, rather than simply optimize predetermined objectives. It explicitly calls for ongoing contextualisation and preservation of human judgment where values remain contestable.

This directly attacks the assumption that objective revision is outside the AI system's proper operating model.

Instead:

```text
information
   ↓
sensemaking
   ↓
objective formation
   ↓
decision
   ↓
new information
   ↓
objective revision
```

is being proposed as a legitimate design target for human-AI systems.

---

# 13. Collaborative Causal Sensemaking

A 2025/2026 research agenda titled *Collaborative Causal Sensemaking* goes even further.

It explicitly proposes human-AI decision support in which:

- mental models;
- goals;
- constraints;
- causal hypotheses

are continually co-constructed, tested, and revised.

The proposed agents would help humans articulate and revise goals, stress-test causal hypotheses, and learn from outcomes of joint decisions.

This is another strong prior-art collision.

The structure is essentially:

```text
human + AI
     ↓
joint model
     ↓
hypothesis
     ↓
decision
     ↓
outcome
     ↓
revised model / goal / constraint
     ↓
next decision
```

---

# 14. The Research Has Therefore Found a Dense Existing Territory

At this point the conceptual family looks like:

```text
                   ┌──────────────────┐
                   │   OBJECTIVE      │
                   └────────┬─────────┘
                            │
                            ▼
                       PURSUIT / ACT
                            │
                            ▼
                       CONSEQUENCE
                            │
                            ▼
                      INFORMATION
                            │
                            ▼
                       SENSEMAKING
                       /          \
                      /            \
                     ▼              ▼
             REVISE MODEL      REVISE GOAL
                     \              /
                      \            /
                       ▼          ▼
                         NEW PURSUIT
```

Different research communities have studied different edges:

| Edge | Research territory |
|---|---|
| Action → information | Epistemic action |
| Consequence → understanding | Reflective practice |
| Surprise → reframing | Design / sensemaking |
| Human + AI → shared understanding | Human-AI sensemaking |
| Solution → revised requirements | HAI-Co² |
| Preferences → objective | Preference learning |
| Outcome → revised goals | Decision support |
| Human + AI → revised goals | Collaborative causal sensemaking |

This is not empty territory.

It is a **well-populated conceptual intersection**.

---

# 15. HAI-Co² Changes the Status of the Hypothesis

Before this excavation, the working hypothesis was:

> pursuit generates knowledge that can change intent.

After this excavation:

> **Existing research already describes pursuit generating understanding that changes requirements and objectives in human-AI co-construction.**

Therefore the hypothesis, as a novelty claim, **does not survive**.

That is a successful research result.

---

# 16. But Something Important Survives

The interesting residue is not the phenomenon itself.

It is the **architecture of the process**.

Existing work describes many mechanisms independently or within specialized frameworks.

The emerging Threadwright structure is:

```text
INTENT
   ↓
PURSUIT
   ↓
ACTIVITY
   ↓
OBSERVATION
   ↓
KNOWLEDGE
   ↓
REASSESS
   ├── change activity
   ├── change pursuit
   ├── change agency allocation
   ├── change framing
   └── change intent
```

The potentially interesting question becomes:

> **Can these levels of change be represented as one general-purpose adaptive pursuit model rather than as separate phenomena such as goal negotiation, problem reframing, co-learning, agency allocation, and sensemaking?**

This is an integration question, not a discovery claim.

---

# 17. Another Important Finding: The Human Does Not Necessarily Own the Objective

HAI-Co² is particularly relevant here.

It explicitly treats the human and AI as complementary participants in **objective co-construction**, rather than treating the objective as permanently owned by the human.

That challenges an assumption embedded in some earlier RESEARCH-0005 language:

> "the human changes intent and the agent adapts."

The more general model is:

```text
human ↔ agent
      ↓
joint understanding
      ↓
jointly evolving objective
```

This may be more accurate than a human-centered intent model.

---

# 18. But Objective Co-Construction Is Not Necessarily Intent Adaptation

There is still an important distinction.

An objective can be refined because:

- requirements become more precise;
- preferences become explicit;
- trade-offs become visible;
- constraints are discovered;
- candidate solutions reveal implications.

That does not necessarily mean the human's **underlying intent** changes.

For example:

```text
Intent:
"build something useful for X"

Objective refinement:
"it must support A, B and C"
```

The underlying intent may remain stable.

Thus:

> **objective revision ≠ necessarily intent revision.**

This distinction should be preserved.

---

# 19. Three Levels of Change

The research therefore suggests separating at least three phenomena:

### Level 1 — Objective refinement

```text
same broad intent
      ↓
more precise objective
```

### Level 2 — Problem reframing

```text
same situation
      ↓
different interpretation
      ↓
different formulation of the problem
```

### Level 3 — Intent transformation

```text
initial intent
      ↓
new understanding
      ↓
different thing is now considered worth pursuing
```

The first two are extremely well represented in prior research.

The third is more philosophically and practically significant, but evidence from this excavation is not sufficient to claim that it is absent.

---

# 20. The Most Interesting Remaining Question

The question should therefore be reformulated again:

> **What distinguishes refinement of an objective from transformation of the intent underlying the objective, and how does human-agent interaction contribute to that transformation?**

This is considerably more precise than:

> "Can pursuit change intent?"

It also avoids inventing a new term prematurely.

---

# 21. Connection to the Expertise Problem

This distinction reconnects to RESEARCH-0005.

Suppose the human begins with:

```text
Intent:
"solve problem X"
```

The agent can help optimize:

```text
Objective:
"produce solution X satisfying A, B, C"
```

But the human may discover:

```text
X is not actually the important problem.
```

That is qualitatively different.

The system has not merely improved the solution.

It has improved the **problem selection process**.

This is where the capability-development question becomes interesting:

> Does an agent help the human become better at recognizing when the objective itself deserves reconsideration?

That is a different research branch from dynamic objectives.

---

# 22. Connection to Epistemic Agency

The educational and cognitive literature uses the concept of **epistemic agency** for the capacity to actively construct, evaluate, revise, and advance knowledge during problem solving.

Research on collaborative problem solving identifies epistemic actions such as proposing explanations, testing ideas, evaluating evidence, revising interpretations, and incorporating others' findings.

This provides another potentially useful distinction:

```text
task agency
    ↓
doing the thing

epistemic agency
    ↓
deciding what to believe,
what to investigate,
and how to revise understanding
```

This may connect directly to RESEARCH-0005's emerging distinction between:

- execution;
- judgment;
- evaluation;
- deciding what to investigate next.

However, this is an adjacent conceptual territory requiring its own investigation.

---

# 23. Important Negative Result

The phrase:

> **pursuit generates knowledge**

sounds novel only if "pursuit" is interpreted narrowly.

In the broader literature, this is already everywhere:

- epistemic action;
- inquiry;
- experimentation;
- reflective practice;
- exploratory design;
- sensemaking;
- scientific investigation;
- interactive problem solving.

The novelty cannot be the proposition itself.

The useful question is instead:

> **How does an AI-mediated pursuit alter the human's epistemic process, particularly their ability to recognize when the current objective should be reconsidered?**

That question connects directly to the expertise/capability branch.

---

# 24. Current Adversarial Verdict

### Killed

> Pursuit can generate knowledge.

**Established.**

> Knowledge generated during pursuit can change requirements.

**Established.**

> Human-AI collaboration can co-construct objectives.

**Established.**

> Human-AI interaction can support objective revision.

**Established.**

> Problem framing can change through action and reflection.

**Established.**

> Human-AI sensemaking can revise goals and constraints.

**Established / emerging.**

### Not yet killed

> There is a useful distinction between objective refinement and deeper intent transformation.

> Existing human-AI research may not yet provide a unified model of execution, pursuit, agency, framing, objective, and intent adaptation across timescales.

> AI-mediated pursuit may alter not only the solution but the human's capability to recognize and revise what should be pursued.

The final two are **research questions**, not claims.

---

# 25. Current Model

The best current abstraction is:

```text
                     INTENT
                       │
                       ▼
                    OBJECTIVE
                       │
                       ▼
                    PURSUIT
                       │
                       ▼
                    ACTIVITY
                       │
                       ▼
                  OBSERVATION
                       │
                       ▼
                   KNOWLEDGE
                       │
                       ▼
                  REASSESSMENT
                  /    |      \
                 /     |       \
                ▼      ▼        ▼
           activity  objective  intent
            change    change     change
                 \     |        /
                  \    |       /
                   ▼   ▼      ▼
                     PURSUIT
```

This is a **research model only**.

It is not yet a Threadwright model.

---

# 26. Current Position

`005_pursuit+knowledge+intent.md` substantially weakens the hypothesis that:

> pursuit → knowledge → changed intent

constitutes a novel research phenomenon.

Existing work already describes closely related mechanisms, including explicit human-AI objective co-construction.

The strongest evidence is HAI-Co², whose authors explicitly state that complex collaborative problem solving involves constructing both the solution and its objective, with requirements changing as collaborators understand the problem and revise assumptions.

The research therefore produces another successful narrowing:

> **The interesting question is not whether pursuit can change objectives. It can.**

The next question is:

> **What is the difference between refining an objective, reframing a problem, and transforming the underlying intent—and what does human-agent collaboration do to those processes?**

A second, potentially more important question emerges:

> **Does AI assistance change the human's epistemic agency: their capacity to discover, evaluate, and revise what is worth pursuing?**

That question reconnects the adaptation/intent investigation with the capability-development problem in RESEARCH-0005.

---

# 27. Next Excavation

The next research target should therefore shift from the generic causal chain to **epistemic agency and capability**.

Priority concepts:

1. epistemic agency;
2. epistemic autonomy;
3. human-AI sensemaking;
4. human-AI inquiry;
5. metacognition;
6. reflective practice;
7. problem formulation;
8. problem selection;
9. inquiry generation;
10. human capability development during AI-assisted problem solving.

The key question becomes:

> **When an AI participates in the process of deciding what to investigate, what to believe, and what to pursue next, does it strengthen or substitute for the human's epistemic agency?**