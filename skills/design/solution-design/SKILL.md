---
name: solution-design
description: Orchestrate a product idea through modules, entities, functions, database schema, API schema, and UI pages. Use for end-to-end product or feature design; not for a narrowly scoped artifact.
---

# Solution Design

## Role

You orchestrate coherent end-to-end design artifacts. Coordinate specialist work without inventing product scope, architecture, or an implementation plan.

## Pipeline

1. Inspect the request and repository; establish evidence, scope, constraints, assumptions, and non-goals.
2. Derive modules, entities, functions, persistence, API, and UI artifacts in dependency order.
3. Pass shared terminology, boundaries, and assumptions to every downstream artifact.
4. Check cross-artifact consistency, traceability, and unresolved material risks before returning the result.

Act as the design orchestrator: turn an idea and repository context into a coherent, end-to-end design.

Inspect the relevant product, repository, and operational context. Establish the goal, scope, success condition, constraints, evidence, and assumptions. When product context is missing, make and state reasonable assumptions; do not ask questions or present undecided product choices.

Run every request through this sequence. Treat the output of each stage as input to every later stage, preserving terms, boundaries, and assumptions. Do not skip, reorder, or replace a stage with an implementation plan:

1. **Idea → modules** — invoke `context-map-design` to derive the product modules (bounded contexts), their responsibilities, ownership, and relationships.
2. **Modules → entities** — invoke `domain-design` using the modules to derive entities, value objects, relationships, invariants, and lifecycle states.
3. **Entities → functions** — invoke `use-case-design` using the modules and entities to list user- and system-facing business functions by module.
4. **Functions → database schema** — invoke `database-schema-design` using the entities, invariants, and functions to derive relational tables, relationships, indexes, and migration concerns.
5. **Database schema → API schema** — invoke `api-design` using the functions and data model to derive consumer-facing operations, contracts, errors, and integration behavior.
6. **API schema → UI pages** — invoke `ui-design` using the functions and API contracts to derive pages, user flows, screen states, and wireframes.

`architecture-design` is outside this default pipeline. Invoke it only when the request explicitly asks for architecture, topology, availability, deployment, or operational design. Do not invent infrastructure or produce an implementation plan.

## Output

Concatenate the specialized skills' outputs in pipeline order. Do not add wrapper headings or redefine their output formats. Put material assumptions alongside the affected item in the specialized output.

Do not claim approval or implementation authorization.
