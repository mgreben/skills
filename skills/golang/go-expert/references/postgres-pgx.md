# PostgreSQL with pgx

Use `pgxpool.Pool` for shared application access and close it during application shutdown. Pass the caller's context to pool, query, transaction, and row operations.

Keep SQL, pgx values, and scan/mapping details at the persistence boundary. Map `pgx.ErrNoRows` to a semantic feature error such as `ErrNotFound`, instead of exposing database-driver behavior to callers. Wrap other database failures with the operation and resource context while preserving the cause.

Use a transaction for one atomic unit of work. On every non-committed path roll it back; check commit errors. Do not start a transaction merely because a query writes data.

Prefer integration tests against PostgreSQL for meaningful query behavior when practical. Avoid mocks that only assert an implementation's exact SQL call sequence instead of protecting feature behavior.
