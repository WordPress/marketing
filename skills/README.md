# Skills

Reusable **skills** for writing and checking content for the WordPress open source project. Each one captures the WordPress.org brand voice, terminology, and editorial conventions so an AI agent can produce on-brand drafts for the project's marketing and communications work.

A *skill* is a largely self-contained capability an AI agent can load on demand. Each skill bundles its instructions and any helper scripts in a single directory and references the shared WordPress Brand Writing Style Guide through a local path with a canonical URL fallback (News skills also load the shared WordPress.org/news Post Rules), so a skills-aware agent can discover it, decide when it applies, and run it.

These skills produce public-facing WordPress content. Treat anything they generate as a draft for human review before it is published under a contributor's name or posted to an official channel.

---

## What's here

| Skill | What it does |
|---|---|
| `wordpress-writer-news/` | Drafts posts for [WordPress.org/news](https://wordpress.org/news/) in the WordPress project voice. Loads the [WordPress Brand Writing Style Guide](https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-brand-writing-style-guide.md) and the [WordPress.org/news Post Rules](https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-news-post-rules.md), drafts, then runs the guide's review pass. |
| `wordpress-writer-news-event-recap/` | Drafts a flagship WordCamp event recap for WordPress.org/news from real event notes and live event sources. Loads the same two references as `wordpress-writer-news` and adds recap-specific structure, sourcing, and a recap checklist. |
| `wordpress-writer-social/` | Turns a single feed item (post title, URL, content) into ready-to-publish, per-platform social copy for X, Bluesky, Threads, Mastodon, Facebook, Instagram, LinkedIn, and Tumblr. |
| `wordpress-writer-showcase/` | Drafts a two-paragraph [WordPress Showcase](https://wordpress.org/showcase/) site description from a submitted Site URL, submitter Description, and Reason for Submission. Reads the live site to ground the copy, and follows the WordPress Brand Writing Style Guide (read from the same local checkout, with a canonical URL fallback). |

`wordpress-writer-news` and `wordpress-writer-news-event-recap` share the WordPress.org/news Post Rules. A change to how News posts are formatted goes in that reference, not in either skill.

---

## How a skill is laid out

Each skill is a directory:

```
skill-name/
├── SKILL.md              Required. Frontmatter (name + description) and the instructions.
├── agents/openai.yaml    Interface metadata: display name, one-line summary, starter prompt.
├── references/           Optional. Bundled documents the skill reads at runtime.
└── scripts/              Optional. Helper scripts the skill can run.
```

The frontmatter `description` in `SKILL.md` is what a skills-aware runtime reads to decide *when* to trigger the skill, so it spells out the situations the skill is for. The body is the instruction set the agent follows.

---

## How to use them

**In a skills-aware agent (the intended path).** Point the agent at this directory, or install a skill into your agent platform. The agent loads each `SKILL.md`, matches the request against the `description`, and runs the skill that fits. `agents/openai.yaml` provides the display name and a `default_prompt` you can use to invoke a skill explicitly, for example:

> Use $wordpress-writer-news to draft a WordPress.org/news post in the WordPress project voice.

**By hand in any LLM client.** A skill is just Markdown. Open its `SKILL.md`, paste the body into your assistant of choice, attach anything it references (the matching WordPress Brand Writing Style Guide, the News Post Rules for News content, your event notes, the feed item), and supply the inputs it asks for.

Because these skills produce public WordPress content, always review and fact-check the output before publishing.

---

## Conventions

- **Keep skills self-contained, with two shared exceptions.** Everything else a skill needs at runtime travels with it: instructions in `SKILL.md`, helpers under `scripts/`, and any skill-specific docs under `references/`. The shared dependencies are the WordPress Brand Writing Style Guide (every writing skill) and the WordPress.org/news Post Rules (skills that produce News content), both loaded from the same local checkout when available. Resolve paths relative to the skill file. If the required local references are incomplete, load the complete reference set from the canonical raw URLs instead; do not mix local and published references. Drafting and review use the same versions.
- **Precedence, most specific wins.** A skill's own instructions override everything else; a channel reference such as the WordPress.org/news post rules overrides the guide; the guide applies wherever both are silent. A more specific layer does not need to announce an override.
- **Anything that applies to all the writing skills goes in the guide.** Voice, tone, terminology, grammar, structure, banned lists, and the review pass live only in the guide. A skill points to the guide by section and never restates it. Channel-specific rules live with the channel: the News rules for WordPress.org/news, otherwise the channel's `SKILL.md`.
- **One skill, two phases.** Each writing skill drafts, then runs the guide's Section 16 review pass as a separate step (a fresh agent when the runtime offers one), then its own format checklist, and returns the corrected draft. A user runs one skill and gets finished writing; no second skill is needed for review.
- **Evaluation fixtures** for maintaining the guide and skills live in `shared/references/evaluation-cases.md` and are not loaded at runtime.
- **Output is a draft.** Every skill here writes or assesses official WordPress content. A person reviews before anything ships.
