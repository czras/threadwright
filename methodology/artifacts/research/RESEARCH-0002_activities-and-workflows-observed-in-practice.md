# RESEARCH-0002: Activities and Workflows Observed in Practice

**Status:** In Progress

## 1. Purpose

This research records concrete activities and workflows observed in real practice while developing and applying Threadwright.

The purpose is to gather evidence about the nature of useful work, Activities, Workflows, Context, Intent, verification, practitioner judgment, and agent participation without prematurely imposing a universal conceptual model.

The research deliberately favors observed practice over conceptual elegance.

---

## 2. Background

RESEARCH-0001 explored several foundational Threadwright concepts, including Intent, Activity, Workflow, Context, consequential gaps, delegation, security, reassessment, and stopping.

That research weakened several initial conceptual formulations, most notably the proposed definition of Activity used by CHANGE-0005.

ASSESSMENT-0011 subsequently concluded that CHANGE-0005 has value but cannot be applied fully based on the current evidence.

This research therefore changes emphasis from primarily conceptual exploration to observation of concrete work.

The central question is not:

> What should an Activity be?

but:

> What useful work are we actually observing, and what can those observations teach us?

---

## 3. Research Principles

The following principles guide this research:

- Observe real work before defining universal abstractions.
- Record concrete cases even when their conceptual classification is unclear.
- Preserve unsuccessful, rejected, and incomplete interpretations as evidence.
- Distinguish observations from hypotheses and conclusions.
- Treat practitioner judgment as a potential source of knowledge rather than merely an approval mechanism.
- Allow concepts to emerge from repeated evidence rather than from isolated examples.
- Avoid creating new artifact types, categories, or abstractions without sufficient evidence.

---

## 4. Observed Cases

### 4.1 Explore, Assess, and Decide a Methodology Change

A recurring workflow has emerged during Threadwright development itself.

A conceptual question is explored through discussion, attacks, examples, and counterexamples. The resulting material is captured as research. The research is then assessed against the current methodology. If the assessment identifies a sufficiently justified methodological change, a CHANGE artifact can be created.

Observed pattern:

```text
Exploration / Research
        ↓
Assessment
        ↓
Reassessment / Decision
        ↓
Change, if warranted
```

This is itself a concrete example of the methodology being applied to its own development.

The process also demonstrated that substantial exploratory work can accumulate before a durable Threadwright artifact is created. Recognizing this mismatch led to the creation of RESEARCH-0001 and subsequently RESEARCH-0002.

This suggests that research capture is not merely documentation after the fact; it can be part of maintaining a usable reasoning trail.

---

### 4.2 Transform a Meeting into Trustworthy Structured Knowledge

A concrete work need arose from a recorded meeting.

The practical input was the transcript automatically produced by Microsoft Teams from the recorded meeting video. The goal was to produce structured information that could be used by people who needed to understand the meeting without consuming the entire recording.

The observed transformation was:

```text
Recorded meeting video
        ↓
Teams-generated transcript
        ↓
Context-aware sanitization
        ↓
Structured compaction
        ↓
Executive summary
        ↓
Task list
        ↓
Human participant review
```

The sanitization stage can include dropping irrelevant conversation such as chit-chat and heuristically correcting transcription errors using contextual semantics.

The structured compaction attempts to preserve the substantive information from the meeting while making it easier to consume.

The executive summary and task list provide more immediately usable representations of the resulting knowledge.

The choice of transcript as the practical input is itself contextual. The company does not currently have suitable multimodal models available for this purpose, while Microsoft Teams already provides the video-to-transcript transformation.

This input choice has a known limitation: information conveyed through shared presentations, screens, diagrams, or other visual material may not be represented adequately in the transcript.

A possible future evolution is therefore to process the original video with a suitable multimodal model and treat visual material as an additional information source.

#### Verification

The review stage cannot be reduced to asking another model whether the result is correct.

The primary reviewers need to be humans who participated in the meeting because they possess contextual and semantic knowledge that may not be recoverable from the transcript itself.

Actual human review of this workflow has already produced important feedback, demonstrating that participant review is a meaningful source of correctness information.

A different model may provide supplementary checking, but it is not a substitute for participant review when correctness depends on meeting context unavailable in the processed representation.

This case therefore provides evidence that:

- useful work can transform one representation of knowledge into another;
- transformation can involve multiple intermediate activities;
- input selection is constrained by Context and available capabilities;
- verification requirements depend on what information may have been lost;
- human contextual knowledge can be essential to verification.

---

### 4.3 Create a Threadwright Implementation for a Specific Context

Another observed form of work is creating a concrete Threadwright implementation for a particular context.

The work involves understanding the target context, determining what parts of Threadwright are useful there, adapting the implementation to the available tools and constraints, and producing an operational implementation.

This is distinct from defining Threadwright itself.

The implementation is therefore evidence about how Threadwright is applied rather than evidence that its implementation structure should become part of the methodology's conceptual foundation.

---

### 4.4 Understand an Artifact System Instance

A recurring need is to understand the artifact system within which work is performed.

This is not limited to Threadwright artifacts.

For example, an organizational environment may contain:

- source code in repositories;
- product and work-management information in Jira;
- project-management information in Jira and other documents;
- documents and organizational knowledge in SharePoint;
- additional artifacts in Confluence;
- explicit identifiers and naming conventions in some systems;
- less structured information in others;
- semantic relationships between artifacts that are not explicitly recorded.

The task is therefore not simply locating files.

It may require understanding:

- what kinds of artifacts exist;
- where they are stored;
- how they are identified;
- how they relate;
- which relationships are explicit;
- which relationships are implicit;
- where important information is likely to be missing;
- how people actually use the system.

This provides evidence that **understanding Context and its artifact system can itself be useful work**.

It also demonstrates that an artifact system does not necessarily correspond to a single repository, tool, or technical boundary.

---

### 4.5 Efficiently Use an Artifact System

Understanding an artifact system and using it efficiently appear to be distinct forms of work.

Once an artifact system has been understood, another capability is needed to navigate it effectively.

Examples include:

- locating relevant information efficiently;
- identifying the correct source of truth;
- following relationships between artifacts;
- creating or updating artifacts in the appropriate system;
- applying local conventions;
- avoiding redundant or contradictory records.

The distinction is retained as an observation rather than being elevated to a canonical Threadwright category.

Further observation is needed to determine whether the two capabilities consistently require different knowledge, skills, or reasoning.

---

### 4.6 Review a Proposed Threadwright Change Implementation

Another observed activity is reviewing the implementation of a proposed Threadwright Change.

The implementation process can produce concrete outputs, review findings, and evidence about whether the intended methodological change was actually realized.

The review can therefore expose gaps between:

- the intended Change;
- its interpretation;
- its implementation;
- the resulting artifacts;
- and the behavior of the resulting methodology.

This provides another example of human judgment operating on the result of agent-assisted work.

---

### 4.7 Practitioner Domain Knowledge Changes the Pursuit

During implementation of the publishing process, the practitioner independently identified a security implication of demoting a file from public to private.

Removing the file from the current repository state is insufficient if the content has previously been committed to a public Git repository, because the content may remain accessible through repository history.

The implication is that a public-to-private transition can require history rewriting and subsequent verification rather than merely changing the current state.

The important observation is not the Git-specific solution itself.

The practitioner recognized a consequential property of the problem through prior domain experience.

The insight was not produced as a response to an explicit agent-generated question or verification request.

This provides direct evidence that:

> Practitioner domain knowledge can materially change the understanding of a problem and consequently change the required pursuit.

The practitioner therefore cannot be modeled merely as an approval or verification step.

Practitioner knowledge may enter the pursuit itself by:

- identifying previously unnoticed gaps;
- recognizing consequences;
- interpreting ambiguous situations;
- identifying relevant constraints;
- changing the understanding of what constitutes an adequate solution.

This observation is consistent with external product-development feedback that effective product work depends on human domain expertise and judgment that cannot simply be reduced to implementation execution.

The observation should not yet be generalized into a claim that such knowledge can never be reproduced by an agent. The current evidence establishes that, in observed practice, the practitioner possessed relevant knowledge that materially affected the pursuit and was not present in the agent's working representation.

---

### 4.8 Sinew: Domain Experience Before Judgment Delegation

The same observation creates a consequential implication for Sinew.

Sinew is intended to support decisions in a domain involving competing objectives, uncertain information, delayed effects, and substantial contextual variation.

Before attempting to encode, automate, or delegate meaningful judgment in that domain, the practitioner needs to gather domain experience and understand how good decisions are actually made.

The current implication is therefore:

> **Sinew should first gather domain experience and observe the practitioner's judgment process before attempting to represent or delegate that judgment.**

This is deliberately treated as a research implication rather than a settled product requirement.

The relevant questions include:

- What information does the practitioner actually use?
- Which signals matter?
- Which signals are misleading?
- What contextual knowledge changes interpretation?
- Which decisions are routine?
- Which decisions require judgment?
- What trade-offs are recognized implicitly?
- How does confidence change with new evidence?
- Which aspects of judgment can be made explicit?
- Which aspects depend on experience that is difficult to articulate?
- Which decisions, if any, can eventually be delegated safely?

Sinew can therefore serve as a concrete environment for investigating practitioner expertise rather than assuming that such expertise can be specified in advance.

---

## 5. Initial Cross-Case Comparison

| Observed case | Primary transformation / purpose | Important evidence |
|---|---|---|
| Explore, assess, decide methodology change | uncertainty → assessed methodological decision | research and assessment emerge from practice |
| Meeting → structured knowledge | raw representation → usable knowledge representation | contextual human verification is essential |
| Create TW implementation | methodology → context-specific implementation | implementation is context-dependent |
| Understand artifact system | fragmented information → usable system understanding | relationships may be implicit |
| Efficiently use artifact system | system understanding → effective action | understanding and usage may be distinct |
| Review TW implementation | implementation → evaluated result | practitioner judgment evaluates realization |
| Practitioner security insight | incomplete problem understanding → consequential gap identified | domain expertise can alter the pursuit |
| Sinew domain learning | experience → understanding of judgment | judgment should be observed before delegation |

No universal Activity taxonomy is inferred from this table.

---

## 6. Initial Patterns

Several patterns are beginning to emerge.

### 6.1 Context dependence

The same apparent action can require substantially different work depending on the Context.

Tools, available information, organizational conventions, permissions, domain knowledge, and security boundaries all affect what useful work is possible.

### 6.2 Composition

Observed useful work frequently consists of several transformations or activities composed together.

The boundaries between those activities are not necessarily intrinsic. They may depend on the abstraction level at which the work is being considered.

### 6.3 Transformation

Many observed cases involve some meaningful transformation:

- representations of knowledge;
- artifact state;
- understanding;
- decisions;
- capabilities;
- available actions.

However, the observations do not establish that every Activity should be defined strictly as artifact transformation.

### 6.4 Verification is risk-dependent

Verification requirements emerge from the consequences of being wrong and from what information may have been lost or misinterpreted.

The meeting case demonstrates that participant review may be necessary because the participants possess contextual knowledge unavailable in the processed representation.

### 6.5 Understanding can itself be useful work

Understanding an artifact system is not necessarily preliminary overhead.

When the system is complex or poorly structured, acquiring a usable model of it can directly enable subsequent work.

### 6.6 Understanding and efficient usage may differ

Knowing how an artifact system works does not necessarily imply being able to navigate and use it efficiently.

This distinction remains an observation requiring further evidence.

### 6.7 Practitioner expertise can alter the pursuit

The practitioner may contribute knowledge that changes problem understanding before implementation or verification occurs.

This means the practitioner is not merely an approval gate at the end of an agentic process.

The practitioner can contribute:

- domain knowledge;
- contextual knowledge;
- risk recognition;
- interpretation;
- judgment;
- previously acquired experience.

### 6.8 Agent capability does not eliminate the need to understand practitioner judgment

Increasing agent capability does not by itself establish that the agent understands the practitioner's domain or decision process.

Before delegating meaningful judgment, the relevant domain and judgment process may need to be observed and understood.

### 6.9 Conceptual explanations remain subordinate to observed practice

The research continues to favor explanations that account for observed work rather than forcing observed work into preselected conceptual categories.

---

## 7. Relationship to RESEARCH-0001

RESEARCH-0001 primarily attacked conceptual definitions.

RESEARCH-0002 extends that work by examining concrete instances of useful work.

This produces a deliberate shift:

```text
RESEARCH-0001
Conceptual exploration and stress testing
        ↓
ASSESSMENT-0011
Current conceptual assessment
        ↓
RESEARCH-0002
Observation of real work
        ↓
Future assessment
```

The purpose is not to replace conceptual reasoning with examples, but to provide stronger empirical grounding for subsequent conceptual reasoning.

---

## 8. Initial Hypotheses

The following hypotheses remain provisional.

### H1 — Useful work should be discovered from practice

A universal taxonomy of Activities may be less useful than a model capable of representing recurring patterns discovered through practice.

### H2 — Purpose can remain stable while implementation mechanism changes

The same useful outcome may be achieved manually, by an agent skill, through an API, by a workflow, or through another mechanism.

### H3 — Composition boundaries are abstraction-dependent

A piece of work represented as one Activity at one abstraction level may be represented as a Workflow at another.

### H4 — Verification requirements emerge from risk and Context

Verification should depend on what can go wrong, what information is available, and who possesses relevant knowledge.

### H5 — Context discovery can itself be useful work

Understanding available artifacts, systems, capabilities, constraints, and relationships can materially advance a pursuit.

### H6 — Efficient usage may require different capability from understanding

Understanding an artifact system does not necessarily imply efficient operation within it.

### H7 — Human contextual knowledge may be an essential verification resource

Some correctness judgments may depend on knowledge possessed by participants or practitioners that is not represented in the processed artifacts.

### H8 — Practitioner expertise may be part of pursuit rather than merely verification

Domain expertise can identify consequential gaps and change the solution space before implementation is complete.

### H9 — Judgment should be observed before it is delegated

Where a pursuit depends substantially on practitioner judgment, attempting to automate or delegate that judgment before understanding its inputs, trade-offs, and decision process may be premature.

### H10 — Conceptual explanations should remain subordinate to observed practice

Definitions should explain recurring observations rather than dictate what observations are allowed to count.

---

## 9. Questions for Further Observation

The following questions remain open.

### Activity

- What distinguishes an Activity from other useful work?
- Is Activity a fundamental concept or merely a useful abstraction?
- Is transformation fundamental, or is it only a common property?
- What is the relationship between an Activity and its representation?

### Intent

- How should implicit Intent be represented?
- How does Intent change during pursuit?
- How are competing or nested Intents represented?
- When does decomposition create useful subintents rather than implementation tasks?

### Workflow

- What makes a composition useful enough to be represented as a Workflow?
- When is Workflow merely an abstraction of Activities?
- Can useful Workflows emerge dynamically during pursuit?

### Context

- Which aspects of Context must be explicitly represented?
- Which can remain implicit?
- How much practitioner knowledge is part of Context?
- How does Context change during pursuit?

### Verification

- When is human verification essential?
- Which kinds of knowledge can agents reliably acquire?
- How should verification handle information unavailable to the agent?

### Practitioner expertise and judgment

- Which practitioner knowledge materially changes pursuit?
- Which knowledge can be represented explicitly?
- Which knowledge is acquired primarily through experience?
- How can an agent recognize that it lacks relevant domain knowledge?
- What evidence is sufficient before delegating a judgment?
- Can judgment be decomposed into parts that can safely be delegated?

### Sinew

- What domain experience is necessary before attempting meaningful decision support?
- How can the practitioner's decision process be observed without prematurely constraining it?
- Which signals actually influence decisions?
- Which trade-offs are explicit versus implicit?
- What should remain practitioner judgment even after substantial domain understanding has been accumulated?

---

## 10. Continuing Research

Further observations should be added to this research as they arise from actual work.

The research should preferentially capture:

1. concrete work that does not fit current concepts;
2. work that exposes consequential gaps;
3. work where practitioner judgment materially changes the pursuit;
4. work where agent capabilities or limitations become visible;
5. work where Context changes what is possible;
6. work where existing conceptual definitions fail to explain what happened.

No new canonical abstraction should be introduced merely because a single interesting case has been observed.

Repeated evidence should be allowed to accumulate before creating another methodological Change.

---

## 11. Current Position

The current evidence is insufficient to finalize a universal definition of Activity.

CHANGE-0005 therefore remains pending rather than being immediately replaced.

The current research direction is deliberately empirical:

> **Observe useful work in practice, capture the observations, and allow the conceptual model to emerge from repeated evidence.**

A particularly important emerging observation is that the practitioner is not simply an approval gate for agent-produced work.

The practitioner can contribute domain and contextual knowledge that changes the understanding of the problem, identifies consequential gaps, and alters the pursuit itself.

For Sinew, this currently implies that domain experience and the practitioner's judgment process should be understood through practice before meaningful judgment is attempted to be represented or delegated.

These conclusions remain provisional and should be tested through further observation.