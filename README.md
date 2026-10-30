# Marketing-Team

The WordPress marketing team is not currently meeting weekly, but this repository remains the place where marketing tasks are organized. Amplification requests for social media and Showcase activities are still running, and you can find out more about them in the following links:
* [Request for Amplification](https://github.com/WordPress/marketing/issues/new?assignees=bjmcsherry&labels=amplification-request&projects=&template=2-request-for-amplification-template.yml&title=%5BAMPLIFY%5D%3A+)
* [WordPress Showcase](https://github.com/WordPress/marketing/wiki/WordPress-Showcase)

----

You can also follow WordPress on social media platforms and help amplify our messages: [WordPress Social Media](https://make.wordpress.org/marketing/handbook/social-media/).

----

## Team handbook

The [Marketing Team Handbook](https://make.wordpress.org/marketing/handbook/) is maintained in [`handbook/`](handbook/). Each page is a Markdown file, and `handbook/manifest.json` maps the files to handbook pages on WordPress.org. Propose changes with a pull request; see [`handbook/README.md`](handbook/README.md) for the conventions and how the sync works.

----

## Marketing skills for AI agents

This repository also hosts a small library of reusable **skills** for AI agents that write and check content in the WordPress project voice. Each skill bundles its own instructions and loads the shared WordPress Brand Writing Style Guide (skills that write for WordPress.org/news also load the shared WordPress.org/news post rules), so a skills-aware agent (or a person working by hand) can produce on-brand drafts for the project's marketing and communications work.

* **wordpress-writer-news**: drafts [WordPress.org/news](https://wordpress.org/news/) posts following the [WordPress Brand Writing Style Guide](https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-brand-writing-style-guide.md) and the [WordPress.org/news post rules](https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-news-post-rules.md).
* **wordpress-writer-news-event-recap**: drafts flagship WordCamp recaps for WordPress.org/news from real event notes and live event sources.
* **wordpress-writer-social**: turns a single feed item into ready-to-publish, per-platform social copy.
* **wordpress-writer-showcase**: drafts a two-paragraph [WordPress Showcase](https://wordpress.org/showcase/) site description from a submitted site.

See [`skills/README.md`](skills/README.md) for what each skill does and how to use it.

The skills are also packaged as an installable plugin. In Claude Code, add this repository as a plugin marketplace, then install the `wordpress-marketing-skills` plugin (listed in the `wordpress-marketing-team` marketplace). The manifests live in [`.claude-plugin/`](.claude-plugin/); see the [plugin marketplace documentation](https://code.claude.com/docs/en/plugin-marketplaces) for the exact `/plugin marketplace add` and `/plugin install` commands.

Everything these skills produce is a draft for human review before it is published under a contributor's name or posted to an official channel.
