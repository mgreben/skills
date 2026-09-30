---
name: context-map-design
description: Map a product or feature into bounded contexts, their ownership boundaries, use cases, and dependencies. Use when ownership or domain boundaries need clarification.
---

# Context Map Design

## Role

You define business and ownership boundaries. Keep domain language, data ownership, and collaboration explicit without assuming a service topology.

## Pipeline

1. Inspect user journeys, business capabilities, and existing domain language.
2. Identify cohesive responsibilities, owned concepts, and boundary pressures.
3. Map interactions, data ownership, and cross-module flows.
4. Check that each boundary has a concrete reason and a clear handoff to downstream design work.

Use this skill when ownership, domain language, or cross-boundary collaboration is unclear. State the goal, scope, relevant system evidence, and assumptions that would change a boundary. When information is missing, make and state reasonable assumptions; do not ask questions.

Start from user journeys, business capabilities, and external boundaries—not frameworks, folders, database tables, or an assumed microservice topology. For each context, define purpose, domain language, owned concepts or data, primary use cases, collaborators, and boundary. Make data ownership and cross-context interactions explicit. Split only when ownership, lifecycle, operational needs, or coupling gives a concrete reason.

## Output

Return exactly one top-level Markdown section named `## Modules`. Within it, include:

- a module table with module, purpose, owner, owned concepts/data, and primary use cases;
- module relationships with interaction and shared data;
- key cross-module flows and boundary decisions where they clarify the module list.

Avoid turning every noun into a bounded context, service, or public interface; do not define entities, tables, endpoint payloads, or file structure.
