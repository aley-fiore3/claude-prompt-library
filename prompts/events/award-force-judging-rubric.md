---
title: "Award Force Judging Rubric & Judge Comms"
task: events
domain: [events, awards]
complexity: intermediate
tags: [award-force, judging, rubric, scoring, judges, communication]
claude_model: opus
last_tested: 2026-04-13
---

# Award Force Judging Rubric & Judge Comms

## Purpose
Design a scoring rubric for Award Force and draft all judge-facing communications — recruitment, onboarding, instructions, and reminders.

## The Prompt

```
Create a judging rubric and judge communication package for {{PROGRAM_NAME}}.

What judges are evaluating: {{EVALUATION_SUBJECT}}
Judging mode in Award Force: {{JUDGING_MODE}}
Number of criteria: {{NUM_CRITERIA}}
Score scale: {{SCALE}}

**Part 1: Scoring Rubric**
For each criterion:
- Name and weight (must total 100%)
- Description of what it measures
- Score descriptors for each level (what does a 1 vs. 3 vs. 5 look like?)
- Common mistakes judges make when scoring this criterion

The rubric should be calibrated so that average entries land in the middle of the scale, not clustered at the top.

**Part 2: Judge Communications**
Write these emails:
1. **Judge Recruitment** — inviting someone to serve as a judge, explaining the commitment
2. **Judge Onboarding** — welcome, platform login instructions, timeline, expectations
3. **Judging Opens** — your assignments are ready, here's how to score, deadline reminder
4. **Mid-Judging Reminder** — progress check, common questions addressed
5. **Judging Complete / Thank You** — appreciation, what happens next, results timeline

Keep judge emails respectful of their time. These are volunteers.

Judge commitment details: {{COMMITMENT}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROGRAM_NAME}}` | Program name | "National Ethics Case Competition 2026" |
| `{{EVALUATION_SUBJECT}}` | What's being judged | "Written ethics case analyses and live team presentations" |
| `{{JUDGING_MODE}}` | Award Force mode | "Scoring with weighted criteria" |
| `{{NUM_CRITERIA}}` | How many criteria | "5 criteria: Ethical Reasoning, Analysis Quality, Practical Application, Communication Clarity, Creativity of Solution" |
| `{{SCALE}}` | Rating scale | "1-5 scale per criterion" |
| `{{COMMITMENT}}` | Time required | "Review 8-10 written submissions (30 min each), score 4 live presentations (15 min each), available April 16-18 in DC" |

## Usage Notes
- The "calibration" instruction prevents score inflation, which is the #1 judging problem
- "Common mistakes judges make" helps build the training document
- Opus writes much better rubric descriptors than Sonnet

## Tips
- Chain with: "Create a 1-page judge quick-reference card I can print and put at each judge's seat"
- Ask: "What happens if two entries tie? Design a tiebreaker protocol."
- For returning programs: "Here's last year's score distribution — was the rubric well-calibrated or do we need to adjust?"
- Test the rubric: "Score this sample entry using the rubric and show your reasoning"
