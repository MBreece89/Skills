# diagnosing-bugs

**Type:** Model-invoked  
**Category:** Engineering

## Purpose
A disciplined diagnosis loop for hard bugs and performance regressions. Forces a
systematic approach rather than random guessing or "just try things."

## When to Apply
- When a bug is non-obvious or has been looked at more than once without resolution
- When a performance regression has appeared but the cause is unknown
- When the user says "I don't know why this is broken"

## The Loop

### Step 1 — Reproduce
Before anything else, establish a reliable reproduction:
- "Can you reproduce this consistently? What are the exact steps?"
- If it's flaky: "Under what conditions does it appear vs. disappear?"
- Goal: a minimal, deterministic reproduction. Do not proceed to Step 2 until you have one.

### Step 2 — Minimise
Strip the reproduction to the smallest possible case:
- Remove unrelated code, data, and configuration
- Replace real data with the simplest input that still triggers the bug
- Confirm the minimal case still reproduces the issue

### Step 3 — Hypothesise
Before looking at the code, form a concrete hypothesis:
- "My best guess is that X is happening because Y."
- List 2–3 plausible causes, ranked by likelihood.
- Do not skip this step — guessing without a hypothesis leads to random changes.

### Step 4 — Instrument
Add observability to test the hypothesis, not to fix it:
- Add logging, assertions, or breakpoints at the exact point where behaviour diverges
- Print intermediate state to understand what the code actually sees
- Measure, don't assume

### Step 5 — Fix
Once the root cause is confirmed:
- Make the smallest possible change that fixes the root cause
- Do not fix symptoms — fix the cause
- Do not refactor while fixing — that's a separate commit

### Step 6 — Regression Test
Add a test that would have caught this bug:
- The test must fail before the fix and pass after
- Name it so it's clear what bug it guards against
- Commit the test and fix together

## Rules
- Never skip Reproduce or Minimise — diagnosing from a fuzzy reproduction wastes time.
- Never make multiple changes simultaneously — change one thing and observe.
- If Step 3's hypothesis is proved wrong, form a new hypothesis — don't just start changing things randomly.

