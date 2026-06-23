# /ask-me

**Type:** User-invoked  
**Category:** Engineering

## Purpose
A router. When you're not sure which skill or workflow fits your situation, invoke this
and the agent will ask you a few questions, then recommend the right skill to use.

## Steps
1. Ask the user: "What are you trying to do right now?" — accept a free-form answer.
2. Ask one follow-up to clarify scope if the answer is ambiguous.
3. Map the answer to the most relevant skill(s) from the available list.
4. Explain briefly why each recommended skill fits, and what it will do.
5. Ask: "Want me to start one of these now?" — if yes, invoke it immediately.

## Available Skills to Route To
- `/grill-me` — clarifying a plan or design before building
- `/grill-with-docs` — same, but also builds domain docs
- `/tdd` — building or fixing something with a test-first loop
- `/diagnosing-bugs` — tracking down a hard bug
- `/to-prd` — turning a conversation into a spec
- `/to-issues` — breaking a spec into tickets
- `/triage` — triaging an issue backlog
- `/prototype` — exploring a design with throwaway code
- `/improve-codebase-architecture` — auditing the codebase for design problems
- `/handoff` — compacting the session for another agent
- `/teach` — learning a concept step by step

## Rules
- Never recommend more than two skills at once — pick the most relevant.
- If nothing fits, say so and ask what the user needs instead of guessing.

