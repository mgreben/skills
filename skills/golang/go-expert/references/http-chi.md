# Chi HTTP

Use standard `net/http` handlers and middleware with Chi. Register routes per feature, such as `user.RegisterRoutes(r, service)`, then compose them in the application router.

Keep a handler limited to transport work: decode and validate the request, call the use case with `r.Context()`, map expected feature errors to HTTP status and response bodies, and encode a response. Do not put SQL, transactions, or core business decisions in handlers.

Use global middleware only for genuine cross-cutting behavior such as request IDs, recovery, logging, authentication, and appropriate request deadlines. Apply narrow middleware to the route or router group it serves. Request-scoped context values need unexported, typed keys; context is not a general dependency container.

At the composition root, configure `http.Server` timeouts and coordinate graceful shutdown. Keep response format and error mapping consistent with established API conventions.
