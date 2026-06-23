# /to-prd

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Turn the current conversation into a PRD (Product Requirements Document) and publish it
to the issue tracker. Does not interview — just synthesizes what has already been discussed.

## When to Use
- After `/grill-me` or `/grill-with-docs` has resolved all ambiguities
- When a long design discussion needs to be captured before it's lost
- When a stakeholder needs a written record of what was agreed

## PRD Format

```markdown
# PRD: [Feature Name]

**Date:** YYYY-MM-DD  
**Status:** Draft | Accepted | Superseded  
**Author:** [name or "AI-assisted"]

## Problem
What user problem or business need does this address? (2–4 sentences)

## Goals
- [Measurable goal 1]
- [Measurable goal 2]

## Non-Goals
- [What this explicitly does NOT cover]

## Proposed Solution
A plain-language description of what will be built. Enough detail that an engineer
can start scoping work, not so much that it specifies implementation.

## User Stories
- As a [user type], I want to [action] so that [outcome].

## Acceptance Criteria
- [ ] [Concrete, testable criterion]
- [ ] ...

## Open Questions
- [Anything still unresolved — owner and deadline if known]

## Dependencies
- [Other systems, teams, or issues this depends on]
```

## Steps
1. Review the conversation so far — extract goals, decisions, and constraints.
2. Draft the PRD using the format above. Fill every section; use "N/A" only if a section
   genuinely does not apply.
3. Show the draft to the user. Ask: "Does this capture everything? Anything wrong or missing?"
4. Apply any corrections.
5. Save the PRD to `docs/prd/NNNN-short-title.md` and create a linked issue in the
   issue tracker pointing to it (or create the issue body from the PRD content directly,
   depending on the tracker).

## Rules
- Synthesize — do not pad. If something wasn't discussed, don't invent it.
- Mark genuinely unresolved items as Open Questions, not decisions.
- The PRD is a snapshot of what was agreed — update it if decisions change.

