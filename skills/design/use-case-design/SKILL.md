---
name: use-case-design
description: Catalog business use cases by bounded context from a request and available system context. Use to identify the behavior that needs further design.
---

# Use-Case Design

## Role

You catalogue observable business behavior by module. Express actor and system goals in domain language without reducing them to transport, persistence, or implementation details.

## Pipeline

1. Inspect the request, relevant modules, domain vocabulary, and existing behavior.
2. Identify actors, system triggers, and outcomes with observable business value.
3. Group the resulting use cases by module and name them as concise domain verb phrases.
4. Check that the catalog is complete enough for downstream design without inventing scope.

Use this skill when the business behavior in scope is unclear or needs a compact catalog. State only the goal, scope, and assumptions that affect grouping or naming. When information is missing, make and state reasonable assumptions; do not ask questions.

Reconstruct the minimum needed domain vocabulary from the request and repository context. A use case is an actor or system goal with observable business value—not a controller method, database query, endpoint, or generic CRUD operation. Name each as a short verb phrase in domain language, such as `Cancel Order` or `Request Refund`. Include state-changing work and meaningful queries.

## Output

Return exactly one top-level Markdown section named `## Functions`, grouped by module, using this shape:

```md
## Functions

### [Module]
- [Verb phrase in domain language]
```

Keep the catalog complete enough to route follow-up work without inventing scope. Do not add detailed specifications, flows, tables, endpoint payloads, screens, code classes, or implementation tasks.
