---
title: "Award Force Entry Form & Guidelines Writer"
task: writing
domain: [events, awards]
complexity: intermediate
tags: [award-force, entry-form, guidelines, competition, submissions, awards]
claude_model: sonnet
last_tested: 2026-04-13
---

# Award Force Entry Form & Guidelines Writer

## Purpose
Design the entry form fields for Award Force and write the entrant-facing guidelines document.

## The Prompt

```
Design the entry form and write submission guidelines for {{PROGRAM_NAME}}.

Program type: {{TYPE}}
Categories: {{CATEGORIES}}
What entrants submit: {{DELIVERABLES}}
Eligibility: {{ELIGIBILITY}}
Key dates: {{DATES}}

**Part 1: Entry Form Design**
For each form field:
- Field name
- Field type (text, long text, file upload, dropdown, checkbox, date, URL, etc.)
- Required or optional
- Character limit or file size limit
- Help text (what the entrant sees as guidance)
- Validation rules

Group fields logically. Keep the form as short as possible — every extra field reduces completion rate.

**Part 2: Submission Guidelines**
Write a clear, friendly guidelines document that covers:
- Who can enter and eligibility requirements
- What to submit and format requirements (file types, page limits, naming conventions)
- Evaluation criteria (reference the judging rubric)
- Timeline with all key dates
- FAQ (8-10 questions)
- Contact info for questions

Write for {{AUDIENCE_LEVEL}} — don't assume they've done this before.

**Part 3: Common Entrant Mistakes**
List the top 5 mistakes entrants make and how the guidelines prevent them.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROGRAM_NAME}}` | Program name | "National Ethics Case Competition 2026" |
| `{{TYPE}}` | Program type | "Academic team competition" |
| `{{CATEGORIES}}` | Entry categories | "Undergraduate Division, Graduate Division" |
| `{{DELIVERABLES}}` | What's submitted | "Team registration form, written case analysis (PDF, 10 pages max), presentation slides (PPTX), faculty advisor endorsement letter" |
| `{{ELIGIBILITY}}` | Who can enter | "Full-time students at accredited US universities, teams of 3-5 members, one entry per team" |
| `{{DATES}}` | Timeline | "Entries open Jan 15, close March 1. Late entries accepted through March 5 with $50 fee." |
| `{{AUDIENCE_LEVEL}}` | Who's reading | "College students, many entering a competition for the first time" |

## Usage Notes
- "Keep the form as short as possible" prevents overbuilding — every extra field is friction
- The "common mistakes" section is useful for the FAQ and for judge briefings
- Sonnet handles form design and guidelines well

## Tips
- Ask Award Force support about field types before finalizing — some types have hidden features
- Chain with: "Create a pre-submission checklist entrants can use before hitting submit"
- For file uploads, specify: "What file naming convention should we require?"
- Test the form yourself before launch: "Walk me through submitting a test entry and flag any confusing steps"
