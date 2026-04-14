---
title: "Allergy-Safe Recipe Adapter"
task: productivity
domain: [wellness, health]
complexity: beginner
tags: [allergies, recipe, dietary, histamine, food, adaptation]
claude_model: sonnet
last_tested: 2026-04-13
---

# Allergy-Safe Recipe Adapter

## Purpose
Take any recipe and adapt it to work with complex food allergies and dietary restrictions.

## The Prompt

```
Adapt this recipe to be safe for my dietary restrictions:

My restrictions:
{{RESTRICTIONS}}

Original recipe:
{{RECIPE}}

For each substitution:
- What you're replacing and why it's a problem
- What you're using instead
- How it changes the flavor/texture (be honest)
- Any technique adjustments needed

If more than 50% of the ingredients need changing, tell me — at that point it might be better to suggest a different dish that naturally works with my restrictions.

Rate the adapted version: will it be genuinely good, or just "edible"?
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{RESTRICTIONS}}` | All your allergies/intolerances | "Histamine intolerance (low-histamine diet), plus allergic to: coconut, almonds, peanuts, corn, soy, tomato, garlic, onion. Avoid aged/fermented foods, vinegar, citrus, spinach, avocado, eggplant." |
| `{{RECIPE}}` | The original recipe | Paste the full recipe |

## Usage Notes
- List ALL restrictions upfront — Claude can't adapt what it doesn't know about
- The "genuinely good or just edible" honesty check saves you from making sad food
- Works for restaurant menus too: "Here's the menu — what can I actually eat?"

## Tips
- Build a master restriction list you can paste into any food-related prompt
- Chain with: "Now create a full week of meals that work with my restrictions — no repeats"
- For dining out: "I'm eating at {{restaurant}}. Based on their menu, what should I order and what modifications should I ask for?"
- For travel: "I'm going to {{destination}}. What local dishes naturally fit my restrictions?"
