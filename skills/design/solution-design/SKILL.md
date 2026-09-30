---
name: solution-design
description: Route a product or technical change through the smallest coherent set of design decisions and artifacts. Use when the route to detailed design is unclear; not for a narrowly scoped API, schema, UI, or implementation plan.
---

# Solution Design

Act as the design entry point: turn a request and repository context into the smallest coherent design route.

Inspect the relevant product, repository, and operational context. Establish the goal, scope, success condition, constraints, evidence, assumptions, and product decisions still missing. Do not disguise a missing product decision as a technical recommendation.

Address the most uncertain or hard-to-reverse decision first. Use a design delta when a small, established-area change has no new business rule, external contract, data migration, or consequential technical decision. Otherwise select only the needed specialists:

- unclear ownership, terms, or cross-boundary collaboration → `context-map-design`;
- unclear business behavior → `use-case-design`, then `domain-design` when lifecycle or invariants matter;
- changed consumer or integration contract → `api-design`;
- changed persistence, integrity, migration, or access patterns → `database-schema-design`;
- changed user journey or interaction states → `ui-design`;
- changed topology, availability, component ownership, or operations → `architecture-design`.

Do not invoke every stage, invent infrastructure, or produce an implementation plan merely to complete a pipeline. Stop when high-impact, difficult-to-reverse decisions are specified or explicitly awaiting approval.

## Output

Present the result in the response.

1. **Design basis** — goal, scope, non-goals, evidence, assumptions, and constraints.
2. **Current solution slice** — the key flow, changed boundaries, and decisions already made.
3. **Design route** — completed, required-next, deferred-safe, and unnecessary artifacts, with a reason for each.
4. **Decision register** — consequential choices, trade-offs, and approvals required.
5. **Handoff** — validation, delivery concerns, and one recommended next action.

Do not claim approval or implementation authorization.
