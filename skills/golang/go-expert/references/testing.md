# Testing

Test observable behavior and contracts rather than private implementation details. Prefer the smallest test level that gives meaningful confidence: unit tests for local behavior, `httptest` for HTTP boundaries, and PostgreSQL integration tests for query semantics.

Use named table-driven tests when cases share setup and assertions. Use `t.Cleanup` for test-owned resources. Avoid `time.Sleep`; synchronize explicitly or use a bounded eventual condition. Use `t.Parallel()` only when isolation, resources, and shared state make it safe.

When the repository uses Testify, follow its established style:

- Use `require` for preconditions that make the rest of a test meaningless; use `assert` for independent expectations.
- Prefer `ErrorIs` and `ErrorAs` assertions for wrapped or typed errors.
- Use `testify/mock` sparingly. A focused fake or test server is often clearer when behavior matters more than exact calls.

Do not add Testify just to replace an established standard-library testing style.
