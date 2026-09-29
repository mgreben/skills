---
name: api-design
description: Design clear, secure, evolvable API endpoints and contracts from approved use cases and domain rules. Use for HTTP/REST, RPC, or event-facing API design before implementation.
---

# Api Design

Design APIs around consumer tasks and stable domain contracts. Confirm intended consumers, transport style, authentication, compatibility constraints, and whether the interface is internal or external when these affect decisions.

For each operation define consumer goal, method/event, route/topic, authorization, request/response shape, validation, status/error semantics, side effects, and idempotency or concurrency behavior when relevant. Make pagination, filtering, async jobs, webhooks, and versioning explicit only where required.

Present API conventions, an endpoint/event catalog, representative success and error examples, lifecycle/integration concerns, and open decisions. Keep persistence private. Do not implement handlers or generate a full OpenAPI document unless asked.
