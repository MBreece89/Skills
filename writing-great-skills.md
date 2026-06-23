# /writing-great-skills

**Type:** User-invoked  
**Category:** Productivity

## Purpose
Reference for writing and editing skills well. Use this when creating a new skill file
or reviewing an existing one. A good skill is predictable, actionable, and scoped.

## The Two Types of Skills

| Type | Who invokes it | Purpose |
|---|---|---|
| **User-invoked** | You, by typing `/skill-name` | Orchestrates a workflow or session |
| **Model-invoked** | The agent automatically | Holds reusable discipline or a loop |

A user-invoked skill may invoke model-invoked skills.  
A user-invoked skill must never invoke another user-invoked skill.

## What Makes a Skill Good

### Scoped
- Covers exactly one discipline or workflow — not two.
- If you can't name it with a noun or a short verb phrase, it's too broad.

### Actionable
- Every rule must describe a specific action, not a vague intention.
  - ❌ "Write good tests" 
  - ✅ "Name tests: `'should [expected] when [condition]'`"
- If a rule requires judgement to apply, make the judgement criteria explicit.

### Predictable
- Two different agents following this skill should produce the same behaviour.
- Avoid words like "consider", "try to", "may", "where appropriate."
  Use "must", "always", "never", "ask the user for X before doing Y."

### Minimal
- Remove anything the agent would do correctly without being told.
- Trim until removing one more rule would make the skill worse.

## Required Sections
Every skill file must have:
- `# skill-name` — title matching the filename
- `**Type:**` — User-invoked or Model-invoked
- `**Category:**` — Engineering or Productivity (or your custom category)
- `## Purpose` — one sentence
- `## When to Use` / `## When to Apply` — specific trigger conditions
- Steps or process — numbered if ordered, bulleted if not
- `## Rules` — non-negotiable constraints listed last

## Format Rules
- Title matches the filename exactly (no `/` prefix in the file, only when invoking)
- Sections use `##`, sub-sections use `###`
- Rules are bulleted, not numbered — order doesn't imply priority
- Use backticks for file names, paths, and code
- Keep files under 80 lines where possible — if longer, consider splitting

## After Writing
- Test the skill: invoke it with the agent and see if the output is what you expected.
- Add a changeset entry: what was added or changed and why.
- Update `CLAUDE.md` and `.github/copilot-instructions.md` if the skill table needs updating.

