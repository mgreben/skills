---
name: test-review
description: Review automated tests and test changes for meaningful behavioral coverage, reliability, and maintainability. Use for pull-request test reviews, test-strategy reviews, and diagnosing weak or flaky test suites.
---

# Test Review

Assess whether tests provide trustworthy evidence that the intended behavior works and regressions will be caught. Begin with the changed behavior and its public contracts, then relate tests to that behavior rather than optimizing for line coverage.

Check for:

- Happy paths, boundary cases, invalid input, permission states, failures, retries, and state transitions that the change makes meaningful.
- Assertions that validate observable outcomes and contracts, rather than incidental implementation details.
- Tests that could pass despite the defect they are meant to catch, including ineffective mocks and missing assertions.
- Correct isolation of external systems, time, randomness, concurrency, network behavior, and shared state.
- Flakiness risks: order dependence, timing assumptions, global state, fixture coupling, leaked resources, and nondeterministic data.
- An appropriate test level: unit, integration, contract, end-to-end, or load test—without duplicating coverage for no added confidence.

Report findings by impact on confidence. State the missing or unreliable scenario, why existing tests do not establish the behavior, and a concrete test shape that would. Call out relevant coverage that is already strong. Do not demand tests for trivial refactors or private implementation details when existing behavior-level coverage suffices.
