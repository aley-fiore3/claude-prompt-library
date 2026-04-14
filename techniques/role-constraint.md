---
title: "Role + Constraint Framing"
complexity: intermediate
tags: [technique, role-prompting, constraints, claude-specific]
---

# Role + Constraint Framing

## What It Is
Assigning Claude a specific professional role AND pairing it with explicit constraints. The role sets expertise level; the constraints prevent the common failure modes of that role.

## Why It Works
Role-only prompting ("Act as a lawyer") produces generic, verbose output. Adding constraints ("...who bills by the word and hates filler") shapes the output into something actually useful.

## The Pattern

```
Act as a {{ROLE}} who {{CONSTRAINT}}.

{{TASK}}
```

## Examples That Work

### Short, Direct Emails
```
Act as a busy executive who never writes more than 5 sentences.
Draft a follow-up email to the hotel contact about missing AV documentation.
```
*Why it works: The constraint prevents Claude's default tendency to write long, polished emails.*

### Honest Feedback
```
Act as a blunt startup mentor who cares more about saving me time than being polite.
Review this pitch deck outline and tell me what's weak.
```
*Why it works: Without the constraint, Claude defaults to encouraging feedback.*

### Technical Review
```
Act as a Cvent platform specialist who has configured 50+ events.
Review my registration setup and flag anything that will cause problems on launch day.
```
*Why it works: The expertise level ("50+ events") calibrates the depth of the review.*

## Anti-Patterns to Avoid

**Too vague:**
> "Act as an expert." → Expert in what? Claude fills in the gaps generically.

**Role without constraint:**
> "Act as a grant writer." → You'll get a technically correct but bloated draft.

**Contradictory framing:**
> "Act as a creative writer who follows a strict template." → Pick one energy.

## Tips
- Stack roles for cross-domain tasks: "Act as a nonprofit CFO who also understands Cvent event budgeting"
- The constraint should target Claude's specific failure mode for that task
- Test the same prompt with and without the constraint to see the difference
