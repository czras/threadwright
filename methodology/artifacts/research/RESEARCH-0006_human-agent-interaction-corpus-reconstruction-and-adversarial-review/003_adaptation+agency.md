# RESEARCH-0006/003_adaptation+agency.md

## 1. Status

Research artifact within RESEARCH-0006 — Human-Agent Interaction Corpus Reconstruction and Adversarial Review.

This artifact investigates the intersection of **adaptation** and **agency** in the Human-Agent Interaction (HAI) corpus and adjacent human-agent / human-AI teaming literature.

It is intended as an adversarial examination of concepts emerging in RESEARCH-0005, particularly:

- adaptive collaborative pursuit;
- dynamic distribution of agency;
- adaptation of both human and agent participants;
- adaptation of pursuit;
- possible adaptation of intent itself.

No conclusion in this document is Threadwright doctrine.

---

## 2. Research Question

The initial question is:

> **What does the HAI research corpus already know about the relationship between adaptation and agency?**

The investigation specifically examines:

1. What is understood by adaptation?
2. What is understood by agency?
3. Who or what adapts?
4. Who or what controls adaptation?
5. Can agency allocation itself adapt?
6. Can the task or pursuit adapt?
7. Can goals or intentions adapt?
8. Are human and agent adaptations treated symmetrically?
9. How are these dynamics represented over time?
10. Does existing research already encompass the proposed notion of adaptive collaborative pursuit?

---

## 3. Initial Historical Finding

The combination of **human-agent mutual adaptation** and agency is not a recent consequence of generative AI.

The HAI lineage contains explicit work on mutual adaptation considerably earlier than the 2020s.

A 2006 Japanese HAI paper is explicitly titled *Mutual Adaptation and Adaptation Gap between a Human and an Agent*. The paper treats adaptation as an established HAI problem rather than a new consequence of contemporary AI.

A 2007 HAI symposium paper investigated the sustainability of human-agent mutual adaptation and examined how robot behavior predictability affects the sustainability of the interaction.

Earlier adjacent work is even older: Yamada and Yamaguchi described mutual adaptation to mind mapping in human-agent interaction in 2002.

A 2012 study explicitly investigated the **formation conditions of mutual adaptation in human-agent collaborative interaction**, using an experimental collaborative task to determine conditions under which human and agent behavior adapt to one another.

Therefore:

> **Mutual adaptation between human and agent is prior art, not a research gap.**

This immediately eliminates any claim that Threadwright's adaptive-control metaphor is novel merely because it describes human-agent interaction as an adaptive loop.

---

## 4. HAI's Foundational Position

The founding international HAI conference in 2013 explicitly described human-agent interaction as involving mutual adaptation between agent and human user.

Its stated research scope included:

- theoretical models of HAI;
- agents learning from human teachers;
- agents influencing humans;
- relationships between different interactions;
- interaction design for mutual adaptation.

The conference therefore began with a conceptual territory already containing both directions of influence:

```text
human → agent
agent  → human
```

This is important because the research question cannot be reduced to:

> "Can an agent adapt to a human?"

That question has been investigated for decades.

The more interesting question is the structure of the **coupled system** produced when both participants adapt.

---

## 5. Adaptation Has Multiple Targets

The corpus reveals that "adaptation" is not one thing.

Examples include adaptation of:

- physical behavior;
- conversational behavior;
- communication strategy;
- user modeling;
- interaction style;
- task performance;
- roles;
- coordination strategies;
- expectations;
- knowledge;
- team behavior;
- agency allocation.

A 2021 study of human-agent interaction explicitly modeled agent adaptation from user reactions at behavioral, conversational, and signal levels, with the objective of improving user experience and engagement.

A 2024 adaptive virtual-agent study similarly investigated real-time reciprocal adaptation, finding that reciprocal behavioral adaptation affected user perception and interaction outcomes.

Thus:

> **Adaptation in HAI is a family of mechanisms rather than a single phenomenon.**

This matters because a claim such as "the system adapts" is insufficiently precise.

---

## 6. Mutual Adaptation and Co-Learning

One of the strongest findings is the existence of research that treats human and agent adaptation as a coupled learning process.

Van Zoelen, van den Bosch, and Neerincx (2021) describe co-learning in human-robot teams as involving two alternating processes:

1. partners adapt their behavior to the task and to one another;
2. partners sustain successful behavior through communication.

They explicitly call the first process **co-adaptation**.

Their experimental work found recurring interaction patterns in which both human and robot changed behavior in response to interaction. They further argue that increased participant adaptation improved robot learning and therefore team-level learning.

This is significant for RESEARCH-0005.

The following is therefore already established territory:

```text
human learns
   ↕
agent learns
   ↕
interaction changes
   ↕
team behavior changes
```

Consequently:

> **"Human and agent jointly adapt through interaction" does not survive as a novel hypothesis.**

---

## 7. Agency Is Already Explicitly Coupled to Adaptation

The strongest conceptual collision comes from Holter and El-Assady's 2024 framework *Deconstructing Human-AI Collaboration: Agency, Interaction, and Adaptation*.

They propose a unified design space for human-AI collaboration with three top-level dimensions:

1. agency;
2. interaction;
3. adaptation.

Their agency model distinguishes:

- **agency distribution** — who has control;
- **agency allocation** — how control is determined.

Crucially, agency allocation may be:

- **pre-determined**, or
- **negotiated** dynamically during collaboration.

This means the corpus already contains a concept very close to:

> **agency itself can be dynamically allocated during interaction.**

That is a direct hit against any simplistic claim that adaptive agency allocation is unexplored.

---

## 8. But a Temporal Problem Appears

The Holter–El-Assady framework contains an especially interesting limitation.

The authors explicitly identify **temporal dynamics** as a limitation of their design space.

Their dimensions characterize systems by generalizing over interactions, making it difficult to represent systems in which agency and adaptation change depending on the stage of the interaction. They note that agency and adaptation are often correlated with interaction stage.

This produces an important distinction.

The corpus already has:

```text
agency
adaptation
dynamic agency allocation
```

But representing the **evolution of these properties through time** remains difficult.

That does not establish a research gap by itself.

However, it identifies a potentially useful pressure point:

> **Static descriptions of agency and adaptation may be insufficient for interactions whose state changes continuously through pursuit.**

This is much closer to the control-loop idea emerging in Threadwright.

---

## 9. Adaptation Usually Preserves the Objective

A recurring pattern in the literature is:

```text
objective
   │
   ▼
observe human / environment
   │
   ▼
adapt behavior
   │
   ▼
better pursuit of objective
```

For example, adaptive agents may learn:

- user preferences;
- human intentions;
- communication style;
- capabilities;
- fatigue;
- behavior;
- knowledge.

The agent then changes its behavior to improve some defined collaboration outcome.

A 2025 perspective on adaptation in collective human-AI teaming formalizes adaptation as learning characteristics of human teammates and subsequently changing agent behavior based on those learned features. The paper considers adaptation parameters including human intentions, cognitive factors, behavior, and knowledge.

This is sophisticated adaptive behavior.

But notice the structure:

> **learn about the human → adapt behavior → better achieve the collaboration objective.**

The objective remains largely external to the adaptation mechanism.

---

## 10. Intent Is Already an Adaptation Parameter

This is where the investigation becomes more interesting.

The 2025 adaptation framework explicitly identifies **human intentions** as one possible adaptation parameter. Agents can infer the human's goals and adapt their behavior accordingly.

Therefore:

> "The agent adapts to the human's intent"

is definitely not novel.

But there is a distinction between:

### A. Adaptation *to* intent

```text
human intent = X

agent learns X
      ↓
agent adapts pursuit
```

and:

### B. Adaptation *of* intent

```text
human intent = X

interaction produces new information
      ↓
human reassesses
      ↓
intent becomes Y
      ↓
pursuit changes
```

The second structure is materially different.

The first treats intent as an input to adaptation.

The second treats intent as **a state variable that may itself be changed by the pursuit**.

This distinction requires substantially more investigation before it can be considered a genuine gap.

---

## 11. The Important Asymmetry

A large part of the literature asks:

> How should the agent adapt to the human?

Another body asks:

> How should human and agent co-adapt?

But the emerging RESEARCH-0005 hypothesis asks something stronger:

> **Can the pursuit itself generate information that changes what the participants believe they should be pursuing?**

This introduces a second feedback path:

```text
                 INTENT
                    │
                    ▼
                 PURSUIT
                    │
                    ▼
                ACTIVITY
                    │
                    ▼
               OBSERVATION
                 /     \
                /       \
               ▼         ▼
        adapt pursuit  reassess intent
```

The first branch is well established.

The second branch is the one that needs investigation.

---

## 12. The 2006–2021 Lineage Already Points Toward Coupled Dynamics

The historical evidence shows a progression:

```text
2002
mutual adaptation
        ↓
2006
mutual adaptation + adaptation gap
        ↓
2007
sustainable mutual adaptation
        ↓
2012
conditions for mutual adaptation
        ↓
2013
mutual adaptation becomes explicit
HAI research territory
        ↓
2016+
specific mutual-adaptation experiments
        ↓
2021
co-adaptation + co-learning
        ↓
2024
agency + interaction + adaptation
        ↓
2025
formalized adaptation parameters
```

This is not a new field suddenly created by LLMs.

It is a mature lineage that has progressively developed more precise models of reciprocal adaptation.

That makes it exactly the kind of corpus against which RESEARCH-0005 needs to be tested.

---

## 13. Contemporary HAI Adds Another Complication

The 2024 HAI literature contains work explicitly examining mutual adaptation involving LLMs and emergent group decision-making.

Shiiku and Takeuchi investigate mutual adaptation of LLMs and emergent decision-making in simulated small-group interactions. The work focuses on complex interaction dynamics such as compromises and new proposals emerging through group interaction.

This is particularly relevant because it moves beyond:

```text
human ↔ agent
```

toward:

```text
human(s)
   ↕
agent(s)
   ↕
emergent group process
```

Again, this makes a generic "adaptive collaborative pursuit" claim less defensible.

---

## 14. What the Corpus Has Already Killed

At this stage, the following claims should be considered **eliminated**:

### Killed hypothesis 1

> Human-agent mutual adaptation is unexplored.

**False.**

Evidence reaches back at least to the early 2000s and is explicitly present in the HAI lineage from its Japanese origins onward.

### Killed hypothesis 2

> Agency and adaptation have not been studied together.

**False.**

Holter and El-Assady explicitly construct a human-AI collaboration framework around agency, interaction, and adaptation.

### Killed hypothesis 3

> Agency can dynamically change during collaboration.

**False as a novel claim.**

Dynamic/negotiated agency allocation is explicitly modeled in existing work.

### Killed hypothesis 4

> Humans and agents can jointly learn through mutual adaptation.

**False as a novel claim.**

Co-learning and co-adaptation are established concepts with experimental work.

### Killed hypothesis 5

> Agents can adapt to human goals or intentions.

**False as a novel claim.**

Goal and intention inference are explicit adaptation parameters in current teaming research.

---

## 15. What Survives the First Attack

One potentially interesting distinction survives:

> **Adaptation of pursuit is not necessarily the same thing as adaptation of intent.**

Existing work strongly covers:

```text
human state
   ↓
agent understanding
   ↓
agent adaptation
```

and:

```text
human ↔ agent
     co-adaptation
        ↓
   better teamwork
```

It also covers:

```text
human intention
      ↓
agent adapts
```

What remains less clearly characterized is:

```text
initial intent
      ↓
pursuit
      ↓
interaction
      ↓
new knowledge
      ↓
reassessment
      ↓
changed intent
      ↓
changed pursuit
      ↓
...
```

This is not yet a claimed research gap.

It is a **candidate distinction requiring further corpus excavation**.

---

## 16. The Key Question Has Changed

The original question was approximately:

> **Can human and agent adapt to one another while pursuing an objective?**

The corpus answers:

> Yes. Very much so.

The sharper question is:

> **How is adaptation represented when the object of adaptation includes the pursuit's objective itself?**

Or more precisely:

> **How do human-agent systems represent and support situations in which interaction produces knowledge that causes participants to revise not merely their strategy for pursuing an objective, but the objective, interpretation, or desired outcome being pursued?**

That is substantially more interesting.

---

## 17. Possible Relation to Adaptive Control

The Tempomat → ACC → TW analogy now requires refinement.

Traditional control:

```text
target fixed
    ↓
adapt control action
    ↓
reach target
```

Adaptive human-agent collaboration:

```text
shared objective
    ↓
adapt behavior / roles / strategy
    ↓
improve pursuit
```

Candidate Threadwright territory:

```text
intent
  ↓
pursuit
  ↓
activity
  ↓
observation
  ↓
new knowledge
  ├──────────────→ adapt pursuit
  │
  └──────────────→ reassess intent
                         ↓
                     new pursuit
```

The defining feature would therefore **not** be adaptation itself.

It would be:

> **the possibility that feedback from pursuit changes the state of the pursuit at multiple levels, including potentially the intention governing it.**

This is the hypothesis that deserves further attack.

---

## 18. A More General Formulation

The emerging structure can be expressed without Threadwright terminology:

> A pursuit is a temporally evolving process in which observations generated by pursuing an objective may alter the agent's model of the task, the available strategies, the allocation of agency, and potentially the objective or interpretation of the objective itself.

This formulation is intentionally broader than "adaptive collaborative pursuit."

It should remain research language rather than doctrine.

---

## 19. Critical Caveat

The evidence examined so far is not sufficient to claim that goal/intent adaptation is absent from HAI.

There are several obvious adjacent literatures that could contain substantially overlapping concepts:

- dynamic goal generation;
- goal revision;
- interactive sensemaking;
- mixed-initiative planning;
- exploratory data analysis;
- co-creative systems;
- human-AI decision making;
- joint activity theory;
- distributed cognition;
- human-autonomy teaming;
- reflective practice;
- collaborative problem solving;
- interactive machine learning;
- evolving task representations.

The HAI corpus itself also contains work concerning emergent decision-making, mutual adaptation, mental models, and adaptive interaction.

Therefore:

> **Survival at this stage means "not eliminated yet," not "novel."**

---

## 20. Current Assessment

### Strongly established

| Concept | Status |
|---|---|
| Human-agent adaptation | Established |
| Mutual adaptation | Established |
| Co-adaptation | Established |
| Human-agent co-learning | Established |
| Agent adaptation to human behavior | Established |
| Agent adaptation to human intent | Established |
| Dynamic agency allocation | Established |
| Agency + adaptation as a joint design space | Established |
| Longitudinal adaptation | Established |
| Emergent interaction dynamics | Established |

### Potentially interesting

| Question | Status |
|---|---|
| How agency/adaptation evolve through time | Open design/research problem |
| Interaction producing changes in pursuit | Plausible, requires deeper extraction |
| Pursuit changing the interpretation of the task | Candidate |
| Feedback changing the objective itself | Candidate |
| Human-agent systems explicitly modeling objective revision as part of collaboration | Unknown |
| A unified model connecting intent revision, pursuit adaptation, and agency reallocation | Unknown |

---

## 21. Research Consequence

The corpus has already forced a substantial narrowing.

We should **not** continue researching "adaptive collaboration."

That territory is enormous and heavily populated.

The next attack should target the following distinction:

```text
ADAPTATION OF PURSUIT
        versus
ADAPTATION OF INTENT
```

and then investigate whether existing HAI work already unifies:

```text
intent revision
      +
pursuit adaptation
      +
agency reallocation
      +
human-agent co-adaptation
```

If it does, the current hypothesis dies.

If those components exist separately but are not conceptually integrated, that becomes interesting.

If the combination is already explicitly theorized, we kill it anyway and follow the prior art.

---

## 22. Current Research Position

The first corpus drill therefore produces neither validation nor rejection of adaptive collaborative pursuit.

It produces a sharper target.

> **The potentially interesting phenomenon is not mutual adaptation. It is whether a human-agent pursuit can adapt at multiple levels, including the possibility that the pursuit generates information that changes the intention governing the pursuit itself.**

This distinction is currently a **research hypothesis**.

It has earned another round of investigation.

It has not earned a Threadwright concept.

---

## 23. Next Excavation

The next corpus drill should specifically search for:

1. **goal revision**
2. **dynamic goals**
3. **changing task objectives**
4. **intent revision**
5. **interactive sensemaking**
6. **co-creation of goals**
7. **emergent goals**
8. **mixed-initiative goal negotiation**
9. **goal-directed human-agent interaction**
10. **human-agent systems where interaction changes what the participants are trying to accomplish**

The question is now:

> **Has HAI already discovered the changing-objective problem under another name?**