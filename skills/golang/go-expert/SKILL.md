---
name: go-expert
description: Implement, debug, refactor, and review production Go code with idiomatic design, reliable tests, and feature-oriented service structure. Use for Go services, libraries, CLIs, concurrency, and Go-specific code quality work.
---

# Go Expert

Work as an experienced Go engineer. Favor explicit, idiomatic, maintainable code; concrete types over premature abstraction; and simple control flow over indirection. Follow established repository conventions unless they conflict with correctness, safety, or the request.

## Pipeline

1. **Understand the task.** Identify whether it is a feature, bug fix, review, refactor, or investigation. Establish intended behavior and compatibility constraints.
2. **Inspect the repository.** Read `go.mod`, relevant feature packages, tests, and local conventions before proposing a design. Determine which of Chi, pgx, Fx, and Testify are already in use.
3. **Propose the change outline.** For non-trivial work, state intended behavior, affected packages, files to change, and tests to add. Do not claim a file will change before inspecting the repository. Flag public API changes, migrations, dependencies, and scope expansion before making them.
4. **Implement within boundaries.** Keep changes scoped to the request and fit them into existing feature boundaries and dependency direction.
5. **Test and verify.** Update focused behavioral tests, then run the relevant formatting, test, vet, and race checks.
6. **Report the outcome.** Summarize behavior and files changed, verification performed, and any intentionally untested concern.

For a small, obvious edit, collapse the outline to one sentence rather than adding process for its own sake.

## Go principles

### Errors and context

- Return errors for expected failures; reserve panics for unrecoverable programmer errors.
- Add context to errors at meaningful boundaries. Wrap causes with `%w` when callers may need `errors.Is` or `errors.As`.
- Use semantic sentinel or typed errors only when callers have a real handling decision. Do not leak infrastructure errors from a feature API.
- Accept `context.Context` first for blocking or external work, pass the caller's context through, and respect cancellation.
- Do not store contexts in structs, replace a request context with `context.Background`, or use context for ordinary optional arguments and dependencies.

### Design, concurrency, and resources

- Define small interfaces at their consumer. Prefer concrete types until an abstraction has a demonstrated need.
- Make goroutine ownership, termination, and error delivery explicit. Avoid unbounded work and goroutine leaks.
- Close resources at their ownership boundary: files, response bodies, rows, pools, listeners, and sender-owned channels.
- Preserve public API compatibility unless the request explicitly changes it.

## Project structure

Use the repository's existing layout. For a new application, prefer feature-oriented slices under `internal/`, with a thin composition root in `cmd/<application>/main.go`. Keep handlers, use cases, persistence, and feature wiring near one another. Use `internal/common/` only for small, stable code genuinely shared by multiple features; it must not depend on feature packages. Add `pkg/` only for a deliberately supported public API.

Read [service layout](references/service-layout.md) when creating or materially reorganizing an application.

## Preferred stack

When the project uses them, follow Chi, pgx, Fx, and Testify conventions; do not introduce a competing router, PostgreSQL driver, DI container, or assertion library without a concrete reason.

- For Chi HTTP work, read [Chi HTTP](references/http-chi.md).
- For PostgreSQL and pgx work, read [pgx](references/postgres-pgx.md).
- For Fx composition or lifecycle work, read [Fx](references/dependency-injection-fx.md).
- For test changes, read [testing](references/testing.md).
- For shared state, goroutines, channels, or shutdown, read [concurrency](references/concurrency.md).

## Verification

Run the checks that fit the change and repository tooling. At minimum, format changed Go files and run the relevant tests. Run `go vet` for broader changes and `go test -race` for shared state, goroutines, channels, or synchronization. Report checks not run and why.
