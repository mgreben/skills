---
name: database-schema-design
description: Design a relational database schema from requirements, business rules, and access patterns. Use for new-project data models, schema changes, and persistence design; not for choosing an entire system architecture.
---

# Database Schema Design

Use this skill when relational persistence, data integrity, migration, or access patterns change. State the goal, scope, relevant system evidence, and assumptions. Confirm database technology and consistency requirements when they materially affect the design; otherwise state the assumed relational dialect.

Translate relevant business rules and access patterns into a durable schema. For each table define columns/types, keys, nullability, defaults, checks, uniqueness, indexes tied to real access patterns, and ownership. Explain cardinality, deletion behavior, audit/history, sensitive fields, tenancy, and retention where applicable.

## Output

Present access patterns, schema with relationships, integrity and security controls, index rationale, migration notes, consequential decisions with rationale, and open decisions. Normalize by default and justify denormalization. Account for compatibility, backfill, validation, and rollback in live schema changes. Do not define HTTP endpoints or UI behavior.
