# Engineering Skills Collection

A small, composable workflow for taking an idea from clarification through architecture, planning, implementation, and focused quality review.

## Possible workflow

```text
grill-me → project-goals ─┐
existing change ──────────┴→ solution-design → selected design work → writing-plans → implementation
                                             │          │
                                             │          └→ context, domain, use cases, data, API, UI, architecture
                                             └→ architecture and focused quality reviews, when consequential
```

Each skill can start from the request and repository context; the diagram is a possible route, not a prerequisite chain. Use only the skills that fit the change. Small, well-understood fixes may begin with `writing-plans` or implementation; larger or unclear work benefits from more of the flow.

## Skills

| Skill | Purpose |
| --- | --- |
| [grill-me](skills/planning/grill-me/SKILL.md) | Clarify an ambiguous idea through focused questions and produce an approved brief. |
| [project-goals](skills/planning/project-goals/SKILL.md) | Define product goals, users, scope, success criteria, and constraints. |
| [solution-design](skills/design/solution-design/SKILL.md) | Turn a goal or change into a proportionate solution and route the remaining design work. |
| [context-map-design](skills/design/context-map-design/SKILL.md) | Map a product into bounded contexts, ownership boundaries, use cases, and dependencies. |
| [domain-design](skills/design/domain-design/SKILL.md) | Define entities, relationships, invariants, lifecycle, and business operations. |
| [use-case-design](skills/design/use-case-design/SKILL.md) | Define business use cases, behavior, and effects by bounded context. |
| [database-schema-design](skills/design/database-schema-design/SKILL.md) | Design relational schemas around domain models and access patterns. |
| [api-design](skills/design/api-design/SKILL.md) | Design secure, evolvable consumer-facing API contracts. |
| [ui-design](skills/design/ui-design/SKILL.md) | Explore core user journeys through screen and interaction prototypes. |
| [architecture-design](skills/design/architecture-design/SKILL.md) | Propose pragmatic system architectures, flows, trade-offs, and delivery considerations. |
| [architecture-review](skills/review/architecture-review/SKILL.md) | Evaluate an existing design for requirement fit, operational concerns, and evolution risks. |
| [writing-plans](skills/planning/writing-plans/SKILL.md) | Turn an approved change into a repository-aware, executable implementation plan. |
| [git-commit](skills/planning/git-commit/SKILL.md) | Prepare focused Git commits with Conventional Commit messages. |
| [go-expert](skills/golang/go-expert/SKILL.md) | Implement, debug, refactor, and review production Go code using idiomatic feature-oriented service practices. |
| [qa-test-design](skills/review/qa-test-design/SKILL.md) | Design prioritized QA scenarios for a feature, change, bug fix, or release. |
| [test-review](skills/review/test-review/SKILL.md) | Assess whether existing automated tests give meaningful behavioral confidence. |
| [security-review](skills/review/security-review/SKILL.md) | Find concrete security risks in code, infrastructure, and technical designs. |
| [scalability-review](skills/review/scalability-review/SKILL.md) | Find capacity, latency, throughput, and resilience bottlenecks. |

## Example

```text
Use $grill-me to clarify a new billing flow.
Use $architecture-design to suggest an architecture for the approved brief.
Use $writing-plans to create an implementation plan for the chosen design.
Use $qa-test-design to prepare release scenarios before implementation begins.
```

The review skills are independent quality gates: invoke the ones relevant to the change rather than treating every review as mandatory.

## Design principles

- Each skill has one responsibility and a visible handoff.
- Suggestions are grounded in the request and existing repository context.
- Plans and designs expose assumptions, risks, alternatives, and unresolved decisions.
- Review findings require evidence and an actionable recommendation.
- Planning and review do not modify application code unless explicitly requested.
