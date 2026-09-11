# RESEARCH-0006/004_adaptive_pursuit+intent.md

## 1. Status

Research artifact within RESEARCH-0006 — Human-Agent Interaction Corpus Reconstruction and Adversarial Review.

This artifact investigates whether existing research already describes the phenomenon emerging from RESEARCH-0005 and 003:

> **A pursuit in which feedback from the pursuit can change not only how the pursuit is conducted, but the intent or objective governing the pursuit itself.**

This is an adversarial investigation.

The objective is not to validate adaptive pursuit + intent, but to determine whether the distinction survives existing literature under alternative terminology.

---

## 2. Research Question

The initial hypothesis is:

> A human-agent pursuit may be adaptive at multiple levels: activity, strategy, agency allocation, interpretation, and potentially intent itself.

The central question is:

> **Has existing research already described human-agent systems in which interaction and pursuit can cause the objective or intent itself to change, rather than merely changing the means of achieving a fixed objective?**

Secondary questions:

1. Are dynamic goals already established?
2. Is goal revision already established?
3. Is goal negotiation already established?
4. Can goals emerge through interaction?
5. Can human and agent jointly construct or redefine a goal?
6. Is goal change merely an input to adaptation, or is it part of the adaptive process?
7. Is there an established model connecting:
   - intent revision,
   - pursuit adaptation,
   - agency reallocation,
   - interaction,
   - and learning?
8. If such models exist, what remains unexplained?

---

## 3. Immediate Result

The hypothesis is **not novel in its broad form**.

The corpus contains substantial work on:

- changing human goals;
- dynamic goal recognition;
- goal inference;
- goal negotiation;
- problem reframing;
- co-creation;
- adaptive processes driven by evolving goals;
- explicit representations of goals in human-AI collaboration.

Most significantly, a 2026 CHI workshop paper argues that goals should become first-class abstractions in human-AI collaboration because goals are often implicit, changing, poorly represented, or confused with outputs.

A 2026 CHI paper on "Just-In-Time Objectives" goes further: it explicitly treats user objectives as being in constant flux and proposes dynamically inducing and updating AI objectives from observed user tasks.

Therefore:

> **"Human-agent systems should be able to adapt to changing goals" is already established territory.**

However, a potentially sharper distinction survives.

---

# 4. Fixed Objective vs Changing Objective

A conventional adaptive system can be represented as:

```text
OBJECTIVE
    │
    ▼
CURRENT STATE
    │
    ▼
GAP
    │
    ▼
ADAPT ACTION
    │
    ▼
NEW STATE
    │
    └───────────────► repeat
```

The objective remains outside the adaptation loop.

A changing-objective system can instead be represented as:

```text
              ┌──────────────┐
              │   INTENT     │
              └──────┬───────┘
                     │
                     ▼
                 PURSUIT
                     │
                     ▼
                 ACTIVITY
                     │
                     ▼
               OBSERVATION
                 /       \
                /         \
               ▼           ▼
          adapt action   revise intent
               │           │
               └─────┬─────┘
                     ▼
                  PURSUIT
```

The important question is not whether the goal can change.

It clearly can.

The question is:

> **Is goal change itself modeled as an endogenous consequence of pursuing the goal?**

That distinction becomes important below.

---

# 5. Dynamic Human Goals Are Established

Recent robotics research explicitly considers humans changing goals during collaboration.

A 2026 IEEE Robotics and Automation Letters paper titled *I've Changed My Mind: Robots Adapting to Changing Human Goals During Collaboration* starts from the observation that humans frequently shift goals during real-world tasks.

Its contribution is a robot that detects goal changes during collaboration and adapts its planning accordingly.

This directly kills:

> "Human goals changing during a task is unexplored."

It is not.

The important limitation is the direction of adaptation:

```text
human changes goal
       ↓
robot detects change
       ↓
robot adapts
```

The goal change is primarily treated as an **event to detect**.

It is not necessarily modeled as something the collaborative process itself generates.

---

# 6. Goal Recognition Is Not Goal Evolution

A large literature concerns **goal recognition**.

The basic structure is:

```text
observe behavior
      ↓
infer hidden goal
      ↓
adapt assistance
```

For example, human-robot collaboration research has demonstrated that inferring a human collaborator's goal from ongoing motion allows a robot to dynamically re-plan its own actions.

Recent work explicitly extends goal recognition toward dynamic environments in which goals can evolve over time.

This is important but conceptually different.

Goal recognition asks:

> **What is the human trying to achieve?**

The present hypothesis asks:

> **Can the interaction change what the human is trying to achieve?**

These are related but not equivalent problems.

---

# 7. Goal Negotiation Is Also Established

Human-agent collaboration research already includes explicit negotiation of goals.

Research on fluid human-agent collaboration notes that cooperative planning often requires explicit exchange and negotiation of goals.

However, the same work identifies an important distinction:

once a common goal is established, the system often treats that goal as fixed while dynamically adapting:

- roles;
- tasks;
- resources;
- assignments;
- plans.

The resulting structure is:

```text
NEGOTIATE GOAL
      ↓
FIX GOAL
      ↓
DYNAMICALLY ADAPT EXECUTION
```

This is different from:

```text
INITIAL GOAL
      ↓
EXECUTE
      ↓
LEARN
      ↓
REASSESS GOAL
      ↓
NEW GOAL
      ↓
EXECUTE
```

The distinction therefore remains relevant.

---

# 8. Fluid Collaboration

Recent work on "fluid human-agent collaboration" provides particularly strong prior art.

The proposed model allows the allocation of collaboration units to change continuously during an activity.

Assignments can change because:

- tasks arise unexpectedly;
- execution fails;
- resources change;
- existing assignments become problematic;
- agents self-assign tasks;
- environmental conditions change.

The team therefore continuously:

1. monitors the environment;
2. evaluates assignments;
3. evaluates performance;
4. performs coordination actions;
5. changes how work is divided.

This is very close to the adaptive pursuit concept at the **execution and agency-allocation level**.

But the model generally assumes a common high-level goal.

Thus:

> **Fluid adaptation of pursuit is established.**

The unresolved question is whether the *high-level goal itself* belongs inside the same adaptive loop.

---

# 9. Goals as First-Class Objects

A particularly important 2026 contribution is *Goals as First-Class Abstractions in Human-AI Collaboration*.

The authors argue that goals are central to human-AI collaboration but remain poorly represented in knowledge-work tools.

They identify problems including:

- implicit goals;
- unexpressed goals;
- confusion between goals and outputs;
- inadequate support for goal articulation;
- inadequate support for goal alignment;
- inadequate contextual use of goals.

They argue that goals should become first-class abstractions in collaborative systems.

This is highly relevant.

It means the research community is moving from:

> "The user gives the system a task."

toward:

> "The collaborative system needs an explicit representation of what the participants are actually trying to accomplish."

That is an important conceptual convergence with Threadwright.

But it still does not automatically establish the stronger proposition that:

> the goal representation itself should be continuously transformed by feedback from pursuing the goal.

That remains a separate question.

---

# 10. Just-In-Time Objectives

The most dangerous prior art found in this excavation is *Just-In-Time Objectives: A General Approach for Specialized AI Interactions*.

This work explicitly starts from the observation that:

> user objectives are in constant flux.

It proposes dynamically inducing objectives from observations of the user's task.

The objectives become:

- explicit;
- visible;
- modifiable;
- usable by downstream AI systems.

This is very close to:

```text
observe context
     ↓
infer objective
     ↓
represent objective
     ↓
adapt AI behavior
```

It therefore kills another naive formulation:

> "AI systems normally assume a fixed objective."

At least some current research is explicitly trying to solve the opposite problem.

However, the mechanism remains primarily:

> **infer/update objectives to better serve the user's evolving task.**

That is not necessarily the same as:

> **interaction itself changes the human's understanding of what is worth pursuing.**

That distinction remains alive.

---

# 11. Reframing

Human-AI co-creativity research provides another attack vector.

Work on human-AI co-creativity explicitly distinguishes:

- framing a problem;
- discovering that the frame is inadequate;
- reframing the problem.

This is extremely relevant.

The process can be:

```text
problem frame
     ↓
exploration
     ↓
discover frame inadequate
     ↓
reframe
     ↓
new exploration
```

This demonstrates that interaction can change the representation of the problem itself.

Therefore:

> **Problem reframing during human-AI interaction is established.**

This substantially weakens any claim that changing the object of pursuit through interaction is itself novel.

But "problem reframing" may still differ from "intent adaptation."

A frame answers:

> How should we understand the problem?

An intent answers:

> What are we trying to accomplish?

Changing one may cause changing the other, but they should not be conflated.

---

# 12. Sensemaking

The adjacent literature on collaborative causal sensemaking is even closer.

Recent work argues that effective human-AI decision making involves collaborative processes in which:

- mental models;
- goals;
- constraints;
- causal hypotheses

are continually **co-constructed, tested, and revised**.

This is almost a direct hit on the hypothesis.

The proposed framework treats human-AI collaboration as an ongoing cognitive process rather than a sequence of requests and outputs.

This means the following is already emerging explicitly:

```text
human + AI
    ↓
co-construct understanding
    ↓
test assumptions
    ↓
revise models
    ↓
revise goals / constraints
    ↓
continue decision process
```

This is extremely close to the conceptual territory being explored in RESEARCH-0005.

Therefore we should not claim that this pattern has been overlooked.

---

# 13. But There Is Still an Interesting Structural Distinction

The literature appears to contain several pieces:

```text
dynamic goals
goal recognition
goal negotiation
problem reframing
co-creative sensemaking
adaptive collaboration
agency allocation
co-learning
```

What is less obvious is whether there is a **single formal model** treating these as levels of one adaptive pursuit.

A possible hierarchy is:

```text
                    INTENT
                      │
                 "why / what"
                      │
                      ▼
                    GOAL
                      │
                 "desired state"
                      │
                      ▼
                   PURSUIT
                      │
                 "strategy / plan"
                      │
                      ▼
                  ACTIVITY
                      │
                 "what happens"
                      │
                      ▼
                OBSERVATION
                      │
                      ▼
                  LEARNING
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
    change pursuit          change intent
```

Existing research covers many edges.

The open question is whether the **whole hierarchy is treated as a coupled adaptive system**.

That is a much more defensible research question.

---

# 14. A Crucial Distinction: Change vs Learning

Another distinction emerges.

Suppose:

```text
human wants X
AI helps pursue X
human discovers X was wrong
human changes to Y
```

There are at least three possible interpretations.

### Interpretation A — external goal change

The human simply changed their mind.

The AI adapts.

### Interpretation B — learning

The human acquired information and consequently changed the goal.

### Interpretation C — collaborative adaptation

The interaction between human and AI generated information that caused the human's goal to change.

The third is the most interesting.

It makes the **interaction itself part of the causal pathway producing the new intent**.

---

# 15. The Stronger Candidate

The surviving hypothesis can therefore be reformulated:

> **A human-agent pursuit may be a coupled epistemic process in which pursuing an intention generates information that changes the participants' understanding of the problem and may consequently change the intention being pursued.**

This is stronger than "dynamic goals."

It says:

> **the pursuit is epistemically generative.**

The system does not merely execute an objective.

It can discover that:

- the objective was misunderstood;
- the problem was framed incorrectly;
- an assumed constraint is false;
- another opportunity is more valuable;
- the desired outcome should be changed;
- the original objective should be abandoned.

This is much closer to the user's actual Threadwright experience.

---

# 16. Why This Matters for Threadwright

The existing TW loop is:

```text
Intended Outcome
       ↓
Current State
       ↓
Consequential Gaps
       ↓
What must be learned,
decided, or changed?
       ↓
Activity
       ↓
Updated Artifact State
       ↓
Reassess
```

The research now suggests that `Reassess` may have at least two qualitatively different outputs:

```text
                    REASSESS
                   /        \
                  /          \
                 ▼            ▼
        pursue differently   pursue something different
             │                    │
        same intent          changed intent
```

The first is ordinary adaptive pursuit.

The second is **intent adaptation**.

But even this terminology may ultimately be wrong.

The important phenomenon is the transition:

> **knowledge generated during pursuit → revision of what should be pursued.**

---

# 17. The Proxy-Optimization Connection

This finding connects directly back to RESEARCH-0005's capability discussion.

If a system is optimized solely for:

> successful completion of the current objective

then changing the objective may look like failure.

For example:

```text
Objective: build feature X

AI:
  optimizes implementation
  → feature X completed

Human:
  discovers feature X was the wrong solution
```

A completion-oriented evaluation says:

> success.

A pursuit-oriented evaluation may say:

> failure — the system optimized the proxy.

But if the system discovers early enough that feature X should not exist, then:

```text
abandon X
     ↓
discover Y
     ↓
pursue Y
```

may be the **better outcome**.

This gives the adaptive-intent question a direct connection to the broader TW lens:

> **Do not optimize a local parameter when doing so destroys future options or the actual objective.**

---

# 18. This Also Explains Why "Reassess" Matters

Reassessment is therefore potentially more than:

> "Did the activity succeed?"

It can be:

> "Given what we now know, are we still pursuing the right thing?"

That produces a hierarchy:

```text
Level 0 — execution
Did the activity work?

Level 1 — strategy
Was the approach effective?

Level 2 — pursuit
Are we pursuing the right intermediate objective?

Level 3 — intent
Are we still trying to achieve the right outcome?

Level 4 — framing
Are we even understanding the problem correctly?
```

This hierarchy is **not yet a Threadwright model**.

It is a candidate analytical structure that should itself be attacked.

---

# 19. The Corpus Has Therefore Killed More Weak Claims

The following should now be considered eliminated:

### Killed hypothesis 6

> Human-agent systems generally assume fixed human goals.

**Too broad.**

Dynamic human goals and goal recognition are established research problems.

### Killed hypothesis 7

> Goal negotiation is absent from human-agent collaboration.

**False.**

Goal negotiation is established.

### Killed hypothesis 8

> Human-AI interaction can change the framing of a problem.

**False.**

Problem framing and reframing are established areas.

### Killed hypothesis 9

> Goals are not treated as explicit objects in human-AI collaboration research.

**Increasingly false.**

Recent work explicitly argues for goals as first-class abstractions.

### Killed hypothesis 10

> Human-AI systems do not model continuously changing objectives.

**False.**

Recent work explicitly addresses changing and just-in-time objectives.

---

# 20. What Survives

A much narrower question survives:

> **Can adaptive pursuit be modeled as a single coupled process in which feedback can change execution, strategy, agency allocation, problem representation, and intent?**

And an even sharper version:

> **What is the causal relationship between pursuing an objective and discovering that the objective itself should change?**

The second formulation is currently the strongest.

It is not a claim of novelty.

It is the next research target.

---

# 21. Current Conceptual Model

The strongest model produced by this excavation is currently:

```text
                     INTENT
                       │
                       ▼
                      GOAL
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
                    /     \
                   /       \
                  ▼         ▼
          adapt pursuit   revise framing
                  │         │
                  │         ▼
                  │       INTENT
                  │         │
                  └────┬────┘
                       ▼
                    PURSUIT
```

Agency allocation operates across the loop rather than at a single level.

The human and agent may each adapt.

This is now a **candidate model**, not doctrine.

---

# 22. Important New Observation

The literature search reveals an interesting terminology problem.

Different communities appear to describe overlapping phenomena using different vocabularies:

| Phenomenon | Possible vocabulary |
|---|---|
| Changing objective | dynamic goals |
| Inferring objective | goal recognition |
| Agreeing objective | goal negotiation |
| Changing problem interpretation | reframing |
| Jointly constructing meaning | sensemaking |
| Changing execution | adaptation |
| Changing responsibility | agency allocation |
| Changing collaboration structure | fluid collaboration |
| Learning through interaction | co-learning / co-adaptation |
| Updating AI objective from context | just-in-time objectives |

This suggests that the potential contribution may eventually be **integrative rather than terminological**.

But we are nowhere near earning that claim yet.

---

# 23. Current Assessment

### Eliminated

```text
adaptive collaboration              ✓ established
mutual adaptation                    ✓ established
dynamic agency                       ✓ established
dynamic goals                        ✓ established
goal recognition                     ✓ established
goal negotiation                     ✓ established
problem reframing                    ✓ established
co-creative sensemaking              ✓ established
changing human goals                 ✓ established
adaptive pursuit                     ✓ established
```

### Still interesting

```text
pursuit → knowledge → changed intent
```

More precisely:

```text
Does pursuing an intention constitute
an epistemic process capable of changing
the intention being pursued?
```

And beyond that:

```text
Can intent revision,
pursuit adaptation,
agency reallocation,
and learning
be represented as one coupled
human-agent control process?
```

---

# 24. Current Research Position

`004_adaptive_pursuit+intent.md` does **not** establish a novel research concept.

It establishes something more valuable:

> **The broad concept of adaptive pursuit with changing intent is already heavily populated by adjacent research.**

The investigation therefore moves one level deeper.

The potentially interesting phenomenon is not:

> "goals can change."

It is:

> **the pursuit of a goal can itself be a mechanism through which the goal becomes better understood, challenged, transformed, or abandoned.**

This places the question at the intersection of:

- adaptive human-agent collaboration;
- sensemaking;
- problem framing;
- goal dynamics;
- co-learning;
- agency;
- decision making;
- epistemic processes.

That intersection requires further investigation.

---

# 25. Next Attack

The next excavation should **not** search for more papers containing "adaptive pursuit."

That vocabulary is already too close to our own.

Instead, search the phenomenon through its causal structure:

> **Does acting toward an objective generate knowledge that causes the objective to change?**

Priority concepts:

1. interactive sensemaking;
2. problem formulation;
3. problem reframing;
4. exploratory search;
5. discovery-driven planning;
6. goal emergence;
7. goal evolution;
8. endogenously generated goals;
9. co-construction of objectives;
10. reflective decision making;
11. joint epistemic action;
12. inquiry-driven collaboration.

The next question is no longer:

> "Has somebody studied changing goals?"

They have.

It is:

> **Has somebody modeled the pursuit itself as the mechanism that produces the evidence for changing the goal?**

That is the next hole to drill.