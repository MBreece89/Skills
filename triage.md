# /triage

**Type:** User-invoked  
**Category:** Engineering

## Purpose
Move issues through a structured triage state machine. Ensures every issue is well-defined,
prioritised, and ready to be worked before it enters a sprint or backlog.

## When to Use
- When reviewing a batch of newly opened issues
- During a regular backlog grooming session
- When an issue has been sitting in an undefined state too long

## The Triage State Machine

```
Inbox → Needs Info → Refined → Prioritised → Ready
                 ↓
              Closed (duplicate / won't fix / out of scope)
```

### States

| State | Meaning |
|---|---|
| **Inbox** | Just created — not yet reviewed |
| **Needs Info** | Missing reproduction steps, acceptance criteria, or context |
| **Refined** | Problem and scope are clear; acceptance criteria written |
| **Prioritised** | Relative priority assigned; effort estimated |
| **Ready** | Fully specified and ready to be picked up |
| **Closed** | Won't be worked — duplicate, out of scope, or resolved elsewhere |

## Steps
1. Ask the user: "Which issue(s) are we triaging?" — accept issue numbers or a list.
2. For each issue, read the current content and determine its state.
3. For each state transition needed, ask the user the minimum questions required:
   - **Inbox → Needs Info / Refined:** Is the problem clear? Are reproduction steps present?
     Are acceptance criteria written?
   - **Needs Info → Refined:** Has the missing info been provided?
   - **Refined → Prioritised:** What is the relative priority? What is the rough effort?
   - **Prioritised → Ready:** Is there anything blocking this from being picked up now?
4. Apply the appropriate label or status change in the issue tracker.
5. Move to the next issue.

## Output
Each issue moved to the correct state with updated labels, acceptance criteria added
where missing, and a brief triage summary comment posted to the issue.

## Rules
- Never mark an issue **Ready** if acceptance criteria are missing.
- Never mark an issue **Closed** without adding a reason in the issue comment.
- One issue at a time — do not batch state changes without reviewing each individually.

