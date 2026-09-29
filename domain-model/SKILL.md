---
name: domain-model
description: Define the domain entities, relationships, invariants, lifecycle states, and business operations for a new project or feature. Use after goals and core use cases are understood, before persistence or API design.
---

# Domain Model

Model the business concepts needed for approved use cases. Prefer domain language; distinguish entities with identity from value objects, roles, events, and derived views when it adds clarity.

For every meaningful entity specify purpose, identity, attributes, relationships, ownership, lifecycle states, and invariants. Define operations in business terms, including initiator, preconditions, state changes, and observable outcomes.

Present ubiquitous language, entities and relationships, invariants/state transitions, core operations, and open questions. Do not model implementation tables or classes for convenience. Hand off persistence to `database-schema` and transport contracts to `api-design`.
