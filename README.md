# 🧠 Claude Prompt Library

A curated collection of prompts and techniques for getting the most out of Claude. Built by [Alessandra Desiderio](https://github.com/aley-fiore3) from real-world use across nonprofit development, event management, entrepreneurship, research, and creative work.

## Why This Exists

After hundreds of conversations with Claude, I've found that **how you ask matters as much as what you ask**. This library captures the prompts, patterns, and techniques that consistently produce the best results.

## 🔎 Full Searchable Index

**[→ VIEW THE MASTER INDEX](INDEX.md)** — every prompt in one searchable table with task, domain, complexity, and tags.

## 📂 Browse by Task

| Category | Description | Prompts |
|----------|-------------|---------|
| [Writing](prompts/writing/) | Emails, docs, communications, content | ✉️ |
| [Coding](prompts/coding/) | Scripts, automation, web projects | 💻 |
| [Research](prompts/research/) | Deep dives, comparisons, sourcing | 🔍 |
| [Analysis](prompts/analysis/) | Data review, strategy, decision-making | 📊 |
| [Productivity](prompts/productivity/) | Workflows, checklists, planning | ⚡ |
| [Events](prompts/events/) | Event logistics, Cvent, coordination | 🎪 |
| [Business](prompts/business/) | Nonprofit, CDFI, entrepreneurship, grants | 💼 |
| [Creative](prompts/creative/) | Branding, design briefs, content ideas | 🎨 |

## 🏷️ Browse by Domain

- **Nonprofit / Community Development** — `#nonprofit` `#cdfi` `#grants`
- **Event Management** — `#events` `#cvent` `#logistics`
- **Entrepreneurship** — `#startup` `#pitch` `#business-plan`
- **Policy & Government** — `#policy` `#lobbying` `#federal`
- **Technology / AI** — `#ai` `#automation` `#web-dev`
- **Travel & Culture** — `#travel` `#italian-american` `#culture`
- **Wellness & Fitness** — `#wellness` `#fitness` `#health`

## 📈 Browse by Complexity

| Level | What It Means |
|-------|--------------|
| 🟢 **Beginner** | Simple, single-turn prompts. Copy-paste and go. |
| 🟡 **Intermediate** | Multi-step or role-based prompts. May need customization. |
| 🔴 **Advanced** | Complex chains, system prompts, or technique patterns. |

## 🔧 Prompt Format

Every prompt in this library uses a consistent format:

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

Followed by the prompt itself, usage notes, example output, and tips.

## 🧩 Claude-Specific Techniques

This library also documents **patterns and techniques** that work especially well with Claude:

- [XML Structured Prompting](techniques/xml-structuring.md)
- [Role + Constraint Framing](techniques/role-constraint.md)
- [Iterative Refinement Chains](techniques/iterative-refinement.md)
- [Memory-Aware Prompting](techniques/memory-aware.md)
- [Tool-Trigger Prompting](techniques/tool-triggers.md)

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add your own prompts. PRs welcome!

## 📜 License

MIT — use these prompts however you want. Attribution appreciated but not required.
