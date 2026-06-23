# Skills

Engineer-grade coding standards for AI agents. Small, composable, and opinionated.

## Quickstart

Install into any project using the [skills CLI](https://github.com/mattpocock/skills):

```sh
npx skills@latest add mb0762/skills
```

Pick the skills you want, select which agents to install them on, and you're done.

## Skills Included

### Reference Skills — applied automatically by context

| Skill | Description |
|---|---|
| [testing](skills/testing.md) | Test philosophy, structure, mocking, anti-patterns, and coverage |
| [security](skills/security.md) | Secrets, input validation, auth, transport, and dependency hygiene |
| [accessibility](skills/accessibility.md) | Semantic HTML, ARIA, keyboard nav, forms, and contrast |
| [documentation](skills/documentation.md) | Comments, JSDoc, README, ADRs, and changelogs |
| [git-conventions](skills/git-conventions.md) | Commit messages, branching, PRs, and rebase workflow |
| [code-review](skills/code-review.md) | Author/reviewer duties, feedback norms, and what to look for |
| [codebase-design](skills/codebase-design.md) | Deep module design: behaviour behind a small interface |
| [domain-modeling](skills/domain-modeling.md) | Build and sharpen the project glossary and ADRs |
| [tdd](skills/tdd.md) | Red-green-refactor loop, one vertical slice at a time |
| [diagnosing-bugs](skills/diagnosing-bugs.md) | Reproduce → minimise → hypothesise → fix → regression test |
| [grilling](skills/grilling.md) | Reusable interview loop for resolving plans before building |

### Workflow Skills — invoked by typing `/skill-name`

#### Engineering
| Skill | Description |
|---|---|
| [/ask-me](skills/ask-me.md) | Router — recommends the right skill for your situation |
| [/grill-with-docs](skills/grill-with-docs.md) | Grilling session that also updates `CONTEXT.md` and ADRs |
| [/triage](skills/triage.md) | Move issues through a triage state machine |
| [/improve-codebase-architecture](skills/improve-codebase-architecture.md) | Scan for architecture weaknesses, produce a report |
| [/setup-skills](skills/setup-skills.md) | Configure skills for a new project — run once |
| [/to-issues](skills/to-issues.md) | Break a plan or PRD into vertical-slice issues |
| [/to-prd](skills/to-prd.md) | Turn the current conversation into a PRD |
| [/prototype](skills/prototype.md) | Build a throwaway prototype to answer a design question |

#### Productivity
| Skill | Description |
|---|---|
| [/grill-me](skills/grill-me.md) | Get relentlessly interviewed until a plan is fully resolved |
| [/handoff](skills/handoff.md) | Compact the session into a handoff doc for another agent |
| [/teach](skills/teach.md) | Learn a concept across multiple sessions with tracked progress |
| [/writing-great-skills](skills/writing-great-skills.md) | Reference for writing and editing skill files |

## How They Work

These are **model-invoked** skills — the agent applies them automatically based on context:

- Writing tests → `testing` rules apply
- Handling user input or auth → `security` rules apply
- Writing UI/HTML → `accessibility` rules apply
- Creating commits or PRs → `git-conventions` and `code-review` rules apply

Rules are treated as non-negotiable defaults unless a project overrides them.

## Manual Setup (No CLI)

Copy individual files into your agent's context directory:

- **Claude Code** → `.claude/skills/` + copy `CLAUDE.md` as-is
- **GitHub Copilot** → `.github/copilot-instructions.md` (copy or append)
- **Cursor** → `.cursor/rules/`
- **Codex** → reference in your system prompt

Both `CLAUDE.md` and `.github/copilot-instructions.md` carry identical rules — only the
filename differs. Keep them in sync when adding or changing skills.

## Source

Inspired by [mattpocock/skills](https://github.com/mattpocock/skills).

