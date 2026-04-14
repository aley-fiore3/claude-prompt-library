---
title: "Meeting Follow-Up with Action Items"
task: writing
domain: [general, nonprofit, business]
complexity: beginner
tags: [email, meeting, follow-up, action-items, professional]
claude_model: sonnet
last_tested: 2026-04-13
---

# Meeting Follow-Up with Action Items

## Purpose
Turn messy meeting notes into a clean follow-up email with clear owners and deadlines.

## The Prompt

```
Write a follow-up email after a meeting.

Meeting: {{MEETING_DESCRIPTION}}
Attendees: {{ATTENDEES}}
My raw notes:
{{NOTES}}

Format:
- Open with one sentence of appreciation (not generic — reference something specific from the meeting)
- 3-5 action items, each with: owner, task, deadline
- One sentence about next steps or next meeting
- Under 150 words total

Don't add any action items I didn't mention. Only use what's in my notes.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{MEETING_DESCRIPTION}}` | What the meeting was | "Breakfast with Christian and Jody from Daniels Fund re: scholarship logistics" |
| `{{ATTENDEES}}` | Who was there | "Me, Christian Kalenga, Jody (Daniels Fund)" |
| `{{NOTES}}` | Your raw notes | "Discussed Daimian's scholarship timeline. Jody will send housing stipend details by Friday. I need to submit the acceptance form by April 20. Christian offered to connect us with the ND alumni network." |

## Usage Notes
- "Don't add action items I didn't mention" is critical — Claude loves to invent extra tasks
- The specific appreciation line prevents generic "thanks for your time" openers
- 150-word limit keeps it scannable

## Tips
- Send within 2 hours of the meeting for maximum impact
- If you didn't capture deadlines, ask Claude: "Suggest reasonable deadlines for each item"
- For recurring meetings, create a template with standing sections
