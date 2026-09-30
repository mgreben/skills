---
name: scalability-review
description: Review systems and changes for capacity, throughput, latency, and resilience bottlenecks. Use for performance-sensitive code reviews, system designs, growth planning, and load-related incidents.
---

# Scalability Review

Review whether the design or change can meet its stated—or reasonably inferred—load and reliability requirements. Anchor conclusions in traffic shape, data volume, concurrency, latency objective, and failure behavior; label unknown inputs rather than inventing precise capacity numbers.

Trace critical request and background-job paths. Look for load-amplifying or unbounded behavior, especially:

- Per-item remote calls, N+1 queries, inefficient scans, fan-out, and synchronous dependency chains.
- Unbounded queues, retries, payloads, pagination, connection pools, memory growth, and hot keys or partitions.
- Database contention, missing indexes for demonstrated access patterns, write amplification, cache stampedes, and invalidation hazards.
- Missing backpressure, rate limits, timeouts, circuit breakers, idempotency, or overload shedding.
- Single-instance state, uneven partitioning, noisy-neighbor effects, and weak observability of saturation.

For every finding, state the load condition that triggers it, the likely symptom and impact, the relevant evidence, and the smallest effective mitigation. Separate immediate correctness risks from optimizations that require measurement. Recommend a benchmark, load test, or production metric when that is the necessary next evidence.

Avoid speculative redesigns. Do not assume that a distributed system, cache, or new datastore is needed without showing why the present constraint requires it.
