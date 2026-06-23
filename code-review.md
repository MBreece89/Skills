# Code Review

## As an Author (Before Requesting Review)
- Self-review your diff before assigning reviewers — catch obvious issues yourself.
- Keep PRs small and focused; one concern per PR makes review fast and safe.
- Write a clear description: what changed, why, and how to test it.
- Mark areas of uncertainty or where you'd especially welcome feedback.
- Ensure CI passes and there are no merge conflicts before requesting review.

## As a Reviewer
- Understand the goal of the change before diving into the code.
- Review the design first, then the details — don't nitpick style if the approach is wrong.
- Read the tests as documentation for what the code should do.
- Look for: missing error handling, security issues, missing edge cases, and coupling.
- Check that the code is as simple as possible — complexity is the enemy.

## Giving Feedback
- Be specific: point to the exact line and explain the concern clearly.
- Distinguish blocking issues from suggestions: use labels like `nit:` or `blocker:`.
- Phrase feedback as questions or observations, not commands: "Could this fail if X is null?" over "Fix this."
- Acknowledge good work — not everything needs to be a criticism.
- If you'd write it differently but it's not objectively wrong, note it as a preference, not a blocker.

## Receiving Feedback
- Assume good intent — reviewers are trying to help.
- If you disagree, explain your reasoning calmly rather than just reverting the comment.
- Resolve conversations after addressing them so the reviewer knows what changed.
- A comment is not an order — discuss if the suggestion doesn't feel right.

## What to Look For
- **Correctness**: Does it do what it says? Does it handle edge cases?
- **Clarity**: Can a new team member understand this in 6 months?
- **Consistency**: Does it match patterns already used in the codebase?
- **Tests**: Are meaningful tests present? Do they test behavior, not implementation?
- **Security**: Is input validated? Are there injection risks or exposed secrets?
- **Performance**: Any obvious O(n²) loops, N+1 queries, or unnecessary re-renders?

## Anti-Patterns to Avoid
- Rubber-stamping approvals without actually reading the code.
- Blocking PRs over stylistic disagreements that a formatter should handle.
- Reviewing at the end of a large feature — review early and often instead.
- Long review delays — aim to review within one working day.
- Scope creep: requesting unrelated refactors in a PR review.

