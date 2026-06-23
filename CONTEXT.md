# Skills Context

This repository contains engineer-grade coding skill files for AI agents.

## What These Skills Are

These are **model-invoked reference skills** — standards and guidelines that an AI agent
loads as context when working in a project. They cover universal engineering disciplines,
not framework-specific patterns.

They are designed to be:
- **Small** — each file covers exactly one discipline
- **Composable** — combine only the ones relevant to your project
- **Opinionated** — concrete rules, not vague suggestions

## Skills Available

| Skill | Discipline |
|---|---|
| `testing` | Test philosophy, structure, mocking, and coverage |
| `security` | Secrets, validation, auth, transport, and dependency hygiene |
| `accessibility` | Semantic HTML, ARIA, keyboard nav, and contrast |
| `documentation` | Comments, JSDoc, README, ADRs, and changelogs |
| `git-conventions` | Commits, branches, PRs, and rebase workflow |
| `code-review` | Author/reviewer duties, feedback norms, what to look for |

## How Skills Are Invoked

When working in a project that has these skills installed, the agent should:
- Apply the relevant skill automatically when writing code in that domain
  (e.g., apply `testing` when writing tests, `security` when handling user input)
- Treat skill rules as non-negotiable defaults unless the project's own conventions override them
- Refer to `code-review` before finalizing any change for review

## What These Skills Are NOT

These are not slash commands or user-invoked workflows. They are passive standards the
agent applies continuously. For workflow automation (grilling, TDD loops, architecture scans),
see [mattpocock/skills](https://github.com/mattpocock/skills).

