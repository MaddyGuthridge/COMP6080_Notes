Tests are flaky if they aren't deterministic, meaning that they don't produce consistent results.

We want to avoid flakiness as much as possible, since it makes our tests unreliable and frustrating to debug with.

## Component testing
In [[component test]]s, things are often flaky due to external components, such as backend services.

We can resolve this through mock services, which we can use to replace the actual services using dependency injection.