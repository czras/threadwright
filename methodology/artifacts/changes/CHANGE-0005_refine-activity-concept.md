# CHANGE-0005: Refine the Activity Concept

## Status

Pending

## Summary

Refine the fundamental Threadwright concept of **Activity** to explicitly define an Activity as a declaration of useful work in a particular context.

The existing concept describes Activity primarily in terms of work performed to reduce consequential gaps or advance an intended outcome. The refinement makes explicit that an Activity is a **declaration of useful work**, while its concrete implementation remains context-dependent.

## Motivation

While defining a reusable methodology change review, it became apparent that the review itself is a domain-specific Activity rather than an instance of a universal Threadwright "Review" operation.

This exposed an important property of the Activity abstraction:

> Threadwright provides the abstraction for declaring useful work; it does not prescribe a universal set of activities.

An Activity therefore needs to be understood independently from the mechanism used to perform it.

A single Activity may be implemented by:

- a human using a manual or how-to;
- an agent using a skill;
- a software system through an API;
- a workflow combining multiple actors or mechanisms;
- another implementation appropriate to the context.

The implementation is therefore not part of the fundamental Activity concept.

## Conceptual Change

Refine the definition of Activity to:

> **Activity** — a declaration of useful work to be performed in a particular context, intended to reduce a consequential gap or otherwise advance the intended outcome.

This preserves the existing relationship between Activity, consequential gaps, and intended outcomes while making two properties explicit:

1. **Declaration** — an Activity describes useful work rather than prescribing its implementation.
2. **Context** — an Activity has meaning within the domain or situation in which the useful work is defined.

## Consequences

### Activity remains a fundamental concept

No new fundamental concept is introduced.

The refinement extends the existing Activity concept rather than creating a separate concept for activity definitions, operations, or protocols.

### Activities are context-specific

Threadwright does not prescribe a universal taxonomy of Activities.

Concrete Activities may be defined by the context in which Threadwright is applied.

For example, "Methodology Change Review" is an Activity within the context of evolving the Threadwright methodology. It should not be interpreted as a universal Threadwright Review activity.

### Implementations remain outside the abstraction

The Activity declaration remains implementation-agnostic.

Its implementation may take different forms depending on the context and available capabilities.

This preserves Threadwright's implementation-agnostic nature.

### Activity documents become valid methodological artifacts

An Activity may be documented as a reusable declaration of useful work.

Such a document describes the Activity's purpose, inputs, outputs, constraints, and completion criteria without prescribing a particular implementation.

An implementation such as a human manual, agent skill, API integration, or workflow can subsequently be derived from the Activity declaration.

## Required Changes

Update the Activity definition in the Threadwright methodology to incorporate the refined definition.

No change is required to the fundamental concept taxonomy.

The existing Activity concept remains the abstraction; this change clarifies its semantics and its relationship to implementations.

## Boundary

This change does **not** establish:

- a universal catalog of Activities;
- a mandatory Activity document format;
- agent skills as the canonical implementation of Activities;
- a workflow model for executing Activities;
- a new methodological category for protocols or operations.

Those may be developed in concrete contexts if experience demonstrates a need for them.

## Success Criteria

The resulting methodology should make clear that:

- an Activity is a declaration of useful work;
- Activities are meaningful within a particular context;
- Activities are not implementations;
- multiple implementation mechanisms may satisfy the same Activity;
- Threadwright does not prescribe a universal set of domain-specific Activities;
- Activity remains one of Threadwright's fundamental concepts.