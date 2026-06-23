# Git Conventions

## Commit Messages
- Use conventional commit format: `type(scope): description`
- Types: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`, `style`, `perf`, `ci`
- Keep the subject line under 72 characters.
- Use imperative mood: "add feature" not "added feature".
- Include a body for non-trivial changes explaining **why**, not just what.

## Commits
- Keep commits atomic — one logical change per commit.
- Ensure each commit compiles and passes tests independently.
- Do not mix formatting changes with functional changes.

## Branches
- Use descriptive branch names with a prefix: `feature/`, `bugfix/`, `chore/`.
- Keep branches short-lived; merge or rebase frequently.
- Delete branches after merging.

## Pull Requests
- Write a clear title and description summarizing the change.
- Reference related issues or tickets.
- Keep PRs small and focused — easier to review and less risk.
- Respond to review comments promptly; resolve conversations.

## Workflow
- Never force-push to shared/protected branches.
- Prefer rebasing feature branches onto main before merging (clean history).
- Squash commits when merging if the branch history is noisy.
- Pull/rebase from main regularly to avoid large merge conflicts.

