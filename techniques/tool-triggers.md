---
title: "Tool-Trigger Prompting"
complexity: advanced
tags: [technique, tools, search, artifacts, claude-specific]
---

# Tool-Trigger Prompting

## What It Is
Phrasing your prompts to activate Claude's built-in tools (web search, file creation, code execution, image search, maps, calendar, etc.) intentionally rather than accidentally.

## Why It Matters
Claude has access to many tools but only uses them when the prompt signals the need. Knowing the trigger words means you control what Claude does vs. just talks about.

## Tool Triggers

### Web Search
**Triggers:** "current," "latest," "today," "now," "recent," "who is the current," "what's the price of"
```
What are the latest CDFI Fund grant deadlines?
```
*Claude will search the web rather than guess from training data.*

### File Creation
**Triggers:** "create a document," "write a report," "make a spreadsheet," "build a presentation"
```
Create a Word document with a summary of our Q1 lending activity.
```
*Claude will actually produce a .docx file, not just show you text.*

### Code Execution
**Triggers:** "calculate," "run this," "analyze this data," "plot," "chart"
```
Calculate the compound interest on a $50K loan at 6.5% over 10 years and show me a chart.
```

### Image Search
**Triggers:** Asking about visual things — places, products, styles, people, animals
```
What does the Mayflower Hotel ballroom look like?
```

### Maps & Places
**Triggers:** "find restaurants near," "show me," "where is," "plan a route"
```
Find Italian restaurants near the Mayflower Hotel in DC.
```

### Calendar & Reminders
**Triggers:** "schedule," "remind me," "add to calendar," "what's on my calendar"
```
Add a reminder to follow up with the hotel contact on Thursday.
```

## Anti-Triggers (When You DON'T Want Tools)

Sometimes Claude reaches for a tool when you just want a conversation:
```
Don't search for this — just based on your training, what do you know about CDFI certification requirements?
```

Or when you want text, not a file:
```
Give me a quick summary in chat — don't create a document.
```

## Tips
- If Claude didn't use the tool you expected, rephrase with a stronger trigger
- You can explicitly say "use web search" or "create a file" — Claude follows direct instructions
- Chain tools: "Search for X, then create a spreadsheet comparing the results"
