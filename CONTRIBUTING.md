# Contributing to Claude Prompt Library

Thanks for contributing! Here's how to add your prompts.

## Adding a Prompt

1. **Fork** this repo
2. **Copy** `templates/PROMPT_TEMPLATE.md` into the right category folder under `prompts/`
3. **Fill in** the frontmatter (title, task, domain, complexity, tags, model)
4. **Write** your prompt with variables marked as `{{VARIABLE}}`
5. **Include** at least one usage note and one tip
6. **Submit** a pull request

## Guidelines

**Do include:**
- Prompts you've actually used and gotten good results from
- Specific variable placeholders so others can customize
- Notes on which Claude model works best
- Honest tips about what doesn't work

**Don't include:**
- Jailbreak or policy-violation prompts
- Prompts that reproduce copyrighted content
- System prompts from Claude's internal configuration
- Prompts with hardcoded personal/sensitive info

## Frontmatter Tags

**Task** (pick one): `writing`, `coding`, `research`, `analysis`, `productivity`, `events`, `business`, `creative`

**Complexity**:
- `beginner` — single turn, no setup, copy-paste ready
- `intermediate` — may need role-setting, variables, or multi-step
- `advanced` — chains, system prompts, structured output techniques

**Domain** (pick all that apply): `nonprofit`, `cdfi`, `events`, `cvent`, `grants`, `startup`, `pitch`, `policy`, `federal`, `ai`, `automation`, `web-dev`, `travel`, `italian-american`, `culture`, `wellness`, `fitness`, `general`

## File Naming

- Lowercase, hyphens, `.md` extension
- Descriptive: `event-order-review-checklist.md` not `prompt1.md`
- Place in the matching task folder

## Quality Bar

Every prompt should be something you'd actually send to a colleague saying "try this." If it only works sometimes or needs a ton of context, note that honestly.
