# domain-modeling

**Type:** Model-invoked  
**Category:** Engineering

## Purpose
Actively build and sharpen a project's domain model. Challenge terms against the glossary,
stress-test with edge-case scenarios, and update `CONTEXT.md` and ADRs inline.

## When to Apply
- When a new concept appears in the codebase that isn't in the glossary
- When the user uses a term ambiguously or inconsistently
- When naming a new module, type, or function and the right name isn't obvious
- When `/grill-with-docs` has uncovered terminology that needs to be locked in

## The Process

### 1 — Identify the Term
Name the concept being modelled. Ask if needed:
- "What do you call this thing in your domain?"
- "Is this the same as [similar existing term] or different?"

### 2 — Challenge Against the Glossary
Open `CONTEXT.md` and check the Glossary:
- If the term exists: does this usage match the definition? If not, flag the mismatch.
- If the term doesn't exist: draft a definition (see format below).

### 3 — Stress-Test With Scenarios
Before locking in a definition, test it against 2–3 edge cases:
- "Is a [edge case] still a [term] by this definition?"
- "Could [term] and [similar term] ever be confused? How do we tell them apart?"
- Revise the definition until it holds across all scenarios.

### 4 — Update CONTEXT.md
Add or update the glossary entry:
```markdown
**[Term]** — [One-sentence definition. Written in plain language. No jargon.]
```

### 5 — Propagate
If the new/updated term affects existing code:
- Note which files or functions use inconsistent naming
- Suggest a rename — do not rename silently without the user's approval
- If a significant design decision was made about this concept, write an ADR

## Rules
- Never invent domain terms — record only what the user uses or explicitly agrees to.
- Definitions must be one sentence — if it takes more, the concept needs to be split.
- When in doubt between two terms, prefer the one already used in the codebase.
- Domain consistency trumps cleverness — boring, clear names are always correct.

