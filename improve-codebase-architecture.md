# /improve-codebase-architecture

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Scan a codebase for architectural weaknesses — modules that are too wide, too shallow,
too coupled, or poorly named — then grill through the most important one and produce an
improvement plan.

## When to Use
- When the codebase feels harder to change than it should
- When adding features keeps requiring edits in many unrelated places
- As a regular audit (recommended: once every few days on fast-moving projects)

## Steps

### Phase 1 — Scan
1. Walk the top-level module/package structure. For each module note:
   - **Width:** how many public exports does it have?
   - **Depth:** how much behaviour does it actually encapsulate?
   - **Coupling:** how many other modules does it import from?
   - **Naming:** does the name accurately reflect what it does?
2. Identify the top 3–5 problem areas using this priority order:
   - Modules that are very wide (many exports) but shallow (little behaviour)
   - High-coupling clusters where changes ripple everywhere
   - Modules with names that no longer match their responsibilities
   - Duplicated logic spread across multiple modules

### Phase 2 — Report
Produce a brief structured report:
```
## Architecture Report

### Problem Areas
1. [module name] — [problem description] — [risk: high/medium/low]
2. ...

### Recommended Focus
[Which problem to tackle first and why]
```

### Phase 3 — Grill
Invoke `grilling.md` on the highest-priority problem. Work through:
- What the module currently does vs. what it should do
- Where the seam should be drawn
- What the new interface should look like
- What tests would prove the refactor is safe

### Phase 4 — Plan
Produce a step-by-step refactor plan. Each step must:
- Be independently committable (no big-bang rewrites)
- Leave the system in a working state
- Include the test that validates it

## Rules
- Do not refactor during the scan — scan first, then plan.
- Never recommend adding abstraction — recommend removing it if the module is too complex.
- Deep modules are the goal: a lot of behaviour behind a small, stable interface.

