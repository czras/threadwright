# SCENARIO-0010 — Multi-Change Interaction

## Situation

Two teams work on Change A, adding enterprise SSO, and Change B, adding fine-grained authorization. They initially appear independent.

A modification to the identity model for Change A affects assumptions in Change B.

## Application

```text
Change A
   ↓
Identity model
   ↓ affects
Authorization design
   ↓
Change B
```

The material change triggers reassessment. An invalid assumption is discovered, creating a new consequential gap and an appropriate activity.

## Demonstrates

The methodology does not require a global sequential workflow. Relationships and reassessment allow concurrent Changes to interact.

Efficient discovery of affected artifacts is an implementation concern, not a new methodological primitive.