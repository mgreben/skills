---
name: use-case-design
description: Catalog business use cases by bounded context from a request and available system context. Use to identify the behavior that needs further design.
---

# Use-Case Design

Use this skill when the business behavior in scope is unclear or needs a compact catalog. State only the goal, scope, and assumptions that affect grouping or naming.

Reconstruct the minimum needed domain vocabulary from the request and repository context. A use case is an actor or system goal with observable business value—not a controller method, database query, endpoint, or generic CRUD operation. Name each as a short verb phrase in domain language, such as `Cancel Order` or `Request Refund`. Include state-changing work and meaningful queries.

## Output

Present the result in the response.

Present only a brief design basis, headings for bounded contexts, bullet lists of use cases, and `## Open Decisions` only when they prevent correct grouping or naming. Keep the catalog complete enough to route follow-up work without inventing scope. Do not add detailed specifications, flows, tables, endpoint payloads, screens, code classes, or implementation tasks.
