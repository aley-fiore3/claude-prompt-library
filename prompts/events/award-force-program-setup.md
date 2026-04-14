---
title: "Award Force Program Setup & Configuration"
task: events
domain: [events, awards]
complexity: advanced
tags: [award-force, competition, awards, judging, configuration, setup]
claude_model: opus
last_tested: 2026-04-13
---

# Award Force Program Setup & Configuration

## Purpose
Plan and configure an awards or competition program in Award Force — categories, entry forms, judging rounds, scoring, and communications.

## The Prompt

```
Help me set up an awards/competition program in Award Force.

Program: {{PROGRAM_NAME}}
Type: {{PROGRAM_TYPE}}
Categories: {{CATEGORIES}}
Entry requirements: {{REQUIREMENTS}}
Judging structure: {{JUDGING}}
Timeline: {{TIMELINE}}

Design the configuration for:

1. **Categories & Subcategories** — how to structure them in Award Force, including any that share entry forms vs. need unique ones
2. **Entry Form Design** — what fields to include for each category, field types (text, upload, dropdown, etc.), character limits, required vs. optional
3. **Judging Setup**:
   - Judging mode (qualifying, scoring, ranking, or top pick/STV)
   - Number of rounds
   - Score criteria and weights
   - Blind judging settings
   - Judge assignment strategy (how many judges per entry, panel vs. individual)
4. **Scoring Rubric** — specific criteria with point scales and descriptions for each score level
5. **Workflow/Seasons** — how to set up the timeline with open/close dates for entries, judging rounds, and results
6. **Communications** — what automated emails to configure at each stage
7. **Reporting** — what exports and dashboards to set up for tracking

Also flag:
- Common setup mistakes that cause problems later
- Settings that are hard to change once entries start coming in
- How to handle edge cases (late entries, judge conflicts of interest, tied scores)
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROGRAM_NAME}}` | Name | "National Ethics Case Competition" |
| `{{PROGRAM_TYPE}}` | What kind | "Multi-round academic case competition with team submissions and live presentations" |
| `{{CATEGORIES}}` | Entry categories | "Undergraduate Division, Graduate Division, each with Preliminary Round → Semifinal → Final" |
| `{{REQUIREMENTS}}` | What entrants submit | "Written case analysis (PDF, 10-page max), team roster, faculty advisor confirmation, presentation slides" |
| `{{JUDGING}}` | How judging works | "3 judges per entry, blind review of written submission, live scored presentation in later rounds, weighted 40% written / 60% presentation" |
| `{{TIMELINE}}` | Key dates | "Entries open Jan 15, close March 1. Written review March 1-20. Semifinalists notified March 25. Live competition April 16-18. Awards April 19." |

## Usage Notes
- Award Force uses "seasons" for recurring programs — set this up correctly from the start
- The "hard to change once entries start" flag is critical — some settings lock after launch
- Opus handles the multi-round judging logic complexity well

## Tips
- Before configuring, ask: "What's the simplest way to achieve this in Award Force?" — sometimes there's a built-in feature you'd miss
- Chain with: "Write the entry guidelines document that matches this configuration"
- Ask: "Design a judge training document that walks through the scoring rubric with examples"
- For returning programs: "Here's what we did last season — what should we change based on judge feedback?"
