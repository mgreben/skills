---
name: context-map-design
description: Map a product or feature into bounded contexts, their ownership boundaries, use cases, and dependencies. Use when ownership or domain boundaries need clarification.
---

# Context Map Design

Use this skill when ownership, domain language, or cross-boundary collaboration is unclear. State the goal, scope, relevant system evidence, and assumptions that would change a boundary.

Start from user journeys, business capabilities, and external boundaries—not frameworks, folders, database tables, or an assumed microservice topology. For each context, define purpose, domain language, owned concepts or data, primary use cases, collaborators, and boundary. Make data ownership and cross-context interactions explicit. Split only when ownership, lifecycle, operational needs, or coupling gives a concrete reason.

## Output

Present a context map, key use cases, dependencies and flows, boundary decisions with rationale, and open questions. Identify validation or approval needed for consequential boundaries. Avoid turning every noun into a bounded context, service, or public interface; do not define entities, tables, endpoint payloads, or file structure.
