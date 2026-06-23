# /setup-skills

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Configure this skills repo for a new project. Sets up the issue tracker integration,
triage label conventions, and domain doc layout. Run once per project.

## Steps

### Step 1 — Issue Tracker
Ask: "Which issue tracker are you using?"
- **GitHub Issues** — default; no extra setup needed
- **Linear** — ask for the team key
- **Local files** — issues will be stored as markdown in `docs/issues/`

Record the answer in `CONTEXT.md` under `## Project Setup`.

### Step 2 — Triage Labels
Ask: "What labels do you use on issues when triaging?"
- Suggest defaults if none: `needs-info`, `refined`, `prioritised`, `ready`, `wont-fix`
- Record agreed labels in `CONTEXT.md` under `## Triage Labels`

### Step 3 — Domain Docs Layout
Ask: "Where do you want to store documentation created by skills (ADRs, PRDs, etc.)?"
- Suggest defaults: `docs/adr/`, `docs/prd/`, `docs/issues/`
- Create those directories with a `.gitkeep` if they don't exist

### Step 4 — CONTEXT.md
Create or update `CONTEXT.md` with the answers from steps 1–3. Template:

```markdown
# Project Context

## Project Setup
- **Issue tracker:** [GitHub Issues / Linear / Local]
- **Team key (if Linear):** [key]

## Triage Labels
- needs-info, refined, prioritised, ready, wont-fix

## Docs Layout
- ADRs: docs/adr/
- PRDs: docs/prd/
- Issues: docs/issues/

## Glossary
<!-- Domain terms added by /grill-with-docs will appear here -->
```

### Step 5 — Confirm
Show the user the created/updated `CONTEXT.md` and confirm everything looks right.

## Rules
- Never overwrite existing `CONTEXT.md` content — append or update sections only.
- If the user skips a step, record the default and note it can be changed later.

