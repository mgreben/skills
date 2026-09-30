---
name: writing-plans
description: Create an executable, repository-aware implementation plan for an approved change. Use after requirements or a design are clear and before modifying code; planning only unless the user explicitly asks to proceed with implementation.
---

# Writing Plans

Create a plan that another capable engineer can execute without rediscovering the change. Treat an approved brief or design as the source of intent; if a missing decision would materially change the approach, identify it before finalizing the plan.

Inspect the relevant repository, conventions, tests, and dependency boundaries before proposing steps. Base file paths, components, and constraints on evidence. Do not modify application files in planning-only work.

Choose the smallest sequence that meets the approved requirements. Each step should be independently understandable and include:

- Exact file paths and the symbols, contracts, or behavior to change.
- The implementation logic and important edge cases; explain existing patterns to reuse.
- Required tests, migrations, compatibility considerations, or operational changes.
- A concrete verification action and expected result.

Order steps by dependencies and preserve safe rollout paths when behavior, data, or public interfaces change. Call out risks, rollback strategy, and unresolved questions separately; do not hide uncertainty behind invented details. Prefer incremental migrations and compatibility phases where the current system requires them.

Present the result in this format:

1. **Summary** — objective, boundaries, and approach.
2. **Current state** — relevant observed components and constraints.
3. **Implementation steps** — small, ordered, verifiable changes.
4. **Validation** — targeted tests, checks, and manual scenarios.
5. **Risks and open questions** — including rollout or rollback concerns.

End by asking for approval to implement if implementation has not already been authorized. Do not add speculative refactors, architecture changes, or scope beyond the approved brief.
