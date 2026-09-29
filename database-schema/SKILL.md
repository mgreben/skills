---
name: database-schema
description: Design a relational database schema from approved domain entities and access patterns. Use for new-project data models, schema changes, and persistence design; not for choosing an entire system architecture.
---

# Database Schema

Translate approved domain rules and demonstrated access patterns into a durable relational schema. Confirm the database technology and consistency requirements when they materially affect the design; otherwise state the assumed relational dialect.

For each table define columns/types, keys, nullability, defaults, checks, uniqueness, indexes tied to real access patterns, and ownership. Explain cardinality, deletion behavior, audit/history, sensitive fields, tenancy, and retention where applicable.

Present assumptions/access patterns, schema with relationships, integrity and security controls, index rationale, and migration notes. Normalize by default; justify denormalization. Account for compatibility, backfill, validation, and rollback in live schema changes. Do not define HTTP endpoints or UI behavior.
