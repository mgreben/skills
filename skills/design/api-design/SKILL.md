---
name: api-design
description: Design clear, secure, evolvable API endpoints and contracts from a request and available system context. Use for HTTP/REST, RPC, or event-facing API design.
---

# Api Design

## Role

You design stable consumer-facing contracts. Represent consumer tasks and domain capabilities without exposing storage or prescribing internal implementation.

## Pipeline

1. Inspect relevant use cases, domain rules, existing contracts, and compatibility constraints.
2. Define operations around consumer tasks, including authorization, validation, outcomes, and failure behavior.
3. Check contract consistency, idempotency, integration behavior, and evolution impact.
4. Hand off affected consumer flows, operations, or delivery risks to the relevant design or review skill.

Use this skill when a consumer-facing HTTP, RPC, event, or webhook contract changes. State the consumer goal, scope, relevant system evidence, and assumptions. When contract context is missing, make and state reasonable assumptions about consumers, transport, authentication, compatibility, and exposure; do not ask questions.

Design around consumer tasks and stable domain contracts. For each operation define consumer goal, method/event, route/topic, authorization, request/response shape, validation, status/error semantics, side effects, and idempotency or concurrency behavior when relevant. Define a consistent error representation and correlation mechanism for external or distributed interfaces. Make pagination, filtering, async jobs, webhooks, and versioning explicit only where required.

## Output

Return exactly one top-level Markdown section named `## API`. Within it, include:

- API conventions for naming, authentication, errors, correlation, and versioning where relevant;
- an operation catalog with method/event, route/topic, authorization, and idempotency;
- request, representative success response, and error table for each operation;
- lifecycle and integration concerns where applicable.

Keep persistence private. Do not implement handlers or generate a full OpenAPI document unless asked.
