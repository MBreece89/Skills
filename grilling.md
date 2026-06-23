# grilling

**Type:** Model-invoked  
**Category:** Productivity

## Purpose
The reusable interview loop behind `/grill-me` and `/grill-with-docs`. Interviews the
user relentlessly about a plan or design until every branch of the decision tree is
resolved. Do not skip this — misalignment is the #1 failure mode in AI-assisted dev.

## When to Apply
Invoked by `/grill-me` or `/grill-with-docs`. Also apply proactively when:
- The user's request is ambiguous or underspecified
- The scope of a change is unclear
- Multiple valid approaches exist and the user hasn't expressed a preference

## The Loop

### Round 1 — Understand the Goal
Ask: "What are you trying to build or change, and why?"
- Accept a free-form answer.
- Identify the top 2–3 things that are still unclear or underspecified.

### Round 2 — Drill Into Ambiguities
For each unclear thing, ask one focused question. Examples:
- "Who is the user of this feature?"
- "What happens in the error case?"
- "Is this replacing existing behaviour or adding to it?"
- "What does success look like?"
- "Are there constraints I should know about (performance, backwards compat, deadlines)?"

### Round 3 — Stress Test
Raise edge cases and failure modes the user may not have considered:
- "What if X is null / empty / unavailable?"
- "What happens if two users do this simultaneously?"
- "Is there a case where we'd want to undo this?"
Push until the user has a concrete answer or explicitly defers it.

### Round 4 — Confirm
Summarize what you've learned in plain language. Ask:
"Does this match what you have in mind? Anything I've missed or got wrong?"
Do not proceed until the user confirms.

## Rules
- Ask one question at a time — never a list of questions in one message.
- Never answer your own questions — keep the user talking.
- Treat "I'm not sure" as an open branch, not an answer — probe further.
- Stop when the user confirms the summary is correct, not before.

