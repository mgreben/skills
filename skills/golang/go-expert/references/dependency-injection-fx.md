# Dependency Injection with Fx

Use Fx for wiring, not as a runtime dependency container. Application and feature logic must not receive or retrieve an Fx application/container.

Build each feature as a focused `fx.Module`; assemble modules in `cmd/<application>/main.go`. Constructors declare explicit inputs and return fully initialized values. Keep dependencies visible rather than using globals or service locators.

Use lifecycle hooks for resources the application owns: servers, pools, consumers, and background workers. Start quickly, make shutdown cancellation-aware, stop accepting work before closing shared resources, and wait for worker termination where required. Long-running work should run outside the hook and have explicit shutdown coordination.
