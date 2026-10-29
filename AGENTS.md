# Agent Skills

A collection of skills for AI coding agents. Works across Claude Code, Cursor, Codex, and Copilot.

## Directory Structure

```
skills/
  {skill-name}/           # kebab-case directory name
    SKILL.md              # Required: skill definition
    references/           # Optional: documentation loaded as needed
    scripts/              # Optional: executable scripts
```

## SKILL.md Format

```markdown
---
name: {skill-name}
description: {One sentence. Include trigger phrases.}
---

# {Skill Title}

{What the skill does, how it works, usage examples.}
```

## Context Efficiency

- Keep `SKILL.md` under 500 lines; move details into `references/`
- Write specific descriptions so the agent knows when to activate
- Use progressive disclosure: reference supporting files that load only when needed
- Prefer scripts over inline code (script execution doesn't consume context)

## Script Standards

- Use `#!/bin/bash` shebang
- Use `set -e` for fail-fast behavior
- Write status messages to stderr: `echo "Message" >&2`
- Write machine-readable output (JSON) to stdout
- Include a cleanup trap for temp files

## Editing Skills

- Prefer surgical changes, don't reformat unrelated markdown
- Information lives in `SKILL.md` or references, not both

## Writing Skills Structure (maintain this)

- Anything that applies to ALL the writing skills (voice, tone, terminology, grammar, structure, banned lists, the review pass) lives in `shared/references/wordpress-brand-writing-style-guide.md` and nowhere else. A `SKILL.md` points to it by section; it never restates it
- Anything specific to content published on WordPress.org/news lives in `shared/references/wordpress-news-post-rules.md`, loaded by every skill that produces News content. Other channel-specific rules live in that channel's `SKILL.md`
- A channel rule may override the guide only where it says so explicitly
- Every writing skill is a single entry point that drafts, then runs the guide's Section 16 review pass as a separate step, then its own format checklist. Never require a second skill for review
- Evaluation fixtures live in `shared/references/evaluation-cases.md` and are not loaded at runtime

## Key Files

- `.claude-plugin/marketplace.json`: Plugin manifest
- `README.md`: Lists available skills
- `shared/references/wordpress-brand-writing-style-guide.md`: The brand guide every writing skill loads
- `shared/references/wordpress-news-post-rules.md`: Format rules for WordPress.org/news content
- `shared/references/evaluation-cases.md`: Maintenance-only evaluation fixtures

## Plan Mode

- Make the plan extremely concise. Sacrifice grammar for the sake of concision.
- At the end of each plan, give me a list of unresolved questions to answer, if any.
