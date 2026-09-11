# RESEARCH-0007: Review Skill as a Bounded Implementation of Threadwright Methodology

## Status

Exploratory research

## Research question

Can an existing agent-assisted software engineering workflow provide a concrete, bounded implementation of Threadwright methodology?

More specifically:

> Does an agent-assisted PR review workflow exhibit the characteristic Threadwright pattern of reconstructing an evolving epistemic state from persistent evidence, generating and evaluating hypotheses, preserving uncertainty, and returning a compressed assessment to a human practitioner for judgement?

## Observation

An existing code-review skill was used to assess a pull request against its corresponding ticket.

The agent was given a simple instruction equivalent to:

> Review PR X versus ticket Y.

The agent independently attempted to acquire the evidence it considered necessary, including Git information and the relevant repository state. Environmental sandbox restrictions prevented some direct evidence acquisition, requiring the human practitioner to provide or expose the required evidence.

The resulting review did not merely produce a list of defects. It produced a structured assessment containing:

- a summary of the implementation;
- assessment of alignment with the ticket;
- potential issues with explicit reasoning;
- confirmed deviations, errors, or failures;
- unresolved questions requiring external clarification;
- positive highlights.

Importantly, some initially identified potential issues were subsequently reasoned through and determined **not to constitute actual problems**.

The agent therefore generated a relatively rich candidate space and subsequently compressed it through investigation and reasoning.

The human practitioner then performs a further compression: deciding which findings are actionable, which are non-issues, and which require additional knowledge or judgement.

## Interpretation

This workflow can be understood as a **bounded implementation of Threadwright methodology**.

It is bounded because:

- the activity is specifically software review;
- the intended outcome is represented by a ticket;
- the primary epistemic space is a software repository and associated change;
- the available agent capabilities are constrained by the execution environment;
- the human practitioner retains final judgement.

It should therefore not be treated as a generic implementation of Threadwright.

However, several structural characteristics correspond closely to the emerging Threadwright model.

### 1. Intent and artifact are explicitly related

The ticket provides an expression of intended change.

The PR represents an implemented change.

The review activity investigates the relationship between the two rather than merely inspecting the code in isolation.

This suggests:

> **review ≅ assessment**

where the congruence operator indicates structural similarity rather than identity.

### 2. The epistemic state is richer than the diff

The relevant evidence is not necessarily limited to changed source files.

The repository, tests, configuration, deployment artifacts, documentation, ticket, PR, and potentially external organizational knowledge may all contribute to understanding the current state.

Consequently, prematurely excluding artifact categories can itself create an epistemic blind spot.

The preferred strategy observed here is:

> **Generate broadly; compress deliberately.**

### 3. The agent can determine its own evidence requirements

The agent attempted to obtain Git information and other evidence without being explicitly instructed how to perform the investigation.

Where environmental constraints prevented access, the human supplied the missing evidence.

This separates:

- reasoning capability;
- evidence acquisition capability;
- environmental capability.

The limitation observed in the experiment was therefore not necessarily a reasoning limitation.

### 4. Candidate generation does not require premature certainty

The review generated potential concerns even when some were ultimately determined to be non-issues.

This is useful because the agent can explore a richer hypothesis space before compression.

The resulting process is approximately:

```text
evidence
    ↓
candidate concerns
    ↓
reasoning / investigation
    ↓
confirmed issues
non-issues
remaining uncertainty
external clarification
```

This is a concrete example of:

> **Generate broadly → compress deliberately.**

### 5. Uncertainty is preserved rather than artificially eliminated

At least one finding required clarification outside the available repository/ticket evidence.

The agent did not need to manufacture certainty.

Instead, the review surfaced the epistemic boundary:

> this cannot currently be determined from the available evidence.

This is an important property of an assessment-oriented agent.

### 6. Assessment is balanced rather than defect-oriented

The review explicitly includes **positive highlights**.

This has both epistemic and interactional value.

Epistemically, the assessment records evidence supporting the quality of the implementation rather than only evidence against it.

Interactionally, it avoids turning the review into an adversarial "what is wrong with this?" artifact.

The resulting human experience is closer to:

> what appears correct → what deserves attention → what remains uncertain

rather than:

> what is wrong.

This suggests that assessment quality includes not only analytical correctness but also the way the resulting knowledge is presented to the human practitioner.

## Relation to Threadwright

The observed workflow can be represented as:

```text
             intended outcome
                   │
                 ticket
                   │
                   ▼
persistent ──► epistemic state ◄── repository / PR / other evidence
knowledge          │
                   ▼
              agent pursuit
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
     findings   non-issues  uncertainty
        │          │          │
        └──────────┼──────────┘
                   ▼
              assessment
                   │
                   ▼
          human judgement
                   │
                   ▼
             next action
```

The agent does not replace the practitioner.

It expands the practitioner's accessible assessment space.

The practitioner remains responsible for interpreting significance, resolving organizational or domain ambiguity, and deciding what should happen next.

## Research significance

This observation provides an empirical example of Threadwright methodology operating inside an ordinary engineering workflow.

This is significant because the workflow was not originally constructed as a generic Threadwright demonstration.

The methodology is being **observed through an existing practical activity**.

This creates a potentially useful research strategy:

> Rather than defining Threadwright entirely top-down, identify naturally occurring bounded implementations, observe their common structure, and use those observations to refine the methodology.

The review skill is therefore the first observed **lab rat** in the Navitasoft laboratory.

Navitasoft can consequently be treated not merely as an organization in which Threadwright might eventually be applied, but as an environment in which human-agent interaction and Threadwright-like patterns can be empirically observed.

## Initial hypothesis

> Existing agent-assisted workflows may already contain bounded implementations of Threadwright methodology, even when they are not described using Threadwright terminology.

If this hypothesis holds across additional activities, Threadwright may be better understood not as a prescriptive workflow but as a **general pattern that can emerge within different bounded activities**.

## Open questions

1. Which parts of the review workflow are essential to its Threadwright-like behavior?
2. Which characteristics are specific to software review and therefore do not generalize?
3. Do similar patterns appear in requirements analysis, incident investigation, implementation planning, or organizational decision-making?
4. How should an agent request or acquire additional evidence without creating excessive human interaction overhead?
5. What is the appropriate boundary between agent exploration and human judgement?
6. Can the same generate-rich/compress-deliberately pattern be observed in other activities?
7. Does the quality of assessment improve when the agent is allowed to inspect the complete accessible epistemic state rather than a pre-filtered subset?
8. How does the interaction change when the relevant agents include multiple humans with different domain knowledge and organizational perspectives?

## Current conclusion

The review skill provides a concrete, bounded implementation of several emerging Threadwright principles.

It demonstrates that an agent can:

- pursue evidence rather than merely consume a pre-curated prompt;
- construct a richer assessment space;
- reason through candidate concerns;
- eliminate false concerns;
- identify confirmed deviations;
- preserve unresolved uncertainty;
- communicate positive evidence;
- and return a compressed assessment to a human practitioner.

The implementation is not generic Threadwright.

It is evidence that **Threadwright-like interaction patterns can exist inside practical agentic workflows**.

This makes it a useful first empirical case for studying what Threadwright actually is.