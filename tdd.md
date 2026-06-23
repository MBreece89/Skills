# tdd

**Type:** Model-invoked  
**Category:** Engineering

## Purpose
Test-driven development with a strict red-green-refactor loop. Builds features or fixes
bugs one vertical slice at a time, using failing tests as the agent's primary feedback signal.

## When to Apply
- When building a new feature from a spec or issue
- When fixing a bug (pair with `diagnosing-bugs.md` to find the root cause first)
- When the user invokes `/tdd` explicitly

## The Loop — Repeat Until Done

### Red — Write a Failing Test
1. Identify the **next smallest vertical slice** of behaviour to implement.
2. Write a test that describes that behaviour. The test must:
   - Test through the public interface — never internal implementation details
   - Have a descriptive name: `"should [expected result] when [condition]"`
   - Fail right now (run it to confirm)
3. Do not write any implementation yet. Confirm the test fails for the right reason —
   not a compile error, but a real assertion failure.

### Green — Make It Pass
4. Write the **minimum code** that makes the test pass. No more.
   - Resist the urge to build more than the test requires
   - Hardcoded values are fine at this stage if they make the test pass
5. Run the tests. All must pass — including previously passing tests.

### Refactor — Clean Up
6. Improve the code without changing behaviour:
   - Remove duplication
   - Improve naming
   - Simplify structure
7. Run the tests again after every change. They must stay green.
8. Only refactor now — not in the Green step.

### Repeat
9. Pick the next slice and go back to Red.

## Slicing Rules
- Each slice should be completable in minutes, not hours.
- Prioritise slices that exercise the happy path first, then error cases, then edge cases.
- If a slice feels too big, split it further.

## What Makes a Good Test
See `testing.md` for full guidance. Key rules:
- Test behaviour, not implementation
- One logical assertion per test
- Deterministic, isolated, fast
- Mock only at external boundaries (network, filesystem, clock)

## Rules
- Never write implementation before a failing test exists.
- Never commit a failing test (unless explicitly marked as a known failing case).
- Never skip the Refactor step — entropy accumulates fast with AI-assisted development.

