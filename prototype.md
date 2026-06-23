# /prototype

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Build a throwaway prototype to flesh out a design. Used when the right approach isn't
clear yet and running code will answer the question faster than discussion.

Prototypes are **disposable** — they prove a concept, not ship to production.

## When to Use
- When you have two or more viable approaches and can't decide without seeing them
- When the business logic is complex enough that a working model would clarify it
- When stakeholders need to react to something visual before committing to a design

## Two Modes

### Mode A — Logic Prototype (Terminal App)
For state, business logic, or algorithm questions where UI doesn't matter.

**Output:** A runnable terminal/CLI app that exercises the core logic with real inputs.

Steps:
1. Ask: "What decision are we trying to make with this prototype?"
2. Identify the minimum logic needed to answer that question — strip everything else.
3. Build a terminal app. It should:
   - Accept inputs (hardcoded or via args — whichever is faster)
   - Exercise the core logic
   - Print output that clearly shows whether the approach works
4. Run it. Show the output.
5. Ask: "Does this answer the question? Do we need to try a different approach?"

### Mode B — UI Prototype (Multiple Variations)
For layout, interaction, or UX questions.

**Output:** Two or more distinct UI variations, togglable from a single route (e.g. `?variant=A`).

Steps:
1. Ask: "What interaction or layout question are we trying to answer?"
2. Propose 2–3 radically different approaches (not minor tweaks — genuinely different).
3. Confirm the approaches with the user before building.
4. Build all variations, toggleable via a query param or feature flag.
5. Show the user how to switch between them.
6. Ask: "Which direction feels right? Do any of these get close?"

## Rules
- **Throwaway only.** Do not use production patterns, proper error handling, or tests.
  Label the prototype directory `_prototype/` or add a `PROTOTYPE.md` warning.
- **Time-box it.** If a prototype is taking longer than one session, it's too big.
- **Never ship prototype code.** If the prototype wins, rewrite it properly — don't promote it.

