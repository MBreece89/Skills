# /to-tickets

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Break a plan, spec, or conversation into tracer-bullet tickets – narrow but complete vertical slices, each declaring its blocking edges, published to the configured issue tracker.

## When to Use
- After `/to-spec` has produced a spec
- When a large feature needs to be decomposed into independently-workable tickets
- When you need a dependency-ordered queue of work an agent can grab one at a time

## What a Good Ticket Looks Like
- **Vertical slice:** cuts through every layer (schema, API, UI, tests) – not a horizontal slice of one layer
- **Independently verifiable:** can be merged and confirmed working on its own
- **Sized for one context window:** completable in a single fresh agent session
- **Blocking edges declared:** lists the other tickets that must finish before it can start

## Steps
1. Gather context from whatever is already in the conversation. If the user passes a spec path or issue URL, fetch and read it in full.
2. Explore the codebase if needed. Ticket titles and descriptions should use the project's domain glossary and respect ADRs in the area you're touching. Look for prefactor opportunities – "make the change easy, then make the easy change."
3. Draft vertical slices. Give each ticket its blocking edges. A ticket with no blockers can start immediately.
4. Present the breakdown to the user – for each ticket show: title, blocked by, and what it delivers. Ask if the granularity feels right, whether blocking edges are correct, and whether any tickets should be merged or split. Iterate until the user approves.
5. Publish the approved tickets to the configured tracker in dependency order (blockers first). Apply the `ready-for-agent` triage label. Use native blocking/sub-issue relationships where the tracker supports them.

## Rules
- Each ticket is a vertical slice, not a layer (no "set up database schema" tickets).
- Wide refactors are the exception: sequence them as expand → migrate batches → contract, each as its own ticket.
- Do NOT close or modify any parent issue.
- Avoid specific file paths or code snippets in tickets – they go stale fast.
- Work the frontier one ticket at a time with `/implement`, clearing context between tickets.
