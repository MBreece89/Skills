# /teach

**Type:** User-invoked  
**Category:** Productivity

## Purpose
Teach the user a new skill or concept over multiple sessions, using the current directory
as a stateful teaching workspace. Tracks progress across sessions so teaching continues
where it left off.

## When to Use
- When the user wants to understand something deeply, not just use it
- When learning a new technology, pattern, or discipline hands-on
- When past sessions have covered some material and more remains

## How State Works
Progress is stored in `docs/teaching/[topic-slug]/progress.md`. Each session:
1. Opens that file to see what's been covered
2. Picks up from the last stopping point
3. Updates the file at the end with what was taught

## Session Structure

### Opening
1. Ask (first session): "What do you want to learn, and why?"
2. Identify the user's current level: "What do you already know about [topic]?"
3. On subsequent sessions: read `progress.md` — summarise where we left off in one sentence.

### Teaching
4. Teach one concept at a time. For each concept:
   - Explain it in plain language (no jargon unless introduced deliberately)
   - Give a concrete example — preferably in the user's current codebase
   - Ask a check question: "How would you apply this to [X]?"
   - Do not move on until the user can explain it back
5. Keep sessions to 3–5 concepts max — depth over breadth.

### Exercises
6. After each concept, give a small hands-on task:
   - "Try writing [X] in this file — I'll review it when you're done."
   - Review what they produce: acknowledge what's right, correct what's wrong, explain why.

### Closing
7. Summarise the session: what was covered, what the user demonstrated understanding of.
8. Update `docs/teaching/[topic-slug]/progress.md`:

```markdown
# [Topic] — Teaching Progress

## Covered
- [Concept 1] — [date] — [user demonstrated: yes/partially/not yet]
- [Concept 2] — ...

## Next Session
[What to cover next and any prerequisites]

## Notes
[Any areas the user is struggling with or wants to revisit]
```

## Rules
- Never move on if the user can't explain the concept back — revisit it.
- Prefer examples from the user's own codebase over abstract toy examples.
- Teaching is not lecturing — ask questions throughout, don't monologue.

