---
title: "Memory-Aware Prompting"
complexity: intermediate
tags: [technique, memory, personalization, claude-specific]
---

# Memory-Aware Prompting

## What It Is
Structuring your prompts to work WITH Claude's memory system — giving it the right context hooks so it can personalize responses without you re-explaining your whole life every time.

## Why It Works
Claude's memory builds over time from your conversations. Prompts that reference your known context ("based on what you know about my work") activate relevant memories and produce more tailored output than generic prompts.

## The Pattern

### Trigger Memory
```
Based on what you know about my role and work, {{TASK}}.
```

### Supplement Memory
```
Quick context you might not have: {{NEW_INFO}}.

Now {{TASK}}.
```

### Correct Memory
```
Update: I no longer {{OLD_FACT}}. I now {{NEW_FACT}}.

Remember this going forward.
```

## Examples

### Leveraging Existing Context
```
Based on what you know about my event management work, draft a post-event survey for a 3-day competition with judges, students, and organizers as separate audiences.
```
*Claude already knows your NECC context, Cvent experience, etc. — it'll tailor the survey accordingly.*

### Adding Temporary Context
```
I'm meeting with a potential funder tomorrow who focuses on rural economic development in the Mountain West.

Based on what you know about my organization, what are the 3 strongest talking points I should lead with?
```

### Building Memory Intentionally
```
Please remember: I prefer very short, direct emails — under 100 words whenever possible.
```
*This creates a persistent preference that shapes future email drafts.*

## Tips
- You can ask Claude "What do you remember about me?" to audit its memory
- If Claude's memory seems off, correct it directly — it sticks
- For sensitive topics, use Incognito mode (memory is disabled)
- Don't over-rely on memory for critical facts — confirm if it matters
