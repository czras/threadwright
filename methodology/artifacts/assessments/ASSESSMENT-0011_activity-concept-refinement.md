# ASSESSMENT-0011: Activity Concept Refinement

## Status

Draft

## Subject

Assessment of `CHANGE-0005: Refine the Activity Concept`

## Inputs

- `RESEARCH-0001: Threadwright Conceptual Exploration`
- `CHANGE-0005: Refine the Activity Concept`
- Current Threadwright conceptual model and implementation experience

---

# 1. Purpose

Assess whether `CHANGE-0005` remains a justified Threadwright methodology change after the conceptual exploration captured in `RESEARCH-0001`.

The assessment does not assume that the proposed Change should proceed.

The purpose is to determine:

1. which observations in `CHANGE-0005` remain supported;
2. which parts have been weakened or invalidated;
3. whether the proposed Activity definition remains appropriate;
4. whether the Change should proceed, be modified, deferred, or abandoned.

---

# 2. Original Change Intent

`CHANGE-0005` proposes refining Activity to:

> **Activity — a declaration of useful work to be performed in a particular context, intended to reduce a consequential gap or otherwise advance the intended outcome.**

The Change was motivated by the observation that Threadwright should provide an abstraction for useful work without prescribing a universal catalog of concrete activities or their implementations.

The proposed refinement therefore attempted to make four properties explicit:

- Activity is a declaration;
- Activity represents useful work;
- Activity is contextual;
- Activity is implementation-agnostic.

The Change also explicitly rejected introducing:

- a universal Activity catalog;
- a mandatory Activity document format;
- agent skills as the canonical implementation;
- a Workflow execution model;
- a new concept for protocols or operations.

---

# 3. Assessment Approach

The Change is assessed against the evidence produced during `RESEARCH-0001`.

Each major claim is examined independently.

The assessment distinguishes between:

- **supported observations** — evidence continues to support the claim;
- **weakened observations** — useful intuition remains, but the formulation is too strong;
- **unsupported claims** — the research does not provide sufficient evidence;
- **contradicted claims** — concrete scenarios demonstrate that the claim is unsuitable.

The objective is not to preserve the proposed wording.

The objective is to preserve the useful insight while removing unsupported conceptual commitments.

---

# 4. Assessment of "Activity Is a Declaration"

## Original claim

> An Activity is a declaration of useful work.

## Evidence

The research identified an important distinction between an Activity and its representation.

A practitioner or system may **declare**, describe, document, or otherwise represent an Activity.

However, the declaration itself may not be the Activity.

For example:

- "send this email" can be a declaration of an intended Activity;
- sending the email is the Activity;
- an Activity document can describe how an Activity is understood;
- an implementation can perform the Activity.

The declaration therefore appears to be a representation of an Activity rather than necessarily its fundamental nature.

## Assessment

**Weakened.**

The research does not support making "declaration" part of the fundamental definition of Activity.

The distinction between an Activity and representations or implementations remains useful, but it should not be encoded by defining Activity itself as a declaration.

---

# 5. Assessment of "Useful Work"

## Original claim

> An Activity is useful work.

## Evidence

The research established that Activity is related to Intent.

However, "useful" is not an intrinsic property of an Activity.

Whether an Activity is useful depends on:

- the Intent being pursued;
- the Context;
- competing Intents;
- consequences;
- available alternatives;
- practitioner judgment.

An Activity may be undertaken with a useful purpose and still:

- fail;
- produce unintended consequences;
- advance one Intent while harming another;
- turn out not to have been useful.

For example, a hard training session can advance an endurance-performance Intent while conflicting with a health-related Intent.

Similarly, an attempted verification mechanism may fail to provide the expected assurance.

## Assessment

**Weakened.**

"Useful" is valuable as a characterization of purposeful work, but it should not be treated as an intrinsic semantic property of Activity.

The relationship between Activity and usefulness is mediated by Intent and Context.

---

# 6. Assessment of "Intended to Reduce a Consequential Gap"

## Original claim

An Activity is intended to reduce a consequential gap.

## Evidence

The research identified consequential gaps as an important Threadwright concern.

However, Activities do not necessarily originate from an identified gap.

Examples include:

- going for a run;
- sending an email;
- buying a computer;
- waiting until tomorrow.

These may be purposeful Activities without requiring a previously identified consequential gap.

Furthermore, an Activity may reveal a consequential gap rather than reduce one.

An Activity may also be performed simply because the current Context makes it appropriate for an Intent.

## Assessment

**Unsupported as a universal property.**

Consequential gaps remain important to Threadwright, but they should not be embedded in the fundamental definition of Activity.

---

# 7. Assessment of "Otherwise Advance the Intended Outcome"

## Original claim

An Activity is intended to reduce a consequential gap or otherwise advance the intended outcome.

## Evidence

The research challenged the existence of a singular "intended outcome."

One Activity can pursue multiple Intents.

An Activity can:

- advance one Intent;
- harm another;
- have no meaningful effect on another;
- fail to produce its intended effect.

The research therefore supports a many-to-many relationship between Intent and Activity.

## Assessment

**Weakened.**

The relationship between Activity and Intent is fundamental to the current conceptual model, but the formulation should not assume:

- one Intent;
- one intended outcome;
- guaranteed advancement;
- uniformly positive effects.

A more robust formulation should allow an Activity to be undertaken in pursuit of one or more Intents without asserting its eventual effect.

---

# 8. Assessment of Context

## Original claim

Activities are meaningful within a particular Context.

## Evidence

This aspect survived the research strongly.

Context affects:

- what actions are possible;
- available capabilities;
- available knowledge;
- constraints;
- permissions;
- tools;
- resources;
- external systems;
- security boundaries.

The same apparent Activity can also have different significance or feasibility in different Contexts.

Context itself can change during pursuit.

## Assessment

**Supported.**

Context should remain an important part of understanding Activity.

However, the evidence does not require Activity to contain Context as part of its definition.

It is sufficient that Activity is interpreted and undertaken within Context.

---

# 9. Assessment of Implementation Agnosticism

## Original claim

An Activity should be independent of its implementation.

The same Activity may be performed by:

- a human;
- an agent;
- software;
- a workflow;
- another mechanism.

## Evidence

This survived the research.

The examples explored during the research repeatedly demonstrated that the underlying useful pursuit should not be confused with the mechanism used to perform it.

The personal-site example is particularly strong:

- the consequential gap was lack of reliable rendered-output verification;
- several solutions could address the gap;
- Playwright was selected as a contextual implementation choice.

Likewise, an Activity such as sending an email does not become a different conceptual Activity merely because it is performed manually or through an API.

## Assessment

**Supported.**

Implementation agnosticism is a valuable property of the Activity abstraction.

---

# 10. Assessment of a Universal Activity Catalog

## Original claim

Threadwright should not prescribe a universal catalog of domain-specific Activities.

## Evidence

The research provides no reason to introduce such a catalog.

Activities are highly dependent on:

- Intent;
- Context;
- abstraction level;
- available capabilities;
- domain.

The exploration also showed that apparently similar Activities may differ significantly in meaning depending on Context.

## Assessment

**Supported.**

No universal Activity catalog should be introduced as a consequence of this research.

---

# 11. Assessment of Activity Documents

## Original claim

An Activity may be documented as a reusable methodological artifact describing:

- purpose;
- inputs;
- outputs;
- constraints;
- completion criteria.

## Evidence

The research distinguishes Activities from representations of Activities.

An Activity document could therefore be useful.

However, the research did not establish that:

- Activity documents are universally necessary;
- they require a particular structure;
- they constitute a fundamental Threadwright artifact type.

## Assessment

**Potentially useful, but not justified as a methodological commitment.**

The possibility should remain open.

No mandatory Activity document format should be introduced by this Change.

---

# 12. Activity and Workflow

The original Change implicitly assumes that Activity is a fundamental abstraction that can subsequently be implemented through mechanisms such as Workflows.

The research weakened the conceptual distinction between Activity and Workflow.

A pursuit such as:

> Deploy Sinew

can be represented as an Activity at one abstraction level and expanded into:

```text
build
→ test
→ deploy
→ verify
```

at another.

This suggests that Workflow may be a derived abstraction over a composition of pursuit rather than a fundamentally different execution mechanism.

Therefore, defining Activity primarily by how it relates to implementation mechanisms or Workflows would be premature.

## Assessment

**Relationship unresolved.**

The Activity concept should not be refined in a way that prematurely commits Threadwright to a particular Workflow model.

---

# 13. Consolidated Findings

| CHANGE-0005 claim | Assessment |
|---|---|
| Activity is a declaration | Weakened |
| Activity represents useful work | Weakened |
| Activity reduces a consequential gap | Unsupported as universal |
| Activity advances an intended outcome | Weakened |
| Activity is Context-dependent | Supported |
| Activity is implementation-agnostic | Supported |
| Threadwright should avoid universal Activity catalogs | Supported |
| Activity documents may be useful | Potentially useful, not established |
| Activity remains fundamental | Not yet sufficiently established |
| Activity should be defined independently of implementation | Supported |

The central result is that **the proposed refinement does not survive intact**.

The research found a stronger foundation for the relationship between Activity, Intent, and Context than for the specific definition proposed by `CHANGE-0005`.

---

# 14. What Survives

The following ideas from `CHANGE-0005` should be preserved:

### 14.1 Implementation independence

An Activity should not be defined by the mechanism used to perform it.

### 14.2 Contextual interpretation

Activities should be understood in relation to the Context in which they are pursued.

### 14.3 No universal domain-specific catalog

Threadwright should not prescribe a universal set of concrete Activities.

### 14.4 Representation is separate from implementation

A description or declaration of an Activity may be useful without making that description the Activity itself.

### 14.5 No premature execution model

Activity should not be defined in terms of a specific Workflow or execution technology.

---

# 15. What Should Not Be Adopted

The following parts of `CHANGE-0005` should not be incorporated into the methodology in their current form:

> **"Activity is a declaration..."**

This conflates the Activity with its representation.

> **"...of useful work..."**

This treats usefulness as intrinsic when it depends on Intent, Context, and judgment.

> **"...intended to reduce a consequential gap..."**

This makes consequential gaps a universal prerequisite for Activity without sufficient evidence.

> **"...or otherwise advance the intended outcome."**

This implies a singular intended outcome and an advancement relationship that does not hold for all Activities.

---

# 16. Candidate Direction

The research suggests that future refinement should begin from the relationship between **Actor, Activity, Intent, and Context**, rather than from the notion of declaration.

A candidate direction is:

> **Activity — an action undertaken by an actor in pursuit of one or more Intents, within a Context.**

A related candidate is:

> **Activity — deliberate action undertaken to transform relevant state in pursuit of one or more Intents.**

These are **research candidates, not approved definitions**.

They should not be adopted merely because they appear cleaner.

In particular, further evidence is needed around:

- what constitutes an action;
- whether every Activity must transform state;
- whether "deliberate" is necessary;
- how Activities relate to observations and decisions;
- how abstraction level affects Activity identity;
- whether Activity is actually a fundamental Threadwright primitive.

---

# 17. Decision on CHANGE-0005

## Recommendation

**Do not implement CHANGE-0005 as currently proposed.**

The research demonstrates that the proposed definition is too specific in several important ways.

However, the underlying motivation remains valid.

The Change identified a real need to clarify that:

- Activities are not implementations;
- Activities are contextual;
- Threadwright should not prescribe a universal activity catalog.

The appropriate response is therefore **not to abandon the problem**, but to reject the current formulation as the solution.

### Recommended disposition

**Defer / supersede the current formulation pending a more fundamental Activity assessment.**

The existing `CHANGE-0005` should remain preserved as historical evidence of the earlier hypothesis.

It should not be silently rewritten to make it appear that the original hypothesis was never made.

If the Threadwright process requires an explicit disposition of the proposed Change, it should subsequently be marked **Abandoned** or otherwise closed with a reference to this Assessment and the resulting future Change, if one is created.

---

# 18. Recommended Follow-up

No immediate replacement Change should be created solely from this Assessment.

The evidence is sufficient to reject the current formulation, but not sufficient to establish a definitive replacement.

The recommended sequence is:

```text
RESEARCH-0001
     ↓
ASSESSMENT-0011
     ↓
reject current Activity formulation
     ↓
retain surviving observations
     ↓
gather further evidence
     ↓
future Activity refinement Change?
```

Further evidence should preferably come from **using Threadwright**, rather than extending conceptual discussion indefinitely.

Particular attention should be paid to real Activities encountered during:

- Threadwright implementation;
- Sinew development;
- methodology change reviews;
- agent-assisted work;
- ordinary human work outside software development.

The objective should be to discover whether a stable Activity abstraction is actually necessary and, if so, what minimum definition is useful.

---

# 19. Assessment Conclusion

`CHANGE-0005` was directionally correct about an important concern:

> Threadwright should describe useful work without prescribing how that work is implemented.

However, the proposed definition:

> **Activity — a declaration of useful work to be performed in a particular context, intended to reduce a consequential gap or otherwise advance the intended outcome.**

does not survive the evidence gathered in `RESEARCH-0001`.

The strongest surviving properties are:

- Activity is related to Intent;
- Activity occurs within Context;
- Activity is independent of implementation mechanism;
- concrete Activities are context-dependent;
- Activity does not require a universal catalog;
- consequential gaps are relevant to some Activities but are not intrinsic to Activity itself.

The fundamental nature of Activity remains unresolved.

Therefore:

> **Do not implement CHANGE-0005 as written. Preserve its useful observations, reject its proposed definition, and defer a replacement until further evidence justifies one.**

This is a successful research outcome even though the proposed Change does not survive.

The purpose of the assessment is not to make every Change succeed.

It is to prevent Threadwright from committing to concepts that have not survived contact with evidence.