---
name: api-design
description: Design clear, secure, evolvable API endpoints and contracts from a request and available system context. Use for HTTP/REST, RPC, or event-facing API design.
---

# Api Design

Use this skill when a consumer-facing HTTP, RPC, event, or webhook contract changes. State the consumer goal, scope, relevant system evidence, and assumptions. Confirm intended consumers, transport style, authentication, compatibility constraints, and internal versus external exposure when they change the contract.

Design around consumer tasks and stable domain contracts. For each operation define consumer goal, method/event, route/topic, authorization, request/response shape, validation, status/error semantics, side effects, and idempotency or concurrency behavior when relevant. Define a consistent error representation and correlation mechanism for external or distributed interfaces. Make pagination, filtering, async jobs, webhooks, and versioning explicit only where required.

## Output

Present API conventions, endpoint/event catalog, representative success and error examples, lifecycle/integration concerns, consequential decisions with rationale, validation concerns, and open decisions. Keep persistence private. Do not implement handlers or generate a full OpenAPI document unless asked.
