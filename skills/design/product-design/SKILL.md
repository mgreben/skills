---
name: product-design
description: "Turn a product idea or feature request into a coherent product design: modules, entities, functions, relational schema, API endpoints, and UI wireframe prototypes. Use for end-to-end idea design; use the specialist design skills to deepen one artifact."
---

# Product Design

Turn an idea into a coherent, implementation-neutral product design. This is the default entry point for designing a new product or feature.

Inspect the request and relevant repository or product context first. Keep observed facts distinct from assumptions. Do not ask questions: make pragmatic, reversible assumptions and proceed. State only assumptions that materially affect the result. Do not produce deployment architecture, an implementation plan, or production code unless requested.

Design the following artifacts in order. Use one shared vocabulary throughout; do not redefine a term, ownership boundary, or business rule in a later section.

1. **Modules** — product ownership and responsibility boundaries.
2. **Entities** — domain concepts, relationships, lifecycle, and invariants.
3. **Functions** — user or system goals with observable business value, grouped by module.
4. **Database Schema** — relational persistence supporting the entities, invariants, and access patterns.
5. **API** — consumer-facing operations that support the functions.
6. **UI Prototype** — task-focused pages, flows, states, and low-fidelity wireframes that use the API.

Keep the design proportionate. Do not invent modules, tables, endpoints, or screens for speculative future scope. Do not expose database structure through the API merely because it exists.

## Output

Return these six top-level Markdown sections in exactly this order:

```md
## Modules
## Entities
## Functions
## Database Schema
## API
## UI Prototype
```

Use concise IDs when they improve traceability: module `M1`, entity `E1`, function `F1`, table `T1`, endpoint `A1`, and page `P1`. A function must belong to a module; persisted entities must have an explicit schema decision; each endpoint and primary UI action must support a function. Mention exceptions rather than silently forcing a mapping.

### Modules

For each module, give its purpose, owned concepts/data, and primary functions. Show cross-module relationships and only the boundary decisions necessary to understand them. Modules are business ownership boundaries, not necessarily services, folders, or teams.

### Entities

Include a concise domain glossary, then identify entities, value objects, relationships, ownership, meaningful lifecycle states, and invariants. Use business language rather than classes or tables.

### Functions

Group functions by module. For each function, state actor or trigger, outcome, and business rules only when needed to define later contracts or state changes. Name functions as domain verb phrases, not CRUD or transport operations.

### Database Schema

For each table, specify columns/types, nullability, keys, constraints, and indexes tied to a function or access pattern. Include relationships, deletion behavior, sensitive-data controls, and migration notes when applicable. Normalize by default; justify denormalization. State the concurrency strategy where an invariant spans rows or requests.

### API

Give conventions only when needed, then an operation catalog with method/event, route/topic, authorization, and idempotency. For each meaningful operation, include request, representative success response, validation/error semantics, and relevant side effects. Keep persistence private.

### UI Prototype

Include a page inventory, primary flow, and material loading, empty, validation, error, permission, success, and destructive-action states. For every primary page, include an ASCII wireframe in a fenced `text` block. Show hierarchy, navigation, controls, and content; do not simulate visual styling. Map each primary UI action to its supporting function and API operation. Include accessibility, responsive, and localization considerations where relevant.

Use the focused design skills when the request concerns only modules, domain entities, functions, schema, API, or UI—not when the user wants this complete product-design output.
