---
title: "Fitness Program Builder"
task: creative
domain: [wellness, fitness]
complexity: intermediate
tags: [workout, fitness, program, training, pilates, jiu-jitsu, HIIT]
claude_model: sonnet
last_tested: 2026-04-13
---

# Fitness Program Builder

## Purpose
Design a structured multi-week fitness program that combines multiple disciplines and works around your schedule and limitations.

## The Prompt

```
Design a {{DURATION}} fitness program for me.

My disciplines: {{DISCIPLINES}}
Current level: {{LEVEL}}
Weekly availability: {{SCHEDULE}}
Equipment access: {{EQUIPMENT}}
Goals: {{GOALS}}
Limitations/considerations: {{LIMITATIONS}}

For each week, provide:
- Daily workout split (which discipline + focus area)
- Specific exercises with sets/reps or time
- Progression plan (how it gets harder over the weeks)
- Active recovery days with specific activities (not just "rest")
- One benchmark test to measure progress at week 1 and final week

Make it realistic — I need to sustain this alongside a demanding work schedule. If I'm doing too much, say so.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DURATION}}` | Program length | "6-week" |
| `{{DISCIPLINES}}` | What you do | "Pilates, pole fitness, jiu jitsu, HIIT, hiking" |
| `{{LEVEL}}` | Fitness level | "Intermediate — been training consistently for 2+ years" |
| `{{SCHEDULE}}` | Available time | "Mon/Wed/Fri mornings (1 hr), Tue/Thu evenings (45 min), Sat flexible (2 hrs)" |
| `{{EQUIPMENT}}` | What you have | "Pilates reformer at studio, home bands and mat, BJJ gym, outdoor trails" |
| `{{GOALS}}` | What you want | "Build grip strength for jiu jitsu, improve flexibility for pole, maintain cardio endurance" |
| `{{LIMITATIONS}}` | Physical considerations | "Post-surgical recovery — no heavy impact on abdomen for first 2 weeks. MCAS — avoid overheating triggers." |

## Usage Notes
- Include limitations upfront — Claude will modify exercises appropriately
- "If I'm doing too much, say so" prevents Claude from creating an unsustainable program
- Sonnet handles program design well; Opus for injury-specific modifications

## Tips
- Follow up with: "Create a printable weekly tracker for this program"
- Ask: "What's the minimum version of this program if I only have 3 days per week?"
- For Fit Alchemy Club content: "Turn week 1 into a sample workout post for the app"
- Update after 2 weeks: "I'm finding X too easy and Y too hard — adjust"
