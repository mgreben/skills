# Engineering Skills Collection

A small, composable workflow for taking an idea from clarification through architecture, planning, implementation, and focused quality review.

## Suggested workflow

```text
grill-me → architecture-design → architecture-review → writing-plans
                                               ↓
                implementation → QA and engineering review skills
```

Use only the skills that fit the change. Small, well-understood fixes may begin with `writing-plans` or implementation; larger or unclear work benefits from the full flow.

## Skills

| Skill | Purpose |
| --- | --- |
| [grill-me](grill-me/SKILL.md) | Clarify an ambiguous idea through focused questions and produce an approved brief. |
| [architecture-design](architecture-design/SKILL.md) | Propose pragmatic system architectures, flows, trade-offs, and delivery considerations. |
| [architecture-review](architecture-review/SKILL.md) | Evaluate an existing design for requirement fit, operational concerns, and evolution risks. |
| [writing-plans](writing-plans/SKILL.md) | Turn an approved change into a repository-aware, executable implementation plan. |
| [git-commit](git-commit/SKILL.md) | Prepare focused Git commits with Conventional Commit messages. |
| [qa-test-design](qa-test-design/SKILL.md) | Design prioritized QA scenarios for a feature, change, bug fix, or release. |
| [test-review](test-review/SKILL.md) | Assess whether existing automated tests give meaningful behavioral confidence. |
| [security-review](security-review/SKILL.md) | Find concrete security risks in code, infrastructure, and technical designs. |
| [scalability-review](scalability-review/SKILL.md) | Find capacity, latency, throughput, and resilience bottlenecks. |

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
