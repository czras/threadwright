# RESEARCH-0001: Threadwright Conceptual Exploration

**Status:** In Progress  
**Type:** Research  
**Subject:** Threadwright conceptual foundations  
**Purpose:** Capture and compress the conceptual exploration, attacks, scenarios, observations, and unresolved questions that emerged while examining the foundations of Threadwright.

---

# 1. Purpose

This research records an extended conceptual exploration of Threadwright.

The purpose is not to establish a finished ontology or formal methodology. It is to preserve useful evidence generated while challenging candidate concepts and relationships.

The exploration focused primarily on:

- Intent
- Change
- Activity
- Workflow
- decomposition
- Context
- consequential gaps
- capability and delegation
- reassessment and stopping
- relationships between these concepts

The research deliberately used adversarial reasoning and concrete scenarios to challenge candidate formulations.

The resulting observations are therefore **research findings and candidates**, not automatically normative Threadwright principles.

---

# 2. Research Approach

The exploration followed a recurring pattern:

1. propose a conceptual formulation;
2. attack it with counterexamples and edge cases;
3. construct or recall concrete scenarios;
4. identify where the formulation breaks;
5. preserve what survives;
6. refine the candidate;
7. leave unresolved questions unresolved where evidence is insufficient.

The scenarios in this document are therefore not merely illustrative examples.

They function as **stress tests**.

A useful scenario is one that exposes a weakness in a candidate concept, distinguishes competing interpretations, or demonstrates that a seemingly obvious relationship is not universally valid.

The exploration also produced an important methodological observation:

> Extended conceptual exploration without producing a durable artifact is itself a process smell.

This research artifact exists partly because the exploration reached the point where preserving the evidence became more valuable than continuing to expand the conversation.

---

# 3. Intent

Intent emerged as a central concept.

An Intent can be messy:

- vague;
- incomplete;
- ambiguous;
- internally inconsistent;
- only partially articulated;
- subject to change;
- discovered through action rather than stated beforehand.

Intent represents what an actor is trying to accomplish, but it does not necessarily begin as a precise or formally stated desired outcome.

An Intent may:

- remain exploratory;
- be refined;
- be split into multiple Intents;
- be merged with another Intent;
- be deferred;
- be abandoned;
- become the basis of a Change;
- remain outside the current pursuit.

Importantly, not every Intent needs to become a Change.

A Jira ticket, request, conversation, observation, or rough idea can be treated as an Intent.

If the input already effectively specifies a Change, the refinement from Intent to Change may be close to a no-op.

---

# 4. Intent and Latent Intent

A recurring observation was that purposeful human action does not necessarily begin with an explicitly articulated Intent.

A person may act before being able to clearly explain why.

This led to a candidate axiom:

> **Actions undertaken by an actor are generally directed by one or more explicit or latent Intents.**

The wording deliberately avoids making a metaphysical claim about every possible human movement or reflex.

The important distinction is:

**Intent may pre-exist explicit articulation.**

Threadwright may therefore help an actor:

- surface an existing Intent;
- articulate it;
- scrutinize it;
- refine it;
- decompose it;
- decide whether to pursue it.

It does not necessarily create the Intent.

---

# 5. Intent Decomposition

An Intent does not necessarily map directly to one implementation path.

When the current Intent is not directly actionable in the current Context, it may be decomposed.

Decomposition can produce:

- smaller Intents;
- alternative approaches;
- dependencies;
- newly exposed gaps;
- future possibilities.

A key observation is that decomposition is **Context-dependent**.

The same Intent may be directly actionable in one Context while requiring decomposition in another.

For example:

```text
Intent
  │
  ├── directly actionable in Context A
  │
  └── requires decomposition in Context B
```

Decomposition should therefore not be confused with implementation task breakdown.

It is primarily about making pursuit actionable or understandable.

---

# 6. Current Pursuit and Deferred Intents

Decomposition can expose more possible pursuits than should be undertaken immediately.

A decision is therefore required about what is actually pursued now.

This produced an important distinction:

```text
Intent decomposition
        ↓
candidate subintents
        ↓
selection / judgment
        ↓
current pursuit
```

Subintents that are not selected for current pursuit do not necessarily disappear.

They can remain valid future Intents.

This prevents exploration from automatically becoming scope expansion.

A useful formulation is:

> **A discovered Intent can remain valid without becoming part of the current pursuit.**

This distinction becomes especially important when exploration reveals broader capabilities or future directions.

---

# 7. Change

Change remains a distinct concept from Intent.

An Intent describes what an actor is trying to accomplish.

A Change represents a deliberate commitment to alter something.

The exploration did not establish that every Intent should become a Change.

Instead, a pursuit may:

- remain exploratory;
- gather evidence;
- be decomposed;
- be redirected;
- be deferred;
- be abandoned;
- eventually produce a Change.

The relationship is therefore not:

```text
Intent → Change
```

as a mandatory lifecycle.

A more accurate current view is:

```text
Intent
  │
  ├── explore
  ├── refine
  ├── decompose
  ├── defer
  ├── abandon
  └── commit to Change
```

This remains a research observation rather than a finalized lifecycle model.

---

# 8. Activity

An earlier candidate formulation was:

> **Activity is a transformation of artifacts.**

This was attractive because it provided a concrete and operational interpretation of Activity.

However, several scenarios weakened a strict interpretation.

Activities may affect:

- knowledge;
- capabilities;
- relationships;
- physical reality;
- economic state;
- available choices;
- time;
- the state of an ongoing pursuit.

If “artifact” is interpreted narrowly, some meaningful Activities fall outside the definition.

If “artifact” is expanded until it includes every relevant form of state, the concept risks becoming so broad that the distinction loses explanatory value.

A broader candidate emerged:

> **Activity is an action undertaken by an actor in pursuit of one or more Intents, which may transform relevant state.**

Another candidate formulation was:

> **Activity is deliberate action undertaken to transform relevant state in pursuit of an Intent.**

Neither formulation has been established as final.

The important surviving observation is that Activity should not be inherently tied to:

- software;
- repositories;
- files;
- source code;
- automation;
- a particular execution mechanism.

---

# 9. Intent ↔ Activity

The exploration established a strong candidate relationship:

> **One Activity can pursue multiple Intents, and one Intent can be pursued through multiple Activities.**

The relationship is therefore potentially many-to-many.

```text
Intent A ─┐
Intent B ─┼──→ Activity X
Intent C ─┘

Intent A ──→ Activity Y
Intent A ──→ Activity Z
```

An Activity can also have different effects on different Intents.

It may:

- advance one;
- harm another;
- leave another unaffected;
- fail to advance any;
- create unintended consequences.

Therefore:

> **Intent explains why an Activity is undertaken; it does not guarantee the Activity's success.**

This distinction became important when considering optimization and competing objectives.

---

# 10. Competing Intents and Optimization

When one Activity is expected to advance multiple Intents, those Intents may conflict.

For example, an Activity may:

- improve one objective;
- worsen another;
- consume resources required by a third.

Selecting among possible Activities therefore becomes an optimization or trade-off problem.

This does not imply that Threadwright itself should become an optimization engine.

A more appropriate role is to help surface:

- competing Intents;
- relevant Context;
- consequential gaps;
- alternatives;
- trade-offs;
- uncertainty.

The practitioner remains responsible for consequential judgment.

---

# 11. Consequential Gaps

Not every gap matters.

A gap becomes consequential in relation to:

- the current Intent;
- the current Context;
- potential consequences;
- available alternatives;
- practitioner judgment.

A consequential gap may concern:

- missing knowledge;
- missing capability;
- missing verification;
- lack of tractability;
- an unresolved decision;
- insufficient authority;
- missing information;
- an unsuitable Context.

The categories themselves are not currently frozen.

A key observation is:

> **Threadwright should surface consequential gaps; it should not steal the practitioner's judgment.**

A gap does not prescribe its solution.

An agent may:

- investigate;
- propose alternatives;
- estimate consequences;
- test approaches;
- gather evidence.

The practitioner may then decide whether the gap is consequential and what response is justified.

---

# 12. Context

A current working formulation is:

> **Context is relevant operational state, knowledge, and capabilities in which pursuit occurs.**

Context may include:

- knowledge;
- capabilities;
- artifacts and artifact state;
- tools;
- skills;
- agents and subagents;
- permissions;
- delegated authority;
- constraints;
- external systems;
- resources;
- time;
- money;
- human availability;
- security boundaries;
- containment boundaries.

Context defines, among other things, what actions are currently possible.

Context is not necessarily equivalent to a repository or project boundary.

An artifact may simultaneously be:

- part of a repository;
- part of the operational Context.

For example:

- `package.json` can establish a project dependency;
- `opencode.json` can establish an operational capability outside the project repository.

Both can affect what an agent can do.

---

# 13. Context as Dynamic State

Context can itself be transformed during pursuit.

An Activity may change Context by:

- adding a capability;
- changing configuration;
- acquiring information;
- obtaining permission;
- changing an artifact;
- introducing a tool;
- changing resource availability.

An important distinction emerged between an artifact's state and its effective operational effect.

For example:

```text
modify configuration
        ↓
configuration artifact changed
        ↓
restart / reload
        ↓
effective Context changed
```

Thus, changing an artifact does not necessarily mean the corresponding Context has immediately changed.

Context should therefore be understood as dynamic rather than static background.

---

# 14. Capability, Delegation, and Security

The exploration distinguished several concepts that are easy to conflate:

### Technical capability

What an agent or system **can** do.

### Delegated capability

What the agent is **authorized or permitted** to do by the practitioner.

### External enforcement

What the surrounding environment technically prevents the agent from doing.

### Trust

What the practitioner believes the agent will or will not do.

These are different dimensions.

For example, a practitioner may allow an agent to:

- modify project files;
- run tests;
- troubleshoot implementation problems;

while not allowing it to:

- modify operational configuration;
- install host-level packages;
- cross a particular security boundary.

These boundaries may initially be maintained through practitioner judgment rather than technical enforcement.

A future sandbox may instead provide a hard security perimeter within which broader autonomy is acceptable.

This suggests an architectural distinction:

> **Threadwright governs pursuit, decomposition, scrutiny, judgment, and escalation; the execution environment enforces hard security constraints.**

Human intervention therefore need not occur after every consequential action.

It is primarily required where:

- delegated authority is exceeded;
- a consequential judgment is required;
- a hard boundary is approached;
- the practitioner must choose among materially different outcomes.

---

# 15. Workflow

The original candidate formulation was:

> **Workflow — purposeful composition of activities and workflows.**

This was heavily attacked.

Several weaknesses emerged.

A Workflow is not necessarily required for every Intent.

For example:

```text
Intent → Activity
```

may be sufficient for a small pursuit.

Likewise:

- multiple Activities do not automatically constitute a Workflow;
- decomposition does not automatically create a Workflow;
- selecting several subintents does not automatically create a Workflow;
- a Workflow need not be a predetermined execution plan.

A stronger surviving interpretation is:

> **Workflow is a useful abstraction for a purposeful composition of pursuit.**

A more specific candidate is:

> **Workflow is a selected/current composition of Activities and/or subintents being pursued toward an Intent.**

Neither formulation is canonical.

The current evidence suggests that Workflow may be a **derived abstraction rather than a fundamental Threadwright primitive**.

---

# 16. Abstraction Level and Workflow

A pursuit can be represented differently depending on abstraction level.

For example:

> Deploy Sinew

may be represented as a single Activity at one level.

At another level it may be expanded into:

```text
build
  ↓
test
  ↓
deploy
  ↓
verify
```

The same underlying pursuit can therefore be:

- an Activity at one level;
- a Workflow at another.

This weakens the idea that Activity and Workflow have universally fixed boundaries.

It also suggests that there may be no universally correct atomic Activity.

The useful abstraction depends partly on the purpose of the representation.

---

# 17. Reassessment and Stopping

A pursuit does not have to continue until every known gap is eliminated.

A practitioner may deliberately stop because:

- the remaining benefit is too small;
- further work costs too much;
- shipping now creates more value;
- learning from real use is more valuable;
- constraints have changed;
- another Intent has become more important.

This produced a strong observation:

> **The stopping condition is decided at reassessment.**

Stopping is therefore not intrinsic to Intent.

Nor does stopping require the elimination of all consequential gaps.

Reassessment may result in:

- continue;
- change approach;
- decompose differently;
- change Intent;
- change Context;
- relax requirements;
- defer;
- abandon;
- stop.

Reassessment may itself be understood as an Activity because it changes the state of the pursuit, but there is currently insufficient reason to make it a special first-class Activity type.

---

# 18. Feedback

Feedback appears throughout the pursuit rather than belonging to one isolated stage.

It may arise from:

- execution;
- observation;
- testing;
- user interaction;
- failures;
- new knowledge;
- Context changes;
- external events;
- reassessment.

Therefore feedback should not currently be elevated into a special universal mechanism.

A simpler observation is:

> **Pursuit continuously produces information that may alter subsequent judgment.**

This is one reason a Workflow should not necessarily be understood as a fixed predetermined sequence.

---

# 19. Scenario Catalogue and Stress Tests

The following scenarios were used during the research to challenge candidate concepts and relationships.

They are not merely illustrative examples. They functioned as **stress tests**: concrete situations were constructed or recalled to determine whether a proposed concept remained useful when applied outside the case from which it originated.

## 19.1 Starship Sinew

### Scenario

The desired product vision is a highly capable "Starship Sinew", but the practical objective is to ship an MVP within a constrained period and then learn from real use.

The original Intent can therefore expose multiple possible pursuits:

- ship an MVP now;
- gather feedback from using the MVP;
- eventually evolve the product toward the larger Starship vision.

### Candidate concept attacked

**Intent decomposition as task breakdown.**

### Stress test

If decomposition simply meant turning an Intent into implementation tasks, the future Starship evolution would naturally become part of the current implementation plan.

That is undesirable.

### Observation

Decomposition can instead expose **multiple subintents with different temporal or pursuit status**.

The current pursuit can contain:

- the MVP;
- feedback and learning;

while the larger Starship evolution remains a valid but deferred Intent.

Therefore:

> **Decomposition can preserve future Intents rather than turning every discovered requirement into current work.**

This also demonstrates that an Intent does not have to become a Change merely because it has been discovered.

---

## 19.2 Concrete Capability Revealing a Broader Capability

### Scenario

While pursuing a concrete capability needed for a current stakeholder or customer need, the work reveals that a broader, more reusable capability would be valuable in a wider context.

The broader capability is not necessary to satisfy the current need.

### Candidate concept attacked

**Intent decomposition and current-pursuit selection.**

### Stress test

A naive interpretation could turn the broader capability into additional implementation scope for the current Change.

That would unnecessarily expand the current pursuit.

### Observation

The practitioner can:

1. implement only what is necessary for the current capability;
2. recognize the broader capability as a separate Intent;
3. preserve that Intent for later reassessment;
4. keep it outside the current pursuit.

This demonstrates that decomposition can distinguish:

```text
current pursuit
        +
valid future Intents
```

rather than producing a single ever-expanding implementation plan.

---

## 19.3 Personal Site: Missing Rendered Content

### Scenario

An agent repeatedly produced changes to a personal website in which intended content was missing from the rendered result.

The agent inspected source code and could find no obvious problem, but the actual rendered output was not reliably verified.

### Candidate concept attacked

**Consequential gaps and solution selection.**

### Stress test

The obvious response might have been to prescribe a specific technology:

> "Use Playwright."

But the observed failure did not itself establish Playwright as the solution.

### Observation

The consequential gap was more fundamental:

> **There was no reliable mechanism for verifying that the rendered result preserved the intended content.**

Several possible solutions could address such a gap.

The agent could explore alternatives, while the practitioner selected the appropriate solution.

The resulting work also changed Context by adding the required project dependency and operational capability.

This demonstrates:

- a gap can be discovered through failed pursuit;
- the gap does not prescribe its solution;
- an agent can explore the solution space;
- practitioner judgment may select the response;
- resolving the gap may require changing Context.

---

## 19.4 NP-Hard Problem

### Scenario

Suppose an Intent requires solving a computationally difficult optimization problem.

The problem may be NP-hard.

### Candidate concept attacked

**Consequential gaps and practitioner judgment.**

### Stress test

A simplistic methodology might infer:

> NP-hard → impossible → abandon.

That is not justified.

### Observation

Computational intractability can itself be a consequential gap.

However, the existence of that gap does not determine the response.

Possible responses include:

- exact computation if tractable for the actual instance;
- approximation;
- heuristics;
- relaxing constraints;
- redefining the objective;
- accepting a good-enough solution;
- deferring;
- abandoning.

Threadwright can surface the constraint and its consequences, but should not automatically decide that exact optimization is required.

This reinforces:

> **Consequential gaps inform judgment rather than prescribe decisions.**

---

## 19.5 Going for a Run

### Scenario

A person says:

> "I'm going for a run."

The explicit statement does not necessarily contain a complete account of why the activity is being undertaken.

Possible Intents include:

- training for a race;
- improving fitness;
- enjoying nature;
- socializing;
- losing weight;
- maintaining a routine;
- maintaining an identity or lifestyle.

The person may be consciously aware of some of these and not others.

### Candidate concept attacked

**Intent as explicit input to Activity.**

### Stress test

If an Activity requires an explicitly articulated Intent, ordinary purposeful human behavior would frequently fall outside the model.

### Observation

Intent may be **latent or implicit**.

This supports the candidate axiom:

> **Actions undertaken by an actor are generally directed by one or more explicit or latent Intents.**

Threadwright therefore need not create Intent from nothing. It may instead help surface, articulate, scrutinize, or refine an Intent that already exists.

---

## 19.6 One Activity, Multiple Intents

### Scenario

The same run may simultaneously pursue:

```text
improve endurance performance
preserve health
enjoy nature
socialize
maintain fitness
```

### Candidate concept attacked

**One Intent → one Activity.**

### Stress test

A one-to-one relationship would require the run to be split into separate Activities merely because it serves multiple purposes.

That does not correspond to the actual situation.

### Observation

The relationship between Intent and Activity is potentially **many-to-many**.

```text
Intent A ─┐
Intent B ─┼──→ Activity
Intent C ─┤
Intent D ─┘

Intent A ──→ Activity X
Intent A ──→ Activity Y
```

---

## 19.7 Activity With Conflicting Effects

### Scenario

A hard training session may:

- advance the Intent of improving race performance;
- conflict with preserving health;
- conflict with recovering from previous training;
- consume time that could serve other Intents.

### Candidate concept attacked

**Activity as something that advances the intended outcome.**

### Stress test

If Activity were defined simply as work that advances "the" intended outcome, the model would have difficulty representing an Activity that advances one Intent while harming another.

### Observation

An Activity can have different effects on different Intents.

It may:

- advance some;
- harm others;
- fail to achieve its intended effect;
- produce unintended consequences.

Therefore:

> **Intent explains why an Activity is undertaken; it does not guarantee the Activity's success or desirability across all relevant Intents.**

---

## 19.8 Sinew as a Multi-Objective Pursuit

### Scenario

Sinew is intended to help a person navigate the competing objectives of:

- preserving health;
- improving endurance performance;

while operating within the changing constraints and uncertainty of everyday life.

The relevant Context can include training load, recovery, available time, work, life events, environmental conditions, measurements, and incomplete knowledge.

### Candidate concept attacked

**Pursuit as a simple linear progression toward one desired outcome.**

### Stress test

There is no single obvious action that maximizes all objectives.

A training session may improve performance while increasing health risk or consuming scarce recovery capacity.

Rest may protect health while reducing immediate training stimulus.

### Observation

Some pursuits are fundamentally **multi-objective optimization under uncertainty**.

Threadwright need not itself solve the optimization problem.

It may instead help make visible:

- competing Intents;
- relevant Context;
- consequential gaps;
- available alternatives;
- trade-offs;
- uncertainty.

The practitioner can then decide what to pursue.

Sinew therefore provides a particularly useful **stress test for Threadwright itself**.

---

## 19.9 Sending an Email

### Scenario

An actor needs to communicate information to another person.

The Activity may be:

> Send an email.

### Candidate concept attacked

**Activity as source-code or filesystem transformation.**

### Stress test

The useful result is not necessarily a changed software artifact.

The relevant transformation may instead be:

```text
recipient does not know X
        ↓
recipient receives X
```

### Observation

Meaningful Activities extend beyond software development and filesystem operations.

This weakens any definition that makes software artifacts a necessary property of Activity.

---

## 19.10 Buying a Computer

### Scenario

An actor decides that they need a computer and purchases one.

### Candidate concept attacked

**Activity as modification of digital artifacts.**

### Stress test

The important transformation occurs in the physical and economic world:

```text
money / purchase offer
        ↓
computer ownership
```

### Observation

Threadwright's notion of Activity cannot be inherently tied to repositories, files, or software.

This also reinforces that Context and artifacts may exist outside a repository boundary.

---

## 19.11 Waiting Until Tomorrow

### Scenario

An actor deliberately decides not to act now and waits until tomorrow.

### Candidate concept attacked

**Activity as artifact transformation.**

### Stress test

No obvious durable artifact needs to change.

The activity may instead alter:

- time;
- available information;
- future options;
- the Context in which the next decision will be made.

### Observation

This scenario weakens a strict interpretation of:

> **Activity = transformation of artifacts.**

It suggests that a broader notion of **relevant state transformation** may be more robust.

The scenario does not by itself establish the broader definition.

---

## 19.12 Deploy Sinew

### Scenario

At a high level:

> Deploy Sinew.

may be treated as one piece of useful work.

At a lower level, the same pursuit may be represented as:

```text
build
→ test
→ deploy
→ verify
```

### Candidate concept attacked

**Activity and Workflow as fundamentally distinct, universally atomic concepts.**

### Stress test

If Activity must be atomic and Workflow must be a composition of Activities, the boundary between the two becomes dependent on arbitrary granularity.

### Observation

The same pursuit can be represented as an Activity at one abstraction level and expanded into a Workflow at another.

Therefore there may be no universal atomic Activity.

Workflow consequently appears more useful as an **abstraction over a composition of pursuit** than as a fundamental execution primitive.

---

## 19.13 MVP Stopping Point

### Scenario

The practitioner wants the Starship version of Sinew, but deliberately stops at an MVP because further work has lower expected value than shipping, learning, earning, or otherwise progressing.

### Candidate concept attacked

**Completion as the natural stopping condition of pursuit.**

### Stress test

The MVP still contains known gaps.

Further action remains technically possible.

Nevertheless, stopping is rational.

### Observation

Stopping does not require eliminating all consequential gaps.

A stopping decision belongs to reassessment.

Reassessment can determine:

- continue;
- change approach;
- decompose differently;
- change Intent;
- change Context;
- relax requirements;
- defer;
- abandon;
- stop.

---

## 19.14 Deferred Broader Intent

### Scenario

A current pursuit exposes a potentially valuable future capability or direction, but pursuing it now would expand scope beyond what is currently justified.

### Candidate concept attacked

**Everything discovered during pursuit becomes part of the current Workflow.**

### Stress test

If discovery automatically expands the current pursuit, every exploration risks becoming an ever-growing project.

### Observation

A discovered Intent can remain outside the current pursuit while being preserved for future reassessment.

This reinforces the distinction between:

- what has been discovered;
- what is currently being pursued;
- what is deliberately deferred.

---

# 20. Cross-Scenario Findings

The scenarios collectively produced several recurring observations.

### Intent is not necessarily explicit

Intent may be latent and later articulated.

### Intent and Activity are not one-to-one

An Activity can serve multiple Intents, and an Intent can be pursued through multiple Activities.

### Activity does not imply success

An Activity can fail, produce unintended effects, or create trade-offs.

### Pursuit can be multi-objective

Competing Intents can make Activity selection an optimization problem.

### Discovery does not imply scope expansion

New Intents can be preserved without becoming part of the current pursuit.

### Context is active, not merely environmental

Context affects what can be done and can itself change during pursuit.

### Workflow is abstraction-dependent

What counts as an Activity or Workflow can depend on the level at which pursuit is represented.

### Reassessment is essential to bounded pursuit

Continuation is not the only valid outcome. Stopping, changing direction, and deferring are legitimate results of reassessment.

### Scenarios are methodological evidence

The value of these scenarios is not that they prove a universal ontology.

Their value is that they expose where a candidate formulation breaks, what survives the attack, and where further research is warranted.

---

# 21. Claims Weakened or Superseded

Several earlier formulations became weaker during the research.

## 21.1 "Activity is a transformation of artifacts"

**Status:** Weakened.

Useful as an intuition, but potentially too narrow.

Counterexamples include:

- waiting;
- communication;
- physical transactions;
- knowledge transformation;
- changes in available options.

A broader state-oriented formulation may survive better.

---

## 21.2 "Workflow is purposeful composition of Activities and Workflows"

**Status:** Weakened.

The formulation does not establish:

- when a Workflow is necessary;
- whether Workflow is fundamental;
- whether composition alone is sufficient;
- whether Workflows are predetermined;
- where Activity ends and Workflow begins.

Current evidence favors treating Workflow as a useful derived abstraction.

---

## 21.3 "Decomposition creates a Workflow"

**Status:** Rejected as too strong.

Decomposition may create candidate subintents without producing a Workflow.

A subsequent selection or structuring decision may result in a Workflow-like representation.

---

## 21.4 "Everything discovered becomes current work"

**Status:** Rejected.

Discovery can produce future Intents that are deliberately deferred.

---

## 21.5 "Stopping means all important gaps are resolved"

**Status:** Rejected.

Stopping can be a rational reassessment outcome even when:

- gaps remain;
- further action is possible;
- improvement is still possible.

---

# 22. Emerging Essence

A broad formulation emerged from the exploration:

> **Threadwright is about navigating purposeful change under uncertainty.**

This is currently an **emerging essence**, not a canonical definition.

"Navigating" is useful because pursuit may involve:

- no known route;
- changing terrain;
- changing Context;
- newly discovered knowledge;
- competing Intents;
- uncertainty;
- changing constraints;
- redirection;
- deferral;
- abandonment;
- stopping.

The phrase therefore appears to capture something that is present across the concepts without prematurely defining their exact relationships.

It should itself be attacked before being elevated into a foundation.

---

# 23. Sinew as a Stress Test

Sinew provides a particularly useful concrete stress test for Threadwright because it combines many of the difficult characteristics identified in this research.

Sinew involves:

- multiple competing Intents;
- uncertain causal relationships;
- incomplete and noisy information;
- changing Context;
- delayed effects;
- resource constraints;
- human judgment;
- trade-offs;
- the possibility of stopping before a theoretical optimum;
- continuous feedback.

Its core pursuit can be understood as navigating the tension between:

```text
preserve health
       ↕
improve endurance performance
       ↕
navigate real life
```

This makes Sinew more than an example.

It is a useful **adversarial test environment** for Threadwright concepts.

If a concept cannot represent Sinew without becoming artificially complicated, that is evidence against the concept.

If the concept naturally explains the situation while remaining useful outside Sinew, that is stronger evidence in its favor.

---

# 24. Research Process as Evidence

The research process itself produced evidence about Threadwright.

The exploration generated a large number of conceptual observations, counterexamples, and refinements before a durable artifact was created.

This exposed a practical failure mode:

> **Conceptual exploration can continue indefinitely while useful knowledge remains trapped in transient conversation.**

The appropriate response was not to prematurely design a complete documentation system.

Instead, the mismatch between the work being performed and the artifact being considered suggested the need for a Research artifact.

This supports an emerging distinction:

```text
Research
   ↓
capture and challenge hypotheses
   ↓
Assessment
   ↓
evaluate current understanding
   ↓
Reassessment / Decision
   ↓
Change?
```

This is an observation from the current development process, not yet a finalized artifact taxonomy.

---

# 25. Unresolved Questions

The research intentionally leaves several questions open.

## 25.1 What is the fundamental definition of Activity?

Candidates include:

- transformation of artifacts;
- deliberate action;
- action in pursuit of Intent;
- transformation of relevant state;
- some combination of these.

Further scenarios are needed.

---

## 25.2 Is Workflow fundamental?

Current evidence suggests that it may be a derived abstraction.

Further implementation experience should determine whether Threadwright actually requires Workflow as a first-class concept.

---

## 25.3 What exactly distinguishes Activity from Workflow?

The distinction may be primarily one of abstraction level rather than ontology.

This remains unresolved.

---

## 25.4 What is the precise relationship between Intent, pursuit, and Workflow?

Current evidence suggests:

```text
Intent
   ↓
possible decomposition
   ↓
selection / judgment
   ↓
current pursuit
   ↓
possibly represented as Workflow
```

But this relationship has not yet been formalized.

---

## 25.5 What constitutes a consequential gap?

The concept appears useful, but the methodology for identifying consequentiality remains open.

In particular:

- how much should be delegated to agents?
- when should evidence be sufficient?
- when should uncertainty trigger escalation?
- how should competing consequences be surfaced?

These should likely be developed empirically rather than defined prematurely.

---

## 25.6 Is reassessment a first-class concept?

Reassessment appears important enough to explain continuation, redirection, and stopping.

However, it is not yet clear whether it should become a formal Threadwright primitive or remain an ordinary Activity.

---

## 25.7 How should authority be represented?

The distinction between:

- capability;
- delegation;
- technical enforcement;
- trust

is clear enough to be useful.

The appropriate representation in Threadwright remains unresolved.

---

## 25.8 How much of Threadwright should be normative?

The exploration repeatedly exposed the danger of turning useful observations into rigid rules.

Further research should determine which principles genuinely improve pursuit and which merely make the methodology more elaborate.

---

# 26. Current Research Position

At the end of this research pass, the strongest observations are:

1. **Intent may be explicit or latent.**
2. **An actor may pursue multiple Intents simultaneously.**
3. **Intent and Activity have a many-to-many relationship.**
4. **An Activity does not guarantee advancement or success.**
5. **Activities can create trade-offs between Intents.**
6. **Intent decomposition can expose future Intents without expanding current scope.**
7. **Current pursuit requires judgment about what to pursue now.**
8. **Consequential gaps should be surfaced rather than automatically solved by methodology.**
9. **Agents can explore solution space while practitioners retain consequential judgment.**
10. **Context determines and changes the action space.**
11. **Capability, delegation, enforcement, and trust are distinct.**
12. **Workflow may be a derived abstraction rather than a fundamental primitive.**
13. **Activity and Workflow boundaries may depend on abstraction level.**
14. **Stopping is a reassessment decision and does not require eliminating all gaps.**
15. **Sinew provides a strong multi-objective, uncertainty-heavy stress test for Threadwright.**
16. **Research itself needs durable artifacts when conceptual exploration becomes substantial.**

These findings are sufficient to inform a subsequent Assessment, but not sufficient to claim that the Threadwright conceptual model is complete.

---

# 27. Suggested Next Step

The next step should not be to immediately formalize all surviving concepts into a complete ontology.

Instead:

1. preserve this research;
2. perform an Assessment against the accumulated evidence;
3. identify which concepts actually require methodological commitment;
4. identify which concepts should remain intentionally loose;
5. determine whether any existing or proposed Changes remain justified;
6. only then introduce or modify normative Threadwright foundations.

In particular, the pending refinement of Activity should remain open until the broader research is assessed.

The objective is not to produce the most elegant conceptual system.

The objective is to discover the **smallest set of useful abstractions that survives contact with real pursuit**.