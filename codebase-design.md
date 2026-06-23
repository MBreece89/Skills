# codebase-design

**Type:** Model-invoked  
**Category:** Engineering

## Purpose
Shared discipline and vocabulary for designing deep modules: a lot of behaviour behind a
small interface, placed at a clean seam, testable through that interface.

The goal is always **depth** — hiding complexity behind a small, stable surface.

## Core Vocabulary

| Term | Definition |
|---|---|
| **Deep module** | High information-hiding: large implementation, small interface |
| **Shallow module** | Low information-hiding: the interface is almost as complex as the implementation |
| **Seam** | A natural boundary where the module can be tested or replaced in isolation |
| **Interface** | Everything a caller needs to know: function signatures, types, side effects, errors |
| **Leakage** | When internal details (types, errors, concepts) escape through the interface |

## When to Apply
- When designing a new module, service, or class
- When reviewing whether a module should be split or merged
- When an interface is changing and the impact needs to be assessed
- When the user is unsure where to draw a boundary

## Principles

### 1 — Favour Depth Over Width
Prefer one function that does a lot over five functions that each do a little.
Ask: "Could a caller do their job by calling just one or two things from this module?"

### 2 — Hide Everything You Can
The interface should expose the minimum needed to use the module. Everything else is private.
Ask: "If I change this internal detail, does any caller need to change? If yes, it's leaked."

### 3 — Place Modules at Clean Seams
A seam is where two parts of the system naturally separate.
Signs of a bad seam:
- Callers need to know about internal ordering or state
- The module can't be tested without pulling in half the system
- Splitting it would require passing data in a circle

### 4 — Write the Interface Before the Implementation
Draft the function signatures and types first. The implementation follows from the interface,
not the other way around. A good interface is usually obvious; a bad one requires explanation.

### 5 — Name Things After What They Do, Not How They Do It
`getUser(id)` not `fetchUserFromDatabaseWithCaching(id)`.
The caller shouldn't need to know how — only what they get and what they must provide.

## Design Review Checklist
- [ ] Does the module have a single, clearly-nameable responsibility?
- [ ] Is the interface smaller than the implementation it hides?
- [ ] Are all errors that a caller needs to handle explicit in the interface?
- [ ] Can this module be tested without mocking more than one external boundary?
- [ ] Would a new developer understand what this module does from its interface alone?

