# Skills — Agent Instructions

This repository contains engineer-grade coding skill files. When working in a project
that has these skills installed, apply the following rules.

## Reference Skills (Model-invoked automatically)

Apply the relevant skill automatically based on what you are doing:

| When you are… | Apply skill |
|---|---|
| Writing or reviewing tests | `skills/testing.md` |
| Handling user input, auth, secrets, or HTTP | `skills/security.md` |
| Writing any UI component or HTML | `skills/accessibility.md` |
| Writing comments, JSDoc, or a README | `skills/documentation.md` |
| Creating commits, branches, or PRs | `skills/git-conventions.md` |
| Preparing or reviewing a PR | `skills/code-review.md` |
| Designing a module or drawing a boundary | `skills/codebase-design.md` |
| Naming a concept or updating terminology | `skills/domain-modeling.md` |
| Building a feature test-first | `skills/tdd.md` |
| Diagnosing a hard bug or regression | `skills/diagnosing-bugs.md` |
| Interviewing the user about a plan | `skills/grilling.md` |

## Workflow Skills (User-invoked via `/skill-name`)

### Engineering
| Skill | What it does |
|---|---|
| `/ask-me` | Router — recommends which skill fits your current situation |
| `/grill-with-docs` | Grilling session that also updates `CONTEXT.md` and ADRs |
| `/triage` | Move issues through a triage state machine |
| `/improve-codebase-architecture` | Scan for architecture weaknesses, produce a report |
| `/setup-skills` | Configure this skills repo for a new project (run once) |
| `/to-issues` | Break a plan or PRD into vertical-slice issues |
| `/to-prd` | Turn the current conversation into a PRD |
| `/prototype` | Build a throwaway prototype to answer a design question |

### Productivity
| Skill | What it does |
|---|---|
| `/grill-me` | Get relentlessly interviewed until every branch of a plan is resolved |
| `/handoff` | Compact this session into a handoff doc for another agent |
| `/teach` | Learn a concept across multiple sessions with tracked progress |
| `/writing-great-skills` | Reference for writing and editing skill files |

## Rules

- Treat skill rules as **non-negotiable defaults** unless the project explicitly overrides them.
- When writing code that touches multiple disciplines, apply all relevant skills simultaneously.
- If a skill rule conflicts with a project-specific instruction, the project instruction wins.
- Never skip the `code-review` checklist before marking work as complete.
- A user-invoked skill may invoke model-invoked skills, but never another user-invoked skill.
- Do not invent rules not present in the skill files — if guidance is missing, flag it.

## Adding or Modifying Skills

- Each skill must cover exactly one discipline.
- Rules must be concrete and actionable — no vague advice.
- Follow the format in `skills/writing-great-skills.md`.
- After modifying a skill, add a changeset entry describing the change.
- Keep `CLAUDE.md` and `.github/copilot-instructions.md` in sync — they must mirror each other.
