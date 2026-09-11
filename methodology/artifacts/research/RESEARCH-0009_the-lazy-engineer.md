# RESEARCH-0009: The Lazy Engineer

## Research question

**Under what conditions does perceived unnecessary recurring work cause an engineer to redesign the work system rather than merely execute the work more efficiently?**

The provocative working label is **the lazy engineer**.

The research question is not whether such engineers are lazy.

It is whether a recognizable behavioral pattern exists beneath the label:

> An actor notices that recurring work consumes scarce cognitive and organizational capacity whose perceived value does not justify its cost, and responds by changing the production system—through elimination, automation, delegation, compression, or redesign—rather than merely improving execution of the existing task.

The investigation asks whether this pattern is already adequately explained by existing constructs such as proactive personality, personal initiative, taking charge, job crafting, Lean/Kaizen, problemistic search, induced innovation, or attention allocation.

---

## 1. The observation

A recurring engineering pattern is easy to describe colloquially:

> “I don't want to keep doing this shit.”

But that statement is ambiguous.

It can mean:

- I dislike effort.
- I am bored.
- I want autonomy.
- I am frustrated.
- I am perfectionistic.
- I want to work on more interesting things.
- I believe the task is unnecessary.
- I recognize a recurring cost that should be removed.
- I recognize that the organization is repeatedly spending scarce attention on something of insufficient value.

These are not equivalent.

The important distinction is therefore not **effort versus no effort**.

A person can willingly expend enormous effort when the effort produces valuable outcomes.

The stronger distinction is:

> **necessary effort versus unnecessary recurring effort.**

This immediately moves the problem from individual motivation toward production-system design.

---

# 2. The first hypothesis: “lazy engineer”

The folk hypothesis is:

> Engineers who automate, simplify, delete, or redesign annoying tasks are lazy.

This is attractive because the resulting behavior can look like avoidance.

Instead of repeatedly doing the task, the engineer spends time changing the system.

From a local perspective this can even look irrational:

> “Why did you spend three days automating something that takes fifteen minutes?”

But the calculation changes when recurrence is included.

If the task takes 15 minutes and occurs once, three days of automation may indeed be irrational.

If it occurs every day, for years, across many people, the economics are completely different.

The relevant quantity is not the cost of one execution.

It is the **future stream of executions**.

A rough representation is:

\[
C_{recurring}
=
frequency
\times
people
\times
duration
\times
recurrence\ horizon
\]

But even this understates the cost because cognitive work includes context acquisition, switching, coordination, reconstruction, and recovery.

Therefore:

\[
C_{system}
>
C_{visible\ execution}
\]

in many knowledge-work situations.

---

# 3. First attack: economics

The hypothesis is not economically novel in its basic structure.

### Induced innovation

The induced-innovation tradition argues that changes in relative factor prices can induce technological change biased toward saving relatively expensive factors. The foundational idea is associated with Hicks, and later work explicitly describes technical change as responding to relative factor scarcity and cost.

This provides an important analogy:

> expensive factor → incentive to develop a production method that uses less of it.

Our candidate mechanism simply moves the scarce factor inward:

> **scarce cognitive attention → incentive to redesign work so less unnecessary attention is consumed.**

The difference is important.

Cognitive attention may have no explicit market price.

An engineer's salary does not increase every time a five-minute recurring task becomes annoying.

Yet the opportunity cost can still be real.

The relevant "price" may therefore be an **internal shadow price of attention**.

---

# 4. The economic literature gets even closer

Gifford's 1992 paper *Allocation of Entrepreneurial Attention* explicitly models attention as a scarce resource allocated among competing uses.

More importantly, innovation can itself create additional activities competing for attention, meaning that the opportunity cost of attention is endogenous to the firm's evolution.

This is remarkably close to the present problem.

The engineer is not simply choosing:

> work or don't work.

They are choosing among:

> execute current task / investigate / automate / document / help colleague / improve architecture / create reusable knowledge / build an agent / eliminate the task.

Every intervention changes the future set of competing demands.

Therefore an important insight emerges:

> **Process improvement is itself an allocation decision over future attention.**

That is stronger than ordinary task efficiency.

---

# 5. Second attack: organizational attention

The Attention-Based View of the Firm is an even more direct hit.

Ocasio's central proposition is that organizational behavior results from how firms channel and distribute decision-makers' attention. Organizational rules, resources, and relationships determine which issues and answers reach which decision-makers through which communications and procedures.

Later work explicitly frames attention as central to organizational adaptation and change.

A 2026 formulation goes even further, describing attention as a bottleneck arising from limited information-processing capacity and emphasizing organizational structures that allocate attention to essential information.

Therefore:

> **Organizational throughput is partly a function of where the organization sends its finite cognitive processing capacity.**

This is strong support for the general mechanism.

But it also exposes a limitation.

The Attention-Based View primarily explains **where attention goes**.

Our observation concerns an actor who asks:

> **Why does the system require this attention expenditure at all?**

That is one level more reflexive.

The actor is not merely allocating attention.

They are attempting to **redesign the mechanism that allocates future attention**.

---

# 6. Third attack: personal initiative

Personal Initiative is an obvious competing explanation.

Frese and Fay define it as self-starting, proactive behavior that overcomes barriers in pursuit of goals. It includes information collection, planning, feedback, persistence, and changing the work situation.

This explains a large portion of the observed behavior.

Likewise, the broader proactive-behavior literature already distinguishes constructs including proactive personality, personal initiative, role-breadth self-efficacy, and taking charge.

Therefore:

> **The lazy engineer is not a newly discovered personality type.**

If the hypothesis claimed that some engineers simply take initiative to improve their work, it would be redundant.

The interesting question is instead:

> **What determines which recurring work becomes the target of that initiative?**

Personal initiative explains **the capacity to act**.

It does not by itself explain the **selection mechanism**.

---

# 7. Fourth attack: taking charge

Morrison and Phelps define taking charge as discretionary behavior intended to produce functional organizational change. Their study of 275 white-collar employees associated taking charge with felt responsibility, self-efficacy, and perceived top-management openness.

Again, substantial overlap exists.

The lazy engineer is clearly capable of taking charge.

But taking charge is broader.

It does not require the trigger to be:

> recurring low-value cognitive expenditure.

Therefore it remains a plausible **behavioral vehicle**, not a complete explanation.

---

# 8. Fifth attack: job crafting

Job crafting comes even closer.

Modern job-crafting research explicitly includes reducing or avoiding hindrance demands—tasks and conditions perceived as obstacles to work goals. A 2024 meta-analysis finds meaningful relationships between job crafting and job characteristics, although the effects of reducing hindrance demands are substantially less straightforward than resource crafting.

The strongest recent counterexample is a 2026 study of 81 employees working across multiple agile teams.

Employees used:

- task elimination,
- reduced task investment,
- uninterrupted time blocks

to protect themselves from demanding work.

But those strategies could **burden coworkers and slow team processes**.

This is an extremely important falsification result.

It kills:

> “Reducing my cognitive cost is good.”

That is **not** the surviving hypothesis.

The stronger hypothesis is:

> **Reduce unnecessary cognitive work at the relevant system boundary.**

This is a fundamentally different optimization target.

---

# 9. The system boundary matters

Consider two interventions.

### Intervention A

> “I don't want to attend this meeting, so I stop attending.”

My cognitive cost decreases.

The organization's cost may increase.

### Intervention B

> “This meeting exists because five people repeatedly reconstruct the same state. Let's create a durable representation and redesign the coordination mechanism.”

My cognitive cost may initially increase.

Collective cognitive cost decreases.

The second behavior is the phenomenon under investigation.

Therefore the optimization target is not:

\[
\min C_{individual}
\]

but something closer to:

\[
\min C_{unnecessary,\ collective}
\]

subject to maintaining or increasing system output.

---

# 10. Sixth attack: Lean and Kaizen

This nearly kills the hypothesis.

Lean has been explicitly concerned with identifying and eliminating waste for decades.

Knowledge-work adaptations make the cognitive component explicit: unnecessary memory and recall, information searching, awkward information handling, and other invisible forms of waste can consume productive capacity.

Kaizen similarly institutionalizes employee-driven continuous improvement.

Therefore:

> **“Notice recurring waste and redesign the process” is not novel.**

It would be intellectually dishonest to claim otherwise.

However, Lean/Kaizen also gives us something useful.

It shows that the phenomenon is not necessarily a personality quirk.

Organizations can deliberately create mechanisms that make:

> observe friction → identify cause → change process → learn

a normal part of work.

That turns our phenomenon from an individual characteristic into a **possible organizational capability**.

---

# 11. Seventh attack: organizational routines

Routine-dynamics research provides another established explanation.

Organizational routines are not necessarily static scripts. Research describes mechanisms through which routines can be modified, including adding, removing, or reinforcing paths in the pattern of activity.

Routine inertia can nevertheless slow organizational adaptation.

This fits the observation:

> recurring work creates persistence.

But the actor can become an endogenous source of routine change.

Again, the novelty cannot simply be:

> “people change routines.”

That is established.

The potentially interesting contribution is the **trigger**:

> perceived recurring attention expenditure whose value no longer justifies its system-level cost.

---

# 12. Eighth attack: cognition

The cognitive mechanism is also established.

Leroy's attention-residue experiments show that switching away from an unfinished task leaves residual attention that impairs subsequent task performance.

This gives empirical grounding to several engineering intuitions:

- context switching is costly;
- interruptions have hidden costs;
- WIP creates cognitive overhead;
- fragmented work can consume more than its visible execution time.

But again:

> attention residue explains **why fragmented work is expensive**.

It does not explain why someone chooses to redesign the work system.

That requires an additional behavioral mechanism.

---

# 13. The emerging model

The literature therefore suggests a multi-stage mechanism rather than a single construct.

### Stage 1 — Recurrence

A task occurs repeatedly.

### Stage 2 — Cost accumulation

Its visible execution cost accumulates.

### Stage 3 — Cognitive amplification

Context acquisition, switching, coordination, memory, and reconstruction increase its effective cost.

### Stage 4 — Value comparison

The actor compares perceived system value against recurring attention expenditure.

### Stage 5 — Discrepancy

A perceived mismatch emerges:

> **“Why are we repeatedly spending this much cognitive capacity on this?”**

### Stage 6 — Search

The actor searches for alternatives.

### Stage 7 — Intervention

Possible interventions include:

1. execute;
2. optimize execution;
3. automate;
4. delegate;
5. compress;
6. redesign;
7. eliminate the task;
8. eliminate the cause of the task.

### Stage 8 — Feedback

The resulting system is observed.

The actor updates their understanding of the work and the available capabilities.

This is therefore not merely proactive behavior.

It is potentially a **feedback-controlled work-redesign loop**.

---

# 14. The crucial distinction: execution optimization versus production-function redesign

This may be the most important surviving distinction.

### Local optimizer

> “How can I do this task faster?”

### System optimizer

> “Why does this task exist?”

### Higher-order system optimizer

> **“What system configuration would make this task unnecessary?”**

The first optimizes execution.

The second investigates process.

The third changes the production function.

This explains why seemingly absurd investments can be rational.

A three-day automation project for a fifteen-minute task is irrational **under a single-execution model**.

It may be highly rational under a lifetime-system model.

---

# 15. Collective attention changes the objective

The Wednesday example provides a naturalistic test case.

An individual engineer can spend a day doing little direct work while spending substantial attention:

- enabling QA;
- helping BAs;
- helping other developers;
- resolving dependencies;
- identifying blockers;
- routing work to DevOps.

Individual task completion may therefore be low.

Collective throughput may be high.

This suggests:

> **Individual utilization is not equivalent to organizational productivity.**

An actor may generate leverage by changing the productive state of other actors.

The relevant question becomes:

> **What did the system become capable of accomplishing because this person spent their attention there?**

That is fundamentally different from:

> “What did this person personally complete?”

---

# 16. Knowledge transformation is the same phenomenon

Consider meeting-transcript transformation.

One actor spends substantial attention converting a high-entropy event into a compact, reusable representation.

The result can then be consumed by many other actors.

The work is therefore not simply information summarization.

It is:

> **attention amortization.**

One cognitive expenditure produces a durable artifact that prevents repeated reconstruction by others.

The same structure appears in:

- documentation;
- reusable workflows;
- abstractions;
- automation;
- agent skills;
- architectural simplification;
- code deletion;
- process redesign.

The common mechanism is:

> **pay cognitive cost once to reduce future collective cognitive expenditure.**

---

# 17. Code deletion is the extreme case

Removing code is particularly revealing.

Adding an abstraction can reduce future work.

Automating a task can reduce future work.

Documenting a decision can reduce future reconstruction.

But deleting the unnecessary requirement removes the future work entirely.

This produces a hierarchy:

> **execute → optimize → automate → delegate → compress → redesign → eliminate**

The further down the hierarchy an intervention goes, the more it changes the future production system rather than merely improving current execution.

This is why:

> **“How can I make this task stop existing?”**

is a more powerful engineering question than:

> “How can I do this task faster?”

---

# 18. The latent-cost problem

A major component of the phenomenon is that organizational costs are frequently invisible at the point where they occur.

A task can appear to cost:

> 5 minutes.

But the actual system cost may include:

- finding context;
- remembering prior decisions;
- switching from another task;
- waiting for clarification;
- asking another person;
- restoring previous context;
- correcting misunderstandings;
- repeating the task across people;
- preserving the infrastructure required for the task.

Therefore the observable cost of a task can be dramatically smaller than its **lifecycle cognitive cost**.

This suggests a research construct worth investigating:

> **latent cognitive cost**

defined provisionally as cognitive and coordination expenditure that is causally attributable to a recurring work requirement but is not represented in the visible execution time of that work.

This is currently a **hypothesis**, not an established construct.

---

# 19. The role of agency

The same recurring cost does not produce the same response in every person.

Possible responses include:

> tolerate → complain → optimize locally → ask someone else → automate → redesign → eliminate.

This suggests at least two gates.

### Gate 1 — Perception

Does the actor recognize the recurring work as unnecessarily expensive?

### Gate 2 — Agency

Does the actor believe they can change the system?

Existing research strongly supports the importance of agency-related variables such as self-efficacy, felt responsibility, autonomy, and organizational openness.

Therefore the phenomenon is unlikely to be explained by cognitive cost alone.

A person can recognize waste and still lack:

- authority;
- capability;
- time;
- confidence;
- organizational support;
- knowledge of the causal structure.

---

# 20. The “lazy engineer” may therefore be an observer of production-system misfit

The provocative interpretation becomes:

> The so-called lazy engineer is not necessarily unwilling to work.

They may be unusually sensitive to:

> **mismatch between recurring cognitive expenditure and system value.**

This could produce a behavioral signature:

- high resistance to repetitive low-value work;
- strong interest in automation;
- strong interest in abstraction;
- preference for elimination over optimization;
- willingness to incur short-term cost for long-term savings;
- sensitivity to recurrence;
- sensitivity to cognitive switching;
- interest in system-level effects;
- willingness to intervene outside immediate task boundaries;
- tendency to create reusable mechanisms;
- preference for durable solutions over repeated execution.

But none of these characteristics individually establishes the phenomenon.

They are candidate observable consequences.

---

# 21. A crucial falsification

The strongest challenge is:

> **Perhaps there is no special phenomenon.**

Perhaps all observed behavior can be decomposed into:

\[
Proactivity
+
Autonomy
+
Self\ efficacy
+
Conscientiousness
+
Intrinsic\ motivation
+
Technical\ competence
\]

If these variables fully predict the behavior, the “lazy engineer” hypothesis adds no explanatory value.

That would be a successful falsification.

Therefore RESEARCH-0009 should not claim a new personality construct.

The more defensible candidate is a **mechanism**:

> perceived recurring system-level attention cost → problemistic search → work-system redesign.

---

# 22. Another falsification: local optimization

The 2026 job-crafting study provides the warning.

An actor may reduce their own workload while increasing collective workload.

Therefore:

> **individual cognitive efficiency ≠ organizational cognitive efficiency.**

This distinction is essential.

The research hypothesis should therefore evaluate interventions at the **system boundary appropriate to the outcome**, not at the individual boundary.

---

# 23. Another falsification: optimization can destroy slack

There is a second danger.

Slack is not simply waste.

Research on slack time shows that lower opportunity-cost time can enable innovation, including complex projects requiring coordination, while excessive slack can also produce resource misallocation.

Therefore an organization that eliminates every apparently unnecessary minute may destroy the capacity required for:

- experimentation;
- learning;
- reflection;
- innovation;
- recovery;
- unexpected problem solving.

So:

> **maximum utilization is not the objective.**

The objective is productive allocation of attention.

Sometimes the correct intervention is deliberately to preserve slack.

---

# 24. The strongest surviving formulation

After attacking the hypothesis through economics, organizational behavior, cognition, Lean, job crafting, and routine dynamics, the strongest formulation is:

> **Recurring work creates claims on scarce cognitive and organizational attention. When an actor perceives that the collective attention required by a recurring activity is disproportionate to its value, and possesses sufficient agency to intervene, that discrepancy may trigger problemistic search for a different production arrangement. The resulting intervention may optimize execution, automate, delegate, compress, redesign, or eliminate the activity.**

This is **not** a new theory of laziness.

It is a candidate synthesis of existing mechanisms.

---

# 25. What appears genuinely interesting

The literature already explains most components separately.

What appears less directly developed is the combination:

### 1. Attention as a scarce productive resource

Established in cognitive psychology and organizational attention theory.

### 2. Recurring work as a future claim on attention

Compatible with economics of entrepreneurial attention and induced innovation.

### 3. Perceived mismatch as a search trigger

Compatible with problemistic search and proactive work behavior.

### 4. System-level rather than individual optimization

Necessary to distinguish organizational leverage from job crafting that merely shifts costs.

### 5. Intervention choice

The actor chooses among execution, optimization, automation, delegation, compression, redesign, and elimination.

### 6. Feedback

The result changes the actor's knowledge of the system and the feasible set of future interventions.

The **combination** is the potentially interesting object.

---

# 26. Human-agent interaction changes the intervention space

This is where HAI enters.

Historically, changing the production system required substantial human cognitive investment.

An engineer had to:

- understand the workflow;
- acquire context;
- design automation;
- implement it;
- document it;
- maintain it.

Agents potentially alter the cost of those interventions.

The important claim is **not**:

> agents make engineers faster.

The stronger hypothesis is:

> **Agents reduce the cognitive and execution cost of changing the production system itself.**

That may shift the economic boundary between:

> “just do the task”

and

> “change the system.”

A process improvement that previously required too much engineering effort may become economically viable.

This is a major HAI research opportunity.

---

# 27. Capability boundaries become endogenous

Suppose:

> human capability = H  
> agent capability = A

The optimal division of cognitive work depends on the capability boundary.

But agent capability is not static.

A workflow is delegated.

The result is observed.

Trust changes.

The delegation boundary moves.

The resulting system produces new evidence.

The boundary moves again.

Therefore:

\[
Capability
\rightarrow
Allocation
\rightarrow
Outcome
\rightarrow
Learning
\rightarrow
Capability\ model
\rightarrow
Allocation
\]

This is an adaptive control loop over cognitive work.

The agent-assisted review experiment is an example.

The human does not merely become faster at reviewing.

The human changes from:

> reviewer

to:

> assessor / curator / governor of an agent performing the review activity.

The organizational capability boundary has moved.

---

# 28. Organizational leverage

This leads to a useful distinction.

### Individual productivity

> How much valuable work can one person produce?

### Team productivity

> How much valuable work can the team produce?

### Organizational leverage

> **How much additional productive capacity can one actor create by changing how other actors work?**

The third is the phenomenon underlying the Wednesday example.

A person can produce little direct artifact output while substantially increasing the productive state of the organization.

This is not reduced productivity.

It is a different **level of productivity**.

---

# 29. A candidate research construct

A provisional construct could be:

## Cognitive Work-System Leverage

> The capacity of an actor to increase durable system-level output by changing the allocation, transformation, preservation, or elimination of cognitive work across multiple actors.

This should **not** yet be treated as an established construct.

It is a research proposal.

Potential indicators might include:

- future work eliminated;
- repeated reconstruction avoided;
- blocked time removed;
- number of actors enabled;
- cycle time reduced;
- coordination overhead reduced;
- knowledge made reusable;
- attention redirected toward higher-value activities;
- durable process capability created.

A particularly interesting metric would be:

\[
\text{Attention Leverage}
=
\frac{\text{durable system value created}}
{\text{attention invested in intervention}}
\]

Again: **candidate metric, not validated measure.**

---

# 30. The real research question

The original question:

> “Why are some engineers lazy?”

is now clearly inadequate.

The stronger question is:

> **When does perceived unnecessary recurring cognitive work cause an actor to redesign the work system rather than optimize execution of the existing task?**

And the deeper organizational question is:

> **How can organizations systematically increase their ability to detect and eliminate unnecessary collective cognitive work without destroying useful slack, shifting costs to others, or over-optimizing the system?**

And with HAI:

> **How does increasing agent capability change the economic and cognitive boundary between executing work and redesigning the system that produces it?**

These are substantially stronger research questions than the original folk hypothesis.

---

# 31. Research propositions

The following are hypotheses for future empirical investigation, not established findings.

### P1 — Recurrence

The likelihood of process redesign increases with the recurrence and cumulative cost of an activity.

### P2 — Latent cost

The likelihood of redesign increases when actors perceive cognitive and coordination costs beyond visible execution time.

### P3 — Value mismatch

Redesign is more likely when perceived recurring attention cost exceeds perceived system value.

### P4 — Agency

The effect of perceived cost on redesign is moderated by autonomy, self-efficacy, felt responsibility, and organizational openness.

### P5 — System boundary

Actors whose objective function includes collective outcomes will select different interventions from actors optimizing only individual workload.

### P6 — Capability

Lowering the cost of intervention increases the probability that actors redesign rather than tolerate recurring work.

### P7 — Agentic discontinuity

Increasing agent capability may lower the threshold at which production-system redesign becomes economically rational.

### P8 — Feedback

Successful interventions change future attention allocation and therefore alter the opportunity structure for subsequent interventions.

---

# 32. What would kill RESEARCH-0009?

This research should be considered unsuccessful if evidence shows that:

1. The phenomenon is completely predicted by existing proactive-behavior constructs.
2. Perceived recurring cognitive cost has no independent relationship with redesign behavior.
3. Recurrence does not materially affect intervention choice.
4. System-level framing does not distinguish the behavior from individual job crafting.
5. Agents do not meaningfully alter the boundary between execution and redesign.
6. The proposed intervention hierarchy has no predictive value.
7. “Latent cognitive cost” cannot be operationalized reliably.
8. Interventions systematically fail to improve system-level outcomes.
9. Apparent high-leverage actors are merely high-performing individual contributors whose effects disappear when measured at system level.

Any of these outcomes would narrow or invalidate the proposed synthesis.

---

# 33. Current conclusion

The **lazy engineer** is almost certainly not a useful scientific construct.

But the behavior that inspired the label survives.

The evidence supports treating it as a potentially important intersection of:

> **attention scarcity + opportunity cost + proactive agency + problemistic search + routine change + process innovation + system-level optimization.**

The distinctive hypothesis is not:

> “Some people dislike work.”

It is:

> **Some actors appear unusually sensitive to recurring unnecessary claims on collective cognitive capacity and respond by changing the production system that creates those claims.**

This reframes “laziness” as a potentially misleading surface description of **system-level efficiency seeking**.

The strongest version is even more general:

> **The object of optimization is not effort. It is the allocation of scarce cognitive capacity to valuable outcomes.**

And therefore:

> **The highest-leverage intervention may not make a task cheaper. It may make the task cease to exist.**

---

# 34. Implication for Human-Agent Interaction

HAI provides a new experimental environment for this mechanism.

The key question is not:

> “How much faster can an agent perform a task?”

It is:

> **“How does increasing machine capability change the set of production systems humans consider worth building?”**

That is a much more consequential question.

If agents lower the cost of:

- context acquisition;
- analysis;
- documentation;
- automation;
- process modeling;
- routine execution;
- knowledge transformation;
- monitoring;
- assessment;

then they may make previously uneconomic forms of organizational redesign viable.

The resulting transformation could therefore be:

\[
\text{human task execution}
\rightarrow
\text{human-agent work allocation}
\rightarrow
\text{human-agent production-system redesign}
\]

The unit of analysis shifts from **AI-assisted task execution** toward **adaptive cognitive organization**.

---

# 35. Final synthesis

The original intuition was:

> “Innovation often begins when someone becomes unwilling to repeatedly pay a cost whose value they can no longer justify.”

RESEARCH-0009 does not establish this as a law.

But after attacking it from multiple disciplines, a defensible version survives:

> **When recurring work imposes a sufficiently salient mismatch between collective cognitive expenditure and perceived value, actors with sufficient agency may treat the mismatch as a production-system problem rather than an execution problem. This can induce search for ways to optimize, automate, delegate, compress, redesign, or eliminate the work.**

The interesting object is therefore not the lazy engineer.

It is the **actor who recognizes unnecessary cognitive expenditure as a signal about the design of the production system.**

And the organizational capability worth investigating is:

> **the ability to continuously detect, evaluate, and redesign the allocation of cognitive work across humans and agents.**

That is where the rabbit hole currently ends.

Or, more accurately:

**that's where RESEARCH-0009 stops being a rabbit hole and becomes a research program.**

## Sources

1. Ocasio, William. *Towards an Attention-Based View of the Firm*. Strategic Management Journal, 1997. [Publisher record](https://doi.org/10.1002/%28SICI%291097-0266%28199707%2918%3A1%2B%3C187%3A%3AAID-SMJ936%3E3.0.CO%3B2-K?utm_source=chatgpt.com)
2. Gifford, Sharon. *Allocation of Entrepreneurial Attention*. Journal of Economic Behavior & Organization, 1992. [Publisher record](https://www.sciencedirect.com/science/article/abs/pii/016726819290038D?utm_source=chatgpt.com)
3. Hicks/induced-innovation literature, summarized in *Induced Innovation and Marginal Cost of New Technology*. Economics Letters, 2009. [Publisher record](https://www.sciencedirect.com/science/article/abs/pii/S0165176509002079?utm_source=chatgpt.com)
4. Leibenstein, Harvey. *Organizational or Frictional Equilibria, X-Efficiency, and the Rate of Innovation*. Quarterly Journal of Economics, 1969. [Publisher record](https://academic.oup.com/qje/article-abstract/83/4/600/1896602?utm_source=chatgpt.com)
5. Frese, Michael & Fay, Doris. *Personal Initiative: An Active Performance Concept for Work in the 21st Century*. Research in Organizational Behavior, 2001. [Publisher record](https://doi.org/DOI%3A%2010.1016/S0191-3085%2801%2923005-6?utm_source=chatgpt.com)
6. Morrison, Elizabeth Wolfe & Phelps, Corey C. *Taking Charge at Work: Extrarole Efforts to Initiate Workplace Change*. Academy of Management Journal, 1999. [Publisher record](https://journals.aom.org/doi/abs/10.5465/257011?utm_source=chatgpt.com)
7. Leroy, Sophie. *Why Is It So Hard to Do My Work? The Challenge of Attention Residue When Switching Between Work Tasks*. Organizational Behavior and Human Decision Processes, 2009. [Publisher record](https://www.sciencedirect.com/science/article/pii/S0749597809000399?utm_source=chatgpt.com)
8. Holman et al. *Does Job Crafting Affect Employee Outcomes via Job Characteristics?* Journal of Occupational and Organizational Psychology, 2024. [Publisher record](https://doi.org/10.1111/JOOP.12450?utm_source=chatgpt.com)
9. Tenzer, Helene. *I Can't Split Myself in Two (or Five): Job Crafting in Highly Demanding and Interdependent Work Environments*. Journal of Organizational Behavior, 2026. [Publisher record](https://doi.org/10.1002/job.70072?utm_source=chatgpt.com)
10. Agrawal, Ajay; Catalini, Christian; Goldfarb, Avi; Luo, Hong. *Slack Time and Innovation*. Organization Science, 2018. [Publisher record](https://pubsonline.informs.org/doi/10.1287/orsc.2018.1215?utm_source=chatgpt.com)
11. Ocasio, William et al. *It's a Different World: A Dialog on the Attention-Based View in a Post-Chandlerian World*, 2023. [Publisher record](https://journals.sagepub.com/doi/10.1177/10564926221103484?utm_source=chatgpt.com)
12. Seidl et al. *Quality over Quantity of Attention! Towards a Qualitative Attention-Based View*. Journal of Management Studies, 2026. [Publisher record](https://onlinelibrary.wiley.com/doi/full/10.1111/joms.70143?utm_source=chatgpt.com)
13. Lean Enterprise Institute. *TPS Fundamentals in a Knowledge Work Environment*. [Knowledge-work discussion](https://www.lean.org/the-lean-post/articles/tps-fundamentals-in-a-knowledge-work-environment/?utm_source=chatgpt.com)
14. Pentland & Goh. *Organizational Routines and Organizational Change*. Oxford Handbook of Organizational Change and Innovation, 2021. [Publisher record](https://academic.oup.com/edited-volume/38627/chapter-abstract/335264216?utm_source=chatgpt.com)

**Status: RESEARCH-0009 — hypothesis survives, original label does not.**