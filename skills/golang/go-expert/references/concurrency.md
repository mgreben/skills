# Concurrency

Before adding a goroutine, state its owner, input and output, cancellation path, error path, and termination condition. The owner must be able to stop and wait for it when the application or request ends.

Prefer a direct synchronous flow unless concurrency materially improves latency, throughput, or responsiveness. Bound fan-out and queues. Use `errgroup` or an equivalent coordination mechanism when sibling goroutines share a cancellation and error boundary.

Protect shared mutable state with a clear synchronization strategy. Do not mix channel ownership and mutex ownership ambiguously. Close a channel only from its sending side when that side owns closure; receivers should not infer completion by closing it.

Run the race detector for concurrency changes. Include cancellation, errors, resource cleanup, and shutdown in tests where those behaviors are part of the change.
