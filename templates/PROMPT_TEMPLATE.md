# Prompt Template

Use this template when adding a new prompt to the library.

## File Naming

`category/descriptive-name.md` — lowercase, hyphens, no spaces.

## Template

Copy everything below the line into your new file:

---

```markdown
---
title: "Your Prompt Title"
task: writing | coding | research | analysis | productivity | events | business | creative
domain: [tag1, tag2]
complexity: beginner | intermediate | advanced
tags: [searchable, keywords, here]
claude_model: sonnet | opus | haiku
last_tested: 2026-04-13
---

# Your Prompt Title

## Purpose
One sentence: what does this prompt accomplish?

## The Prompt

\```
Paste your exact prompt here. Use {{VARIABLE}} for parts the user should customize.
\```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{VARIABLE}}` | What to put here | "example value" |

## Usage Notes
- When to use this prompt
- What model works best
- Any setup or context needed

## Example Output
> Brief excerpt of what good output looks like.

## Tips
- Variations that work well
- Common mistakes to avoid
- How to chain with other prompts
```
