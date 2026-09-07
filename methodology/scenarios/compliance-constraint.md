# Scenario — Compliance Constraint

## Situation

A product must legally log every transaction. The constraint is represented as an authoritative artifact. A proposed design does not log every transaction.

## Application

```text
Compliance constraint
        │
        └── constrains → Design
```

The conflict becomes a consequential gap. The design cannot legitimately be treated as compatible without resolving or otherwise accounting for the constraint.

Threadwright does not itself know what the law requires. That knowledge must enter the artifact state from an appropriate authority.

## Demonstrates

The methodology can reason with external constraints without pretending to generate domain truth.
