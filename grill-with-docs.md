# /grill-with-docs

**Type:** User-invoked  
**Category:** Engineering

## Purpose
A grilling session that also builds the project's domain model. Sharpens terminology,
resolves ambiguities, and writes the output into `CONTEXT.md` and ADRs.

## When to Use
- At the start of a new feature or significant change
- When the codebase lacks a shared language or consistent naming
- When you want to align the agent on domain terminology before it writes any code

## Steps
1. Run the `grilling` loop (see `grilling.md`) — interview the user about the plan until
   all branches are resolved.
2. After grilling, extract all domain terms introduced during the session:
   - New entities, concepts, or roles
   - Any jargon, abbreviations, or business-specific vocabulary
3. Open `CONTEXT.md`. If it doesn't exist, create it. Update the **Glossary** section
   with each new term and a one-sentence definition agreed on during grilling.
4. For each significant architectural or design decision made during grilling, create or
   update an ADR in `docs/adr/`. Format: `NNNN-short-title.md`.
5. Summarize what was decided and what the agent now understands — confirm with the user
   before moving on.

## ADR Format
```markdown
# ADR NNNN: Title

**Status:** Accepted  
**Date:** YYYY-MM-DD

## Context
What situation or problem prompted this decision.

## Decision
What was decided.

## Consequences
What becomes easier or harder as a result.
```

## Output
- Updated `CONTEXT.md` with glossary entries
- New or updated ADR file(s) in `docs/adr/`
- A clear summary of the plan, ready to feed into `/to-prd` or `/to-issues`

## Rules
- Never invent domain terms — only record terms the user actually used or agreed to.
- If the user is unsure about a term, leave it as a question in `CONTEXT.md` marked `[TBD]`.

