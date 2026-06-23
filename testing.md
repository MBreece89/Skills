# Testing

## Philosophy
- Write tests that describe **behavior**, not implementation details.
- Prefer integration tests over isolated unit tests where appropriate.
- Tests should be deterministic, independent, and fast.

## Structure
- Use the **Arrange-Act-Assert** (AAA) pattern consistently.
- Name tests descriptively: `"should [expected behavior] when [condition]"`.
- One logical assertion per test (multiple related asserts are fine if testing one behavior).

## Practices
- Mock sparingly — only at boundaries (network, file system, clock).
- Avoid testing private methods directly; test through the public API.
- Use factories or builders for test data instead of copy-pasting objects.
- Prefer real implementations over mocks when feasible.

## Anti-patterns to Avoid
- Tests that break when refactoring internals (brittle tests).
- Shared mutable state between tests.
- Testing framework code or third-party libraries.
- Overly DRY test code that sacrifices readability.

## Coverage
- Aim for meaningful coverage, not 100% line coverage.
- Prioritize testing: error paths, edge cases, business logic.
- Every bug fix should include a regression test.

