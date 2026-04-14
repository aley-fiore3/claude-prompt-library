---
title: "XML Structured Prompting"
complexity: advanced
tags: [technique, xml, structured-output, claude-specific]
---

# XML Structured Prompting

## What It Is
Claude responds especially well to prompts that use XML-style tags to organize instructions, context, and expected output. This isn't just formatting — it changes how Claude parses and prioritizes your request.

## Why It Works
Claude's training emphasizes XML structure. Using tags creates clear boundaries between instructions, context, and output format, reducing ambiguity and improving consistency.

## The Pattern

```xml
<context>
Background information Claude needs to understand the task.
Can include documents, data, or situational details.
</context>

<instructions>
What you want Claude to do. Be specific.
- Step 1
- Step 2
- Step 3
</instructions>

<constraints>
Rules Claude must follow:
- Maximum length
- Tone requirements
- What to avoid
</constraints>

<output_format>
How you want the response structured.
Can include headers, sections, or specific fields.
</output_format>

<examples>
<good_example>What a great response looks like</good_example>
<bad_example>What to avoid</bad_example>
</examples>
```

## Real-World Example

```xml
<context>
I'm reviewing hotel event orders for a 200-person conference at The Mayflower Hotel, April 16-19. The event has 8 separate meal functions and 3 breakout rooms running simultaneously.
</context>

<instructions>
Compare the attached EOs against the master schedule. Flag any discrepancy in headcount, timing, or room assignment.
</instructions>

<constraints>
- Only flag genuine issues, not style preferences
- Prioritize as CRITICAL / IMPORTANT / MINOR
- Keep each flag to one sentence
</constraints>

<output_format>
## CRITICAL
- [flag]

## IMPORTANT
- [flag]

## MINOR
- [flag]
</output_format>
```

## Tips
- You don't need to use every tag — pick the ones that help
- `<constraints>` is the most underused and most impactful tag
- Nest tags for complex tasks: `<section><subsection>...</subsection></section>`
- Claude will mirror your structure — if you're organized, the output is organized
