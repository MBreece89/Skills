# /handoff

**Type:** User-invoked  
**Category:** Productivity

## Purpose
Compact the current conversation into a handoff document so another agent (or a future
session) can continue the work without losing context.

## When to Use
- When a session is getting long and a fresh context window would help
- When handing work to a different agent or model
- When finishing for the day and wanting to pick up cleanly tomorrow

## Steps
1. Review the full conversation from the beginning.
2. Produce a handoff document using the format below.
3. Save it to `docs/handoff/YYYY-MM-DD-HH-MM.md` (or ask where to save it).
4. Ask: "Does this capture everything? Anything missing before I hand off?"

## Handoff Document Format

```markdown
# Handoff — [YYYY-MM-DD HH:MM]

## What We Were Doing
[1–2 sentences: the task or feature being worked on]

## Current State
[What is done, what is in progress, what is not started]

## The Plan
[Ordered list of remaining steps to complete the work]

## Decisions Made
- [Decision]: [Rationale] — agreed on [when/why]

## Open Questions
- [Question that still needs an answer before a step can be taken]

## Key Context
[Anything a fresh agent needs to know that isn't obvious from the code:
- Which files are most relevant
- Any gotchas, constraints, or non-obvious behaviour
- Links to relevant issues, PRDs, or ADRs]

## Next Action
[The single next thing the next agent should do to continue]
```

## Rules
- Be ruthlessly concise — the next agent shouldn't have to read a wall of text.
- Include the "Next Action" section — it's the most important line in the document.
- Never summarise decisions that weren't actually made — mark them as Open Questions.

