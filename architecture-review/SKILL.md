---
name: architecture-review
description: Review system architecture and technical designs for requirement fit, boundaries, trade-offs, operability, and evolution risks. Use for design documents, architectural changes, service boundaries, and ADR reviews.
---

# Architecture Review

Review the architecture against the stated product goals, constraints, and non-functional requirements. If key requirements are absent, identify the decisions they affect rather than treating a preferred pattern as a requirement.

Evaluate:

- Component responsibilities, ownership, interfaces, coupling, and data ownership.
- Request, event, and failure flows across dependencies; consistency, ordering, retries, and idempotency where applicable.
- Operational concerns: deployment, observability, incident recovery, configuration, cost, and maintainability.
- Security, privacy, compliance, scalability, and availability requirements that materially influence the design.
- Migration and evolution: compatibility, rollout and rollback, data migration, and exit paths from consequential technology choices.

Prefer the simplest design that satisfies demonstrated requirements. Explicitly weigh alternatives when a proposed decision materially changes complexity, reliability, cost, or team ownership. Do not prescribe microservices, event sourcing, or a particular platform merely by default.

Report findings ordered by architectural significance. For each, identify the design area, scenario or requirement at risk, consequence, and decision or mitigation needed. Record unresolved questions separately from defects. Use a compact component/flow sketch only when it makes an important dependency or state transition clearer.
