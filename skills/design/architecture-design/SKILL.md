---
name: architecture-design
description: Propose and compare pragmatic system architectures for a product, feature, or technical change. Use for new designs, service boundaries, integration choices, and major technical decisions; not for reviewing an already proposed architecture.
---

# Architecture Design

Use this skill for consequential system decisions: component boundaries, integration style, deployment topology, availability, data ownership, or operational responsibility. Start by establishing functional, scale, reliability, security, data, integration, operational, team, and cost constraints. Clearly separate observed facts, requirements, and assumptions. Ask focused questions only when unknowns would change the design; otherwise state assumptions.

Inspect relevant repository or system context before suggesting a replacement. Preserve established patterns and platform choices unless a demonstrated requirement or failure mode justifies a change.

For the preferred approach, define:

- Components, responsibilities, ownership, interfaces, and data ownership.
- Synchronous requests, asynchronous events, key state transitions, and dependency/failure behavior.
- Authentication and authorization boundaries, sensitive-data handling, and meaningful threat mitigations.
- Capacity strategy, availability goals, observability, deployment, configuration, backup/recovery, and operational responsibilities as applicable.
- Compatibility, migration, rollout, rollback, and evolutionary paths for externally visible or data-bearing changes.

Evaluate alternatives only when they are credible options. Compare them against the actual decision criteria: complexity, delivery speed, reliability, scale, cost, team expertise, and reversibility. Do not prescribe microservices, queues, caches, event sourcing, or a particular cloud product merely because they are common patterns.

## Output

Present the result in the response.

Present the result as:

1. **Context and requirements** — confirmed inputs, assumptions, and non-goals.
2. **Recommended architecture** — components, responsibilities, interfaces, and key flows; include a compact Mermaid diagram when it clarifies the relationships.
3. **Key decisions and trade-offs** — alternatives considered and why the recommendation fits.
4. **Failure and operational model** — important failure modes, mitigation, and observability.
5. **Delivery and evolution** — migration, rollout/rollback, validation, and decisions still requiring approval.

Write an ADR-style record only for consequential decisions that need a durable rationale. Do not implement the architecture unless explicitly asked.
