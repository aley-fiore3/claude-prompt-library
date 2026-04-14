---
title: "Iterative Refinement Chains"
complexity: advanced
tags: [technique, chaining, multi-turn, claude-specific]
---

# Iterative Refinement Chains

## What It Is
Breaking a complex task into a sequence of prompts where each step builds on the last. Instead of one massive prompt, you run a focused chain.

## Why It Works
Claude produces better output when each turn has a narrow focus. A 3-step chain almost always beats a single mega-prompt for quality.

## The Pattern

```
Step 1: GENERATE → Get a first draft or raw output
Step 2: CRITIQUE → Ask Claude to evaluate its own output
Step 3: REFINE  → Apply the critique to produce a final version
```

## Real-World Example: Grant Narrative

**Step 1 — Generate:**
```
Draft a 500-word grant narrative for a CDFI seeking funding to expand small business lending in rural Colorado. Focus on community impact.
```

**Step 2 — Critique:**
```
Review the narrative you just wrote. Score it 1-10 on:
- Specificity (concrete numbers, names, outcomes)
- Emotional pull (does it make the reader care?)
- Funder alignment (does it speak to what funders want to hear?)

List 3 specific improvements.
```

**Step 3 — Refine:**
```
Rewrite the narrative incorporating all 3 improvements. Keep it under 500 words.
```

## Variations

### The Expert Panel
```
Step 1: Draft the content
Step 2: "Review this as if you were [Expert A]. What would you change?"
Step 3: "Now review as [Expert B]. What would they change?"
Step 4: "Synthesize both reviews into a final version."
```

### The Compression Chain
```
Step 1: Write a comprehensive version (no length limit)
Step 2: "Cut this in half. Keep only what matters."
Step 3: "Cut it in half again. Every word must earn its place."
```
*Great for emails, bios, and pitch language.*

### The Angle Finder
```
Step 1: "Give me 5 different angles for approaching [topic]"
Step 2: "Expand angle #3 into a full draft"
Step 3: "Tighten and polish"
```

## Tips
- Save good chains as reusable sequences — they're your secret weapon
- The critique step is where the magic happens; be specific about evaluation criteria
- Works across models: use Haiku for Step 1, Opus for Step 2-3 if you're on API
