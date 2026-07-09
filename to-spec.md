# /to-spec

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Turn the current conversation into a spec and publish it to the project issue tracker. Does not interview – just synthesizes what has already been discussed.

## When to Use
- After `/grill-me` or `/grill-with-docs` has resolved all ambiguities
- When a long design discussion needs to be captured before it's lost
- When a stakeholder needs a written record of what was agreed

## Spec Format

```markdown
## Problem Statement

The problem that the user is facing, from the user's perspective.

## Solution

The solution to the problem, from the user's perspective.

## User Stories

A numbered list of user stories. Each in the format:

1. As an <actor>, I want a <feature>, so that <benefit>

## Implementation Decisions

A list of implementation decisions that were made. Can include:

- Modules that will be built/modified
- Interface changes
- Architectural decisions
- Schema changes
- API contracts

Do NOT include specific file paths or code snippets – they go stale.

## Testing Decisions

- What makes a good test for this feature
- Which modules will be tested
- Prior art for the tests in the codebase

## Out of Scope

What is explicitly not covered by this spec.

## Further Notes

Any further notes about the feature.
```

## Steps
1. Explore the repo to understand the current state of the codebase if you haven't already. Use the project's domain glossary vocabulary throughout the spec.
2. Sketch out the seams at which you'll test the feature. Prefer existing seams over new ones. Use the highest seam possible – the fewer seams across the codebase, the better. Check with the user that these match their expectations.
3. Write the spec using the format above, then publish it to the project issue tracker. Apply the `ready-for-agent` triage label.

## Rules
- Synthesize – do not pad. If something wasn't discussed, don't invent it.
- Mark genuinely unresolved items in Further Notes, not as decisions.
- Do NOT interview the user – synthesize from what you already know.
- Respect any ADRs in the area you're touching.
