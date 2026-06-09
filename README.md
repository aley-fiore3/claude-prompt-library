# Claude Prompt Library

> 52 battle-tested prompts and 5 techniques for deploying Claude in real client workflows — across nonprofit operations, event management, business automation, and field engagements.

**Built by [Alessandra Desiderio](https://alessandradesiderio.com)** · [Case Studies](https://github.com/aley-fiore3/fiore3-automation-demos) · [Automation Tools](https://github.com/aley-fiore3/event-data-tools)

---

## Why This Exists

When I embed with a client, I'm often standing up AI-assisted workflows in hours, not weeks. That means I can't start from scratch on prompting every time. This library is the playbook I actually use — prompts that have been tested in real engagements, refined based on what actually worked, and structured so a non-technical operator can pick them up and run them.

**How you ask matters as much as what you ask.** This library captures the patterns that consistently produce the best results across Claude models.

---

## What's In Here

| Category | What It Covers | Prompts |
|---|---|---|
| [Writing](prompts/writing/) | Emails, docs, client communications, content | 8 |
| [Coding](prompts/coding/) | Scripts, automation, debugging, web projects | 7 |
| [Research](prompts/research/) | Deep dives, competitive analysis, sourcing | 6 |
| [Analysis](prompts/analysis/) | Data review, strategy, decision-making | 7 |
| [Productivity](prompts/productivity/) | Workflows, checklists, meeting prep | 6 |
| [Events](prompts/events/) | Logistics, Cvent, coordination, run-of-show | 9 |
| [Business](prompts/business/) | Nonprofit, CDFI, grants, entrepreneurship | 6 |
| [Creative](prompts/creative/) | Branding, design briefs, content ideation | 3 |

**→ [VIEW THE MASTER INDEX](INDEX.md)** — every prompt in one searchable table with task, domain, complexity, and tags.

---

## Complexity Levels

| Level | What It Means |
|---|---|
| 🟢 Beginner | Single-turn. Copy-paste and go. |
| 🟡 Intermediate | Multi-step or role-based. May need light customization. |
| 🔴 Advanced | Chains, system prompts, or technique patterns. |

---

## Claude-Specific Techniques

Beyond individual prompts, this library documents five patterns that work especially well with Claude:

**1. XML Structured Prompting** — Use `<context>`, `<task>`, and `<constraints>` tags to separate what Claude needs to know from what it needs to do. Dramatically reduces ambiguity on complex tasks.

**2. Role + Constraint Framing** — Tell Claude who it is *and* what it cannot do. The constraint half is often more important than the role.

**3. Iterative Refinement Chains** — Use the output of one prompt as structured input to the next. Particularly powerful for drafting → editing → formatting workflows.

**4. Memory-Aware Prompting** — Structure long conversations so that critical context appears at the start *and* is re-stated before the key ask. Claude performs better when it doesn't have to infer context from conversation history.

**5. Tool-Trigger Prompting** — Design prompts that produce outputs formatted for immediate use by downstream automation (CSV, JSON, markdown tables). Removes the "copy-paste into another system" step entirely.

See [techniques/](techniques/) for full writeups with examples.

---

## Prompt Format

Every prompt uses a consistent frontmatter block:

```yaml
---
title: "Descriptive Name"
task: writing | coding | research | analysis | productivity | events | business | creative
domain: [nonprofit, events, tech, ...]
complexity: beginner | intermediate | advanced
tags: [specific, searchable, tags]
claude_model: sonnet | opus | haiku
---
```

Followed by: the prompt itself, usage notes, example output, and customization tips.

---

## Related Work

- **[fiore3-automation-demos](https://github.com/aley-fiore3/fiore3-automation-demos)** — Automation demos and case studies showing these prompts deployed in real workflows
- **[event-data-tools](https://github.com/aley-fiore3/event-data-tools)** — Python scripts for data cleaning and reconciliation, used alongside prompt-driven analysis

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add your own prompts. PRs welcome.

## License

MIT — use these prompts however you want. Attribution appreciated but not required.
