# RESEARCH-0006/006_epistemic-agency+capability.md

## 1. Status

Research artifact within RESEARCH-0006 — Human-Agent Interaction Corpus Reconstruction and Adversarial Review.

This artifact investigates the relationship between:

- epistemic agency;
- human capability;
- human-agent collaboration;
- cognitive offloading;
- learning;
- judgment;
- long-horizon capability development.

The investigation is motivated by the emerging engineering objective of designing human-agent systems that help individuals and organizations evolve knowledge and intent over extended periods.

This artifact does not assume that Threadwright terminology is correct.

---

# 2. Research Question

The initial research question is:

> **What scientific machinery already exists for describing and designing systems that use AI to augment knowledge work while preserving or developing the human's capacity to know, judge, learn, and decide?**

A sharper formulation is:

> **What happens to human epistemic agency and capability when an AI system participates continuously in the processes of inquiry, reasoning, evaluation, decision-making, and pursuit?**

Secondary questions:

1. What is epistemic agency?
2. How does it differ from general human agency?
3. How is epistemic agency developed?
4. Can epistemic agency be shared with AI?
5. Can AI strengthen epistemic agency?
6. Can AI substitute for the epistemic work through which capability develops?
7. What kinds of cognitive work can safely be delegated?
8. What kinds of work should remain actively practiced?
9. Can human-AI interaction be designed as a capability-development process rather than merely a performance-enhancement process?
10. How should these effects be evaluated over long time horizons?

---

# 3. Immediate Finding

The concept of **epistemic agency in AI-mediated interaction is already established and rapidly expanding**.

Recent work explicitly discusses:

- human epistemic agency;
- shared epistemic agency;
- epistemic co-agency;
- epistemic dependence;
- cognitive agency transfer;
- epistemic autonomy;
- AI-mediated knowledge construction;
- AI-supported capability development.

Therefore:

> **Epistemic agency is not a missing concept.**

The research branch has successfully located existing scientific machinery for an important part of the problem.

However, the literature also reveals a significant distinction between:

> **preserving human agency during an AI-assisted task**

and:

> **designing AI-assisted interaction so that the human's epistemic capability develops over repeated use.**

The second is less mature and more fragmented.

---

# 4. Epistemic Agency

Epistemic agency concerns the capacity to actively participate in the production, evaluation, revision, and use of knowledge.

This is broader than merely:

> "thinking critically about AI output."

It includes questions such as:

- What should I investigate?
- What evidence is relevant?
- What should count as sufficient evidence?
- Which claims should I accept?
- Which assumptions should I challenge?
- What remains uncertain?
- What should I do next?
- When should I revise my model?
- When should I abandon the current pursuit?
- Who or what should be trusted?
- Which conclusions am I willing to own?

This is strikingly close to the human responsibilities that have emerged repeatedly during RESEARCH-0005.

---

# 5. Epistemic Co-Agency

Wu et al. (2025) explicitly examine **shared epistemic agency between humans and generative AI**.

They argue that effective human-AI collaboration should preserve active human epistemic agency rather than reducing interaction to accepting AI outputs.

Their framework describes humans and AI as participating in knowledge-related and process-oriented activities including:

- setting goals;
- monitoring progress;
- identifying knowledge gaps;
- facilitating discussion;
- creating shared understanding;
- generating and negotiating ideas.

They emphasize that users should adopt adaptive epistemic stances toward AI rather than treating AI outputs as unquestionable knowledge.

This is a direct prior-art hit.

The idea:

> **human + AI jointly participate in knowledge construction**

is established.

---

# 6. Epistemic Agency Is More Than Critical Thinking

A 2026 framework on epistemic agency in AI-mediated knowledge building makes the distinction particularly explicit.

It describes epistemic agency as the capacity to coordinate a system involving:

- purpose;
- data sources;
- knowledge-building processes;
- uncertainty;
- evaluation;
- revision.

Importantly, the framework describes evaluation feeding back into **purpose**, meaning that epistemic agency includes deciding what constitutes a worthwhile goal and when the system should be revised.

This is extremely close to the loop investigated in 003–005.

The conceptual structure is approximately:

```text
PURPOSE
   ↓
SOURCE
   ↓
KNOWLEDGE PROCESS
   ↓
KNOWLEDGE
   ↓
EVALUATION
   ↓
REVISE PURPOSE
   ↓
...
```

Therefore:

> **The scientific literature already contains machinery in which knowledge production and purpose-setting form a feedback loop.**

---

# 7. The Critical Distinction: Agency vs Capability

However, epistemic agency and epistemic capability are not identical.

A person may retain agency while having poor capability.

For example:

```text
human:
"I will decide whether this AI answer is correct."

but:

human:
"does not possess enough domain knowledge
to evaluate the answer."
```

The person technically retains control.

But the epistemic process may still be weak.

Conversely, capability can grow through repeated practice:

```text
knowledge
   ↓
practice
   ↓
better judgment
   ↓
better inquiry
   ↓
better knowledge
   ↓
...
```

This suggests two separate objectives:

### Agency preservation

> The human remains responsible for and capable of governing the epistemic process.

### Capability development

> The human becomes progressively better at governing the epistemic process.

The second is substantially stronger.

---

# 8. Epistemic Dependence

A 2026 review of **epistemic dependence in AI-mediated learning** makes this distinction explicit.

The authors argue that the central issue is not simply whether learners rely on AI, but whether reliance:

> preserves or displaces the epistemic work through which judgment develops.

The review connects AI-mediated learning with:

- epistemic cognition;
- cognitive offloading;
- information behavior;
- epistemic authority;
- agency;
- over-reliance.

This provides strong theoretical support for the distinction between:

```text
AI performs epistemic work
```

and:

```text
AI supports the human
while the human develops epistemic capability.
```



This is highly relevant to the expertise-pipeline problem from RESEARCH-0005.

---

# 9. Cognitive Agency Transfer

An especially useful concept appears in recent work on cognitive offloading.

The authors distinguish **cognitive agency transfer** from trust.

Cognitive agency transfer means that the individual progressively transfers governance of the thinking process to AI:

- what information matters;
- how evidence should be evaluated;
- what conclusions should be drawn.

This is explicitly framed as:

> **relocation of cognitive governance — who steers the thinking process.**

Trust is different.

A person can trust AI while retaining cognitive governance, or distrust AI while still habitually deferring cognitive governance to it.

This is an extremely useful distinction.

It gives us a much sharper version of the earlier:

> "AI cannot be allowed to do everything."

The problem is not delegation itself.

The problem is:

> **Who governs the epistemic process?**

---

# 10. This Reframes Cognitive Offloading

The earlier RESEARCH-0005 formulation:

> offload cognitive overhead that is not itself consequential to the judgment being exercised

can now be examined using existing scientific vocabulary.

Instead of asking:

> Is cognitive work being offloaded?

we can ask:

> **Is epistemic governance being offloaded?**

This creates three possible states:

```text
A. Cognitive assistance

AI performs supporting work.
Human governs inquiry and judgment.

B. Cognitive delegation

AI performs substantial cognitive work.
Human remains responsible for evaluating it.

C. Cognitive agency transfer

AI increasingly governs:
what to investigate,
what matters,
how evidence is evaluated,
and what conclusion to pursue.
```

These are not equivalent.

This is potentially much more useful than the binary:

> human work vs AI work.

---

# 11. Capability-Aware Design

A 2026 HCI workshop explicitly frames this as a **capability-aware design problem**.

It argues that AI-supported work should be evaluated across:

- performance;
- agency;
- skills;

and across:

- short-term;
- medium-term;
- long-term

time horizons.

The workshop explicitly asks whether cognitive offloading can improve immediate performance while gradually reducing critical engagement, agency, or professional skill. It calls for longitudinal evaluation of human expertise and skill sustainability.

This is remarkably close to the engineering objective emerging from RESEARCH-0005.

The research community is therefore already moving toward:

```text
performance
    +
agency
    +
skill sustainability
    +
time
```

rather than measuring AI systems only by immediate task performance.

---

# 12. Long-Horizon Evaluation Is the Missing Dimension

This becomes particularly important.

Most conventional AI evaluations ask:

> Did the user perform better?

Capability-aware evaluation asks:

> Did the user become more capable?

Longitudinal capability-aware evaluation asks:

> **What happened to the user's capability after months or years of interaction?**

This gives us:

```text
SHORT TERM
performance

MEDIUM TERM
learning / adaptation

LONG TERM
capability trajectory
```

This is much closer to the actual engineering objective of a human-agent system intended to operate continuously over a person's or organization's evolving work.

---

# 13. Human-AI Collaboration as a Learnable Capability

A 2026 Academy of Management paper explicitly proposes treating **human-AI collaboration itself as a learnable capability**.

It identifies three broad components:

- task theory;
- coordination;
- evaluation and governance.

It also highlights the importance of:

- knowing when to rely on AI;
- knowing when to override it;
- calibration;
- disciplined updating;
- evaluating long-term effects on learning and professional capability.

The paper explicitly warns that short-term productivity gains can hide longer-term costs to learning, skill development, engagement, and professional voice.

This is another direct collision with RESEARCH-0005.

The notion:

> **humans need to learn how to work effectively with AI**

is established.

---

# 14. Training Humans to Know When to Engage

The HAI / human-agent teaming literature provides empirical support.

Lange et al. (2025) studied training humans to work with AI agents on a novel task.

Scaffolded training produced more robust human-agent teaming than self-paced learning.

Importantly, the timing of AI use mattered: knowing **when to engage the AI** had a particularly strong effect during high-stakes periods.

This suggests that human capability in an AI-mediated environment includes:

> **knowing when not to delegate.**

That is different from simply knowing how to use the tool.

---

# 15. National Academies: Human-AI Teams Require Training

The 2022 National Academies report *Human-AI Teaming: State-of-the-Art and Research Needs* makes a similar argument at system level.

It identifies the need for humans to develop:

- accurate mental models of AI behavior;
- appropriate trust;
- accurate decisions based on AI input;
- timely and appropriate control.

It explicitly argues that human-AI teams need training in both taskwork and teamwork.

The report also identifies long-term human-AI teaming, goal alignment, communication, coordination, and training as research needs.

Its training chapter emphasizes that human-AI training must include understanding:

1. one's role;
2. the AI teammate;
3. how to interact with it;
4. how to interact with human teammates.

It also identifies the need to continually reassess training because AI capabilities themselves change.

Thus:

> **Human capability for AI collaboration is already recognized as a trainable system property.**

---

# 16. But Training Is Not the Same as Development

This distinction matters.

Training generally asks:

> Can we teach the human to perform effectively in this human-AI configuration?

Capability development asks:

> **Does participation in the configuration make the human progressively better at the underlying activity?**

For example:

```text
TRAINING
learn when to call AI
learn how to prompt
learn how to evaluate output

CAPABILITY DEVELOPMENT
become better at:
  framing problems
  identifying uncertainty
  evaluating evidence
  recognizing failure
  deciding what matters
  deciding what to investigate
  revising assumptions
  knowing when to delegate
```

The second is closer to the original engineering ambition.

---

# 17. AI Can Strengthen Epistemic Agency

The literature is not uniformly pessimistic.

Wu et al. explicitly argue that AI can support active epistemic agency when interaction is designed around:

- inquiry;
- goal setting;
- monitoring;
- feedback;
- knowledge gaps;
- discussion;
- negotiation of ideas.

They describe a symbiotic relationship in which human and AI influence one another during knowledge construction.

Likewise, recent work on AI-driven adaptive feedback reports relationships among adaptive feedback, engagement, metacognition, epistemic agency, and performance.

Thus:

> AI assistance does not inherently imply epistemic agency loss.

The important variable is **how the interaction is designed and used**.

---

# 18. AI Can Also Substitute for Epistemic Development

The opposite evidence is equally important.

A study of AI assistance in peer feedback found a tendency for students to **rely on AI rather than learn from AI**, highlighting a potential reduction in student agency.

Recent educational work similarly identifies risks including:

- cognitive offloading;
- metacognitive disengagement;
- reduced epistemic agency;
- over-reliance.

Design proposals therefore increasingly emphasize:

- cognitive friction;
- evaluation;
- reflection;
- AI-free phases;
- provisional rather than authoritative AI roles.

So the outcome is not:

```text
AI → deskilling
```

nor:

```text
AI → upskilling
```

It is:

```text
AI interaction design
       +
human interaction behavior
       ↓
capability trajectory
```

That is a much more useful engineering model.

---

# 19. Epistemic Co-Agency Is Not Automatically Capability Development

The 2026 paper *Learning with machines: Toward a theory of epistemic co-agency* proposes an **Epistemic Entanglement Framework**.

It explicitly frames the desired interaction as humans reasoning:

> with, through, and against

generative systems.

It emphasizes:

- challenging assumptions;
- surfacing contradictions;
- maintaining epistemic responsibility;
- epistemic transformation rather than merely task efficiency.



This is very close to the thinking-companion interaction emerging in RESEARCH-0005.

But there is still a distinction:

> **A good interaction can preserve epistemic agency without necessarily producing long-term capability growth.**

That needs to be empirically established rather than assumed.

---

# 20. The Capability Trajectory

This suggests a new way to formulate the engineering objective.

Instead of:

```text
AI system
    ↓
task performance
```

consider:

```text
AI system
    ↓
interaction
    ↓
current performance
    ↓
learning
    ↓
capability state
    ↓
future performance
    ↓
new interaction
    ↓
...
```

The system therefore has **two coupled outputs**:

### Immediate output

> accomplishment of the current pursuit.

### Long-term output

> evolution of the human's capability to pursue future objectives.

This is very close to the proxy-optimization problem identified in RESEARCH-0005.

---

# 21. A Two-Objective System

The engineering problem can therefore be represented as:

```text
              HUMAN-AGENT SYSTEM
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
       CURRENT PURSUIT      HUMAN CAPABILITY
             │                   │
             ▼                   ▼
       task outcome         future capability
             │                   │
             └─────────┬─────────┘
                       ▼
                  NEXT PURSUIT
```

The system should not maximize current task performance independently of capability trajectory.

A pathological optimizer might produce:

```text
excellent current output
        +
decreasing human capability
```

A different pathological optimizer might produce:

```text
excellent human learning
        +
terrible current outcomes
```

The engineering challenge is therefore a **multi-horizon optimization problem**.

---

# 22. This Reframes the Expertise Pipeline

The earlier expertise pipeline:

```text
novice
  ↓
practice
  ↓
competence
  ↓
independent work
  ↓
expertise
  ↓
mentor
```

can now be interpreted as an epistemic-capability trajectory.

AI introduces another possible path:

```text
novice
  ↓
AI-assisted performance
  ↓
high output
  ↓
???
```

The missing variable is:

> **capability trajectory**

It can branch:

```text
             AI-assisted work
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
     substitution         capability
          │                development
          ▼                   │
      dependency              ▼
                           expertise
```

The key research problem is therefore not:

> "Does AI make people worse?"

It is:

> **Under what interaction conditions does AI assistance produce substitution versus capability development?**

---

# 23. This Connects Directly to the User/Agent Boundary

The earlier distinction:

> judgment-bearing vs judgment-supporting work

can now be expressed more scientifically.

Potentially:

```text
JUDGMENT-GOVERNING WORK
  deciding what matters
  choosing evidence
  evaluating claims
  deciding when uncertainty is acceptable
  selecting what to investigate
  revising goals
  taking epistemic responsibility

JUDGMENT-SUPPORTING WORK
  retrieval
  transformation
  synthesis
  drafting
  cross-referencing
  computation
  alternative generation
  structured comparison
```

This is not yet a universal division.

An AI can perform some judgment-like activities.

The important question is:

> **Which activities must remain practiced by the human if long-term human epistemic capability is itself an objective?**

That is a substantially stronger and more useful formulation than:

> "AI can't do judgment."

---

# 24. The Interesting Engineering Possibility

This suggests that a human-agent system could deliberately implement **capability-preserving interaction patterns**.

For example:

```text
AI:
"I found three plausible explanations."

Human:
"Which one do you think is strongest?"

AI:
"Before I answer, what evidence would distinguish them?"

Human:
"Let's investigate X."

AI:
"Here are the observations."

Human:
"Given this, I think hypothesis B is wrong."

AI:
"Agreed. What should we investigate next?"
```

The AI is not merely producing answers.

It is participating in a process that repeatedly exercises:

- hypothesis formation;
- evaluation;
- uncertainty management;
- investigation selection;
- revision;
- judgment.

Whether such interaction actually develops human capability is an empirical question.

But this gives us a concrete engineering target.

---

# 25. Thinking Companion Revisited

This gives a much stronger interpretation of the "thinking companion" idea.

A conventional AI assistant:

```text
human → request → AI → answer
```

A capability-oriented thinking companion:

```text
human ↔ AI
   ↓
joint inquiry
   ↓
challenge
   ↓
evidence
   ↓
reflection
   ↓
revised understanding
   ↓
next inquiry
```

The value is not merely the answer.

The value includes:

> **improvement of the human's ability to conduct the next inquiry.**

This is much closer to the actual engineering objective emerging from the research.

---

# 26. The Long-Horizon Dimension

The strongest remaining difference from ordinary AI-assistant design may therefore be **time**.

Most systems optimize:

```text
this interaction
```

Some optimize:

```text
this task
```

Capability-aware systems should consider:

```text
this task
      ↓
this learning episode
      ↓
this capability trajectory
      ↓
future tasks
      ↓
future capability
      ↓
future goals
```

This is the first point in RESEARCH-0006 where the **long-horizon** requirement appears as more than a generic aspiration.

It changes what the system should optimize.

---

# 27. The Organizational Extension

The same reasoning applies beyond individuals.

An organization has:

- collective knowledge;
- institutional memory;
- processes;
- decision patterns;
- expertise;
- coordination capability;
- strategic intent.

An AI system can optimize today's organizational work while potentially degrading tomorrow's organizational capability.

Therefore the system-level trajectory becomes:

```text
ORGANIZATION
     ↓
AI-mediated activity
     ↓
current outcome
     ↓
knowledge accumulation
     ↓
organizational capability
     ↓
future decisions
     ↓
future intent
```

This connects directly to the original engineering objective:

> **human-agentic systems that help individuals and organizations evolve knowledge and intent over long horizons.**

---

# 28. What the Corpus Has Killed

The drill eliminates several possible claims.

### Killed

> Epistemic agency is an undiscovered concept.

**False.**

It is well established and currently expanding rapidly in AI research.

> Human-AI collaboration can involve shared epistemic agency.

**Established.**

> AI can transfer cognitive governance away from the human.

**Established as an emerging construct.**

> AI can create deskilling / agency risks.

**Established concern.**

> Human-AI collaboration can be trained as a capability.

**Established research direction.**

> Long-term human-AI teaming requires capability and training considerations.

**Established.**

---

# 29. What Survives

The investigation leaves a much more engineering-oriented question:

> **Can human-agent systems be deliberately designed to optimize current task outcomes while simultaneously developing the human's future epistemic capability?**

And a stronger version:

> **What interaction mechanisms cause AI assistance to function as capability development rather than capability substitution?**

And an even broader system question:

> **Can a human-agent system maintain a long-horizon capability trajectory in which current work contributes to the human or organization's ability to pursue future knowledge and intent?**

These questions are not established as novel.

They are, however, substantially closer to the actual engineering objective.

---

# 30. Emerging Scientific Machinery

The corpus has now assembled a surprisingly coherent toolbox:

```text
EPISTEMIC AGENCY
    │
    │ governs
    ▼
INQUIRY / KNOWLEDGE CONSTRUCTION
    │
    │ produces
    ▼
KNOWLEDGE
    │
    │ changes
    ▼
UNDERSTANDING / CAPABILITY
    │
    ├──────────────► INTENT
    │
    └──────────────► PURSUIT
                         │
                         ▼
                      ACTION
                         │
                         ▼
                    CONSEQUENCE
                         │
                         └──────────► new knowledge
```

Around this loop:

```text
agency
cognitive offloading
metacognition
sensemaking
co-learning
goal revision
human-AI teaming
capability development
```

are already established scientific concepts.

This is increasingly looking less like a missing theory and more like a **composition problem**.

---

# 31. Composition May Be the Actual Engineering Problem

The research is beginning to suggest:

> The machinery may already exist, but it is distributed across multiple disciplines and optimized for different objectives.

For example:

| Discipline | Useful machinery |
|---|---|
| Cognitive science | epistemic action, cognitive offloading |
| Learning science | metacognition, capability development |
| HCI / HAI | interaction, agency, adaptation |
| Human-AI teaming | delegation, coordination, training |
| Design research | framing, reframing, reflective practice |
| Education | epistemic agency, learning-to-learn |
| Organizational science | capability, collective learning |
| Decision science | judgment, uncertainty, decision processes |

The engineering opportunity may therefore be:

> **compose existing scientific machinery into a practical long-horizon human-agent system.**

That would be entirely consistent with engineering rather than scientific novelty seeking.

---

# 32. This Changes the Research Objective

The research objective should therefore no longer be:

> Find a novel theory.

Instead:

> **Find the smallest sufficient set of established concepts and mechanisms needed to engineer the desired class of human-agent systems.**

Novelty is optional.

Scientific novelty becomes a possible by-product:

```text
find existing machinery
       ↓
compose it
       ↓
build system
       ↓
discover missing piece
       ↓
research novelty
```

Rather than:

```text
invent theory
       ↓
hope it works
       ↓
build system
```

This is a significantly better engineering strategy.

---

# 33. Current Position

`006_epistemic-agency+capability.md` substantially narrows the engineering problem.

The corpus already provides scientific machinery for:

- epistemic agency;
- shared epistemic agency;
- epistemic co-agency;
- cognitive agency transfer;
- cognitive offloading;
- capability-aware AI design;
- human-AI team training;
- adaptive epistemic interaction;
- long-horizon skill sustainability.

The remaining question is therefore not whether these concepts exist.

It is:

> **How can they be composed into an operational human-agent system whose objective includes both current effectiveness and long-term evolution of human or organizational capability?**

This is now the most promising engineering-oriented research question to emerge from RESEARCH-0006.

---

# 34. Candidate System Objective

A provisional formulation is:

> **Help a human or organization accomplish the current pursuit while improving its capacity to understand, evaluate, decide, learn, and pursue future objectives.**

This is intentionally not a Threadwright definition.

It is a candidate engineering objective against which existing scientific machinery can be assembled and tested.

---

# 35. Next Excavation

The next investigation should move from **epistemic agency** to **capability development mechanisms**.

Priority areas:

1. metacognitive regulation;
2. learning-to-learn;
3. deliberate practice;
4. expertise development;
5. scaffolding and fading;
6. cognitive apprenticeship;
7. adaptive tutoring;
8. human-AI skill transfer;
9. capability-aware interaction design;
10. organizational learning;
11. long-horizon human-AI collaboration;
12. evaluation of capability trajectories.

The key question is:

> **What interaction mechanisms have evidence of actually changing human capability over time, rather than merely preserving human agency during AI-assisted performance?**

That is the next drill.