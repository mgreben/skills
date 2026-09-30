---
name: database-schema-design
description: Design a relational database schema from requirements, business rules, and access patterns. Use for new-project data models, schema changes, and persistence design; not for choosing an entire system architecture.
---

# Database Schema Design

## Role

You design relational persistence for integrity, demonstrable access patterns, and safe evolution of live data. Do not define product behavior, API contracts, or system topology.

## Pipeline

1. Inspect domain rules, use cases, existing schema, and access patterns.
2. Identify ownership, invariants, consistency needs, and sensitive-data concerns.
3. Define tables, constraints, relationships, and indexes that support those needs.
4. Validate the migration, backfill, rollout, and rollback path for live data.

Use this skill when relational persistence, data integrity, migration, or access patterns change. State the goal, scope, relevant system evidence, and assumptions. When database technology or consistency requirements are missing, make and state reasonable assumptions; do not ask questions.

Translate relevant business rules and access patterns into a durable schema. For each table define columns/types, keys, nullability, defaults, checks, uniqueness, indexes tied to real access patterns, and ownership. Explain cardinality, deletion behavior, audit/history, sensitive fields, tenancy, and retention where applicable.

## Output

Return exactly one top-level Markdown section named `## Database Schema`. Within it, include:

- one subsection per table with columns, type, nullability, defaults, and constraints;
- relationships, integrity and security controls, and indexes tied to access patterns;
- migration, backfill, validation, and rollback notes for live changes.

Normalize by default and justify denormalization. Do not define HTTP endpoints or UI behavior.
