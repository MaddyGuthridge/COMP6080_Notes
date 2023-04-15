[[testing|Tests]] are flaky if they aren't deterministic, meaning that they don't produce consistent results.

We want to avoid flakiness as much as possible, since it makes our tests unreliable and frustrating to debug with.

## Causes of test flakiness
- Randomness and time-variability
- Performance (what if the machine running the tests is slow and they don't render fast enough?)
- Testing environment: is the browser up-to-date? Is the browser reliable (👀 Safari)

## Component testing
In [[component test|component tests]], tests are often flaky due to external components, such as backend services.

We can resolve this through mock services, which we can use to replace the actual services using dependency injection.
