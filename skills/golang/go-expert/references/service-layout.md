# Service Layout

For a new service, organize application code by feature or bounded context rather than globally by technical layer:

```text
cmd/
  api/
    main.go
internal/
  user/
    module.go
    routes.go
    handler.go
    service.go
    repo.go
    postgres.go
    user_test.go
  auth/
  common/
    pagination/
    validation/
pkg/
  client/
```

`main.go` is the composition root: configuration, dependency wiring, route registration, process lifecycle, and graceful shutdown. It should not contain business behavior.

Keep transport and storage concerns at a feature's edge. Do not let driver, framework, or HTTP types leak through its use-case APIs. Define a repo interface at the consumer—normally the feature service—and keep its pgx implementation local to that feature.

Extract code to `internal/common/` only after two or more features have a demonstrated shared need. Avoid generic `utils` or `helpers` packages. `common` may be imported by features but must not import feature packages. Do not add directories or layers without a concrete responsibility.

Use `pkg/` only when another module is expected to import a documented, stable API; `internal/` is the default for application code.
