# /to-issues

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Break any plan, spec, PRD, or conversation into independently-grabbable issues using
vertical slices. Each issue should deliver user-visible value on its own.

## When to Use
- After `/grill-me`, `/grill-with-docs`, or `/to-prd` has produced a plan
- When you have a large feature that needs to be decomposed into tickets
- When a PRD exists but no issues have been created yet

## What a Good Issue Looks Like
- **Title:** `[verb] [what]` — e.g., "Add email validation to sign-up form"
- **Vertical slice:** touches all layers needed to deliver the value (UI, logic, data)
- **Independently deliverable:** can be merged and used without depending on another in-progress issue
- **Small:** completable in one focused session (hours, not days)
- **Acceptance criteria:** 2–5 concrete, testable statements of done

## Steps
1. Read the input (plan, spec, PRD, or conversation summary).
2. Identify the vertical slices — group work by user-visible outcome, not by layer.
   - ❌ Bad slice: "Set up database schema" (no user value on its own)
   - ✅ Good slice: "User can register with email and password"
3. For each slice, draft an issue:
   - Title
   - One-paragraph description: what the user can do after this is done
   - Acceptance criteria (bulleted, testable)
   - Any known dependencies on other issues (list by title, not number)
4. Show all drafted issues to the user. Ask: "Does this look right? Any missing slices,
   or issues that should be merged or split?"
5. After confirmation, create the issues in the configured issue tracker (see `CONTEXT.md`).

## Output
Issues created in the issue tracker, each with title, description, and acceptance criteria.

## Rules
- No issue should depend on another issue that isn't yet merged.
- If a true dependency exists, note it explicitly — don't hide it.
- Never create a spike or research ticket unless the user asks for one.

