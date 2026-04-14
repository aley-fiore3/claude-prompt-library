---
title: "React Component from Description"
task: coding
domain: [web-dev, ai]
complexity: intermediate
tags: [react, frontend, component, tailwind, UI]
claude_model: sonnet
last_tested: 2026-04-13
---

# React Component from Description

## Purpose
Turn a plain-English description into a working React component with Tailwind styling.

## The Prompt

```
Build a React component for {{COMPONENT_DESCRIPTION}}.

Requirements:
- Functional component with hooks
- Tailwind CSS for styling (no separate CSS file)
- Mobile-responsive
- Accessible (proper aria labels, keyboard navigation)
- Include sample data so it renders immediately

Design: {{DESIGN_STYLE}}

The component should be a single file I can drop into a project or use as a Claude artifact.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{COMPONENT_DESCRIPTION}}` | What it does | "A dashboard card that shows lending metrics — total loans, amount deployed, default rate — with sparkline trends" |
| `{{DESIGN_STYLE}}` | Look and feel | "Clean, minimal, dark mode, with accent color #4F46E5" |

## Usage Notes
- Say "Claude artifact" if you want it to render in chat immediately
- Adding "include sample data" prevents the blank-component problem
- Claude handles Tailwind very well — be specific about spacing, colors, and breakpoints

## Tips
- Chain with: "Now add a filter dropdown and animate the transitions"
- If the component is complex, break it up: "First build the data display, then we'll add interactivity"
- Specify "no external dependencies beyond React and Tailwind" to keep it portable
