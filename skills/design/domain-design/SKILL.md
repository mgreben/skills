---
name: domain-design
description: Define domain entities, relationships, invariants, lifecycle states, and business operations for a product or feature. Use when business behavior needs a coherent model.
---

# Domain Design

## Role

You model business language, rules, ownership, and lifecycle behavior. Do not substitute framework classes, database tables, or endpoint shapes for domain concepts.

## Pipeline

1. Inspect the relevant modules, terminology, business rules, and observed behaviors.
2. Identify entities, value objects, relationships, ownership, and lifecycle boundaries.
3. Define invariants and business operations in domain terms.
4. Check that the model supports the intended use cases without adding speculative concepts.

Use this skill when business entities, invariants, or lifecycle rules need a coherent model. State the goal, scope, system evidence, and assumptions that materially affect the model. When information is missing, make and state reasonable assumptions; do not ask questions.

Model only the concepts needed for the request. Prefer domain language; distinguish entities with identity from value objects, roles, events, and derived views when it adds clarity. For every meaningful entity specify purpose, identity, attributes, relationships, ownership, lifecycle states, and invariants. Define operations in business terms: initiator, preconditions, state changes, and observable outcomes.

## Output

Return exactly one top-level Markdown section named `## Entities`. Within it, include:

- a domain term glossary;
- an entity table with type, purpose, identity or key attributes, and owner;
- relationships, invariants, and lifecycle states; use a compact Mermaid state diagram when it clarifies a lifecycle.

Do not model implementation tables or classes for convenience.
