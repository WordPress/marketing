---
name: wordpress-writer-news-release
description: >-
  Draft a WordPress version release announcement for WordPress.org/news in
  the Releases category: a major release (the "X.Y" general availability
  post with the jazz artist tribute), a Beta 1 or later beta post, a release
  candidate (RC1 or later) post, a maintenance release, a maintenance and
  security release, or a security-only release. Use when the user asks to
  write, draft, prepare, update, or revise any of these, including "the 7.2
  Beta 3 post," "the RC1 announcement," "the 7.1.5 maintenance release
  post," "the GA post," or "the release post for X.Y." Reproduces the
  standing structure and copy of the current WordPress release posts,
  derived from every release post since 6.0, fills in the release-specific
  facts from the sources supplied, and runs the brand review pass. For any other WordPress.org/news post, use
  wordpress-writer-news; for a WordCamp recap, use
  wordpress-writer-news-event-recap.
---

# WordPress Writer: News Release

You are drafting a version release announcement for WordPress.org/news. Release posts are the most templated content the project publishes: each type of post has kept the same shape, section order, and standing copy across many releases, and readers, translators, hosts, and the press rely on that consistency. The job is to reproduce the established format exactly and to write the release-specific parts well.

Before drafting, read two shared references and one release-type reference. This skill restates none of them; it covers only what is specific to release posts.

1. **WordPress Brand Writing Style Guide:** voice, tone, terminology, grammar, structure, the banned lists, and the review pass.
   - Local: [WordPress Brand Writing Style Guide](../../shared/references/wordpress-brand-writing-style-guide.md)
   - Canonical: https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-brand-writing-style-guide.md
   - Raw Markdown to fetch: https://raw.githubusercontent.com/WordPress/marketing/main/shared/references/wordpress-brand-writing-style-guide.md
2. **WordPress.org/news Post Rules:** everything specific to a News post.
   - Local: [WordPress.org/news Post Rules](../../shared/references/wordpress-news-post-rules.md)
   - Canonical: https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-news-post-rules.md
   - Raw Markdown to fetch: https://raw.githubusercontent.com/WordPress/marketing/main/shared/references/wordpress-news-post-rules.md
3. **The reference for the release type** you are writing, from this skill's `references/` directory. Load only the one that applies:
   - [Major release](references/major-release.md): the "WordPress X.Y" general availability post
   - [Beta release](references/beta-release.md): Beta 1 and every later beta
   - [Release candidate](references/release-candidate.md): RC1 and every later RC
   - [Maintenance release](references/maintenance-release.md): maintenance, and maintenance and security
   - [Security release](references/security-release.md): security-only, fast-follow, and combined posts

Resolve local paths relative to this `SKILL.md`. Use the two shared references from the same local checkout when available. If either is unavailable, fetch both canonical raw URLs for this run; do not mix local and published references. If you cannot retrieve the complete pair, say so and ask for the missing material before drafting.

**Precedence:** this skill and its type references override both shared references wherever they differ; the News Post Rules override the guide; the guide applies wherever all are silent. The places this skill knowingly departs from the News Post Rules and the guide are listed under "Where release posts differ."

---

## Identify the release type

Decide the type before anything else. The type reference sets the title, the section order, and the standing copy.

| Type | Version pattern | Published when | Typical length (prose, excluding name lists) |
|---|---|---|---|
| Major release | X.Y, with a jazz artist code name | Release day, at the end of the release party | 1,000 to 2,000 words plus squad list, credits, and images |
| Beta 1 | X.Y Beta 1 | Start of the beta phase | 1,300 to 2,200 words |
| Later beta | X.Y Beta 2, 3, 4, 5 | Weekly during the beta phase | 600 to 1,100 words |
| RC1 | X.Y RC1 | Start of the release candidate phase | 1,000 to 1,600 words |
| Later RC | X.Y RC2, 3, 4 | Weekly until release | 800 to 1,300 words |
| Maintenance | X.Y.Z, bug fixes only | After its own RC on Make/Core | 200 to 400 words plus names |
| Maintenance and security | X.Y.Z, bug fixes and security fixes | Same day the fixes ship | 350 to 650 words plus names |
| Security | X.Y.Z, security fixes only | Same day the fixes ship, often with no RC | 230 to 600 words plus names |

Edge cases:

- **Silent betas and RCs** (an extra milestone the squad adds mid-cycle) may be announced on Make/Core rather than News, and the technical leads sometimes write those posts themselves. Confirm where the post will publish and who is writing it before drafting; when it goes on News (7.0 Beta 5 and 7.0 RC4 did), it follows the normal beta or RC structure.
- **A fast-follow release** that fixes a regression from a release published hours or a day earlier, and a **combined post** that announces a minor release and a beta together, follow the patterns in the security reference.
- **A minor release's RC post** goes on Make/Core and is out of scope for this skill.

---

## Inputs

Ask for what the type reference lists under "Facts to collect" before drafting. Do not draft around a missing version number, date, or link. The sources are evidence for facts and scope; apply the WordPress voice independently of how a source phrases things (guide Section 12). Never invent names, numbers, quotes, dates, ticket numbers, or version details.

Sources release posts draw on, in order of authority for a given claim:

- **The release squad and release leads:** feature list and priorities, counts of fixes, the squad roster, the schedule, and anything the post should call out. Treat counts as provisional until the squad confirms them on the day.
- **Make/Core posts:** the release schedule post, dev notes (`https://make.wordpress.org/core/tag/dev-notes+X-Y/`), the Field Guide, "What's new in Gutenberg" posts, and the minor release's RC post.
- **Trac and GitHub:** closed-ticket queries, changesets, and pull requests for ticket references and counts.
- **The Security Team:** the list of vulnerabilities, reporter credits, severity wording, backport status, and advisory links. Reproduce these exactly as supplied; do not add detail about a vulnerability from any other source.
- **The previous post of the same type:** for continuity (the Beta 1 link, the schedule link, the squad roster, phrasing of a feature introduced earlier in the cycle). Use the URL the user gives, or find it in the Releases category at https://wordpress.org/news/category/releases/.
- **The handbook:** the Marketing and Communications Release Cycle Guide covers the process around these posts (timelines, who reviews, the CMS checklist, the jazz artist protocol). Local copy: [`handbook/resources/marketing-communications-release-cycle-guide.md`](../../handbook/resources/marketing-communications-release-cycle-guide.md); published at https://make.wordpress.org/marketing/handbook/resources/marketing-communications-release-cycle-guide/.

### The jazz artist (major releases only)

The release's jazz artist is confidential until the post publishes and is shared with the writer a few days before release day. Draft the tribute only when the user supplies the artist. Otherwise leave `[JAZZ ARTIST PASSAGE: supplied on release day]` in place of the opening paragraphs and the title's code name. Never guess, infer, or research a likely artist. When the artist is supplied, biographical facts come from the user or from a reputable reference you fetched during the run; keep the passage to two or three short paragraphs and end it with one sentence that connects the artist to the release.

---

## Standing copy and substitution

Each type reference marks its sections as **standing copy** or **release-specific**.

- **Standing copy** is reproduced as the reference gives it, with only the marked substitutions (version, milestone number, dates, links, counts, names). Standing copy keeps its published wording even where it uses a word from the guide's watch lists. The review pass checks that every substitution is correct and complete; it does not restyle standing copy. When the user supplies newer approved wording for a standing section, use theirs and note the change in an editor note so the reference can be updated.
- **Release-specific copy** (feature descriptions, highlights, the jazz tribute, the welcome summary, security fix lines) is written fresh from the sources and gets the full guide and News review.
- **Drift check:** when you fetched the latest published post of the same type, compare its section set and standing copy with the reference. Follow the reference for the draft; list any differences in an editor note. The reference, not the live post, is the source of structure, because live posts sometimes carry one-off edits and typos.

---

## Workflow

1. **Identify the type** and load its reference.
2. **Collect the facts** the reference lists. Fetch the previous post of the same type for continuity. Ask for anything missing that the draft cannot be published without; use a clearly marked placeholder for anything that is expected to arrive on release day (final counts, the jazz artist, image URLs, the video embed).
3. **Build a silent source bank:** every number with its source and status (confirmed, provisional, needs wiggle room), every link with its status (verified live, supplied, needs confirmation), every named person with their WordPress.org profile URL, and every feature with its source (dev note, Field Guide, squad brief, Gutenberg release post) and the strongest safe verb for it.
4. **Draft** in the order the reference gives, title first, then standing copy with substitutions, then the release-specific sections.
5. **Review** in a separate pass, as guide Section 16 describes: a fresh agent when the runtime offers one, otherwise a deliberate re-read. Grammar first (guide Section 9), then the Section 16 checklist, then the News format checklist, then the release checklist at the end of this file. The reviewer must know which sections are standing copy.
6. **Return the corrected draft** as a draft for human review, followed by the post metadata block and a short list of non-public editor notes: unverified facts, placeholders still in the draft, links that need confirmation, and any drift from the reference.

---

## Writing rules specific to release posts

### Versions, milestones, and dates

- Write the software as "WordPress X.Y" on first mention in a paragraph and "X.Y" after that when the sentence stays clear. A milestone is "WordPress X.Y Beta 2" or "Beta 2," and "WordPress X.Y RC1" or "RC1." Introduce the RC abbreviation the way the standing opener does: the first Release Candidate ("RC1").
- Dates follow guide Section 9: "August 19, 2026." The scheduled release date in beta and RC posts is bold. Say "scheduled" or "planned" for any date that has not happened.
- Code names sit in double quotes after the version: WordPress 7.1 "Mary Lou." Only major releases have one.

### Counts

- Use the number the squad or the Security Team confirms. For counts that may still move on the day (fixes, contributors, first-time contributors, locales), use "more than N" with room below the real figure, as the handbook recommends; "more than 1,000" is safer than "1,123."
- Bold the counts inside the standing count sentence of beta and RC posts, as the reference shows. Do not bold numbers anywhere else.
- Spell out zero to nine and use numerals from 10 (guide Section 9), except inside a sentence the reference marks as standing copy.

### Features and highlights

- Each feature gets what it is, what the reader can now do, and where it lives (Site Editor, post editor, dashboard, `theme.json`, an API). Lead with the user outcome in user-facing sections and with the API or mechanism in the developer section.
- Match the verb to the source. A merged pull request or dev note supports "adds," "introduces," "now supports." A roadmap item or an open ticket supports only "is planned" or "is in progress," and it belongs in an editor note until it has shipped in the milestone.
- Name blocks, screens, and settings exactly as the UI does (Site Editor, Style Book, Command Palette, Notes, Media Library) and follow the guide's capitalization test (Section 5) for everything else.
- Do not promise what a future milestone will contain. A beta post says what is in that beta; later changes are "expected" only when the squad has said so.
- Link each feature to its dev note, ticket, or pull request where the type reference asks for it. A "Learn more:" line lists references as "Trac #NNNNN" and "GitHub #NNNNN"; give the ticket type and number, not the ticket title. (The RC1 ticket list is the one place that pairs each number with its title.)
- Inline code is for literal commands, functions, filenames, and `theme.json` keys only.

### Security fixes

- One list item per vulnerability, in the order and wording the Security Team supplied: the issue as described, then "reported by" and the credit exactly as given (person, organization, link). Keep the Security Team's severity words; add none.
- Never add exploit detail, affected-version analysis, or mitigation advice beyond what the Security Team supplied. The "update immediately" line and the backports paragraph carry the guidance.
- CVE and GHSA references appear only when the Security Team supplies the advisory links.

### People and credits

- Link every named contributor to their WordPress.org profile (`https://profiles.wordpress.org/slug/`), using the name form the squad supplies. Release leads are named in the standing "led by" sentence; the squad list uses the role labels the roster gives.
- Major release credits use the `[wpcredits X.Y]` shortcode in place of a typed list. Minor release credits are a comma-separated, alphabetized list of linked names supplied by the release squad.
- The props line at the end of beta, RC, and maintenance posts credits the people who reviewed the post, by @username, in italics. Leave it as a placeholder until the user names them.

### Haiku

- Beta and RC posts end with a haiku under its own heading; major and minor release posts do not. The handbook calls the haiku optional, so omit it when the user asks, but include one by default for betas and RCs.
- Three lines, roughly five, seven, and five syllables, about the milestone or testing. Keep it plain and universally acceptable: no puns on people's names, no in-jokes, nothing that needs cultural context. Credit a contributor-written haiku in the props line as the reference shows.

### Tone

Release posts are the project speaking plainly about its own software. Enthusiasm comes from what the release does, not from adjectives. The fixed opener lines carry the format's exclamation points; add none in release-specific copy. No self-congratulation outside the standing contributor paragraphs. Positive, forward-looking framing (guide Section 8) applies to removed features and known issues: say what changed and where to follow along, without apology or speculation.

### Where release posts differ

These are the deliberate departures from the News Post Rules and the guide, so the review pass does not "correct" them:

- **Openings:** each type has a fixed opener. Major releases open with the artist tribute, then the "Welcome to WordPress X.Y!" summary that leads with the biggest changes. Betas, RCs, and minors open with their standing availability line. This overrides the News rule to lead with the version and the biggest change.
- **Exclamation points** in standing openers and the "Welcome to WordPress X.Y!" heading stay.
- **Headings:** standing headings keep their published form, including Title Case where the reference shows it. New headings you write (feature H3s and H4s) are sentence case with no final punctuation, per the News rules.
- **Links** are standard Markdown links, because the draft is pasted into the block editor. This replaces the News rules' bold-plus-URL convention. Bold is used for the one-line feature taglines, the counts, the dates, and the bold lines in standing copy.
- **Lists and tables** are routine in this format: the how-to-test table, query link lists, security fix lists, the squad list, and feature bullets in beta posts.
- **Credits:** the squad section, the contributors section, and the props line are part of the format and are not a "credits section" in the sense the News rules discourage.
- **Haiku** in beta and RC posts.
- **Standing copy** keeps its wording even where it contains a watch-list word or an announcement-style phrase.

---

## Output format

Return the post as Markdown that maps directly onto block editor blocks:

- Title on the first line as `# Title`, then the body.
- Headings as `##`, `###`, and `####` exactly as the reference assigns them.
- Buttons as a link on its own line prefixed with `Button:`, for example `Button: [Download WordPress 7.1](https://wordpress.org/wordpress-7.1.zip)`.
- The how-to-test block as a two-column Markdown table.
- Images as `![alt text](IMAGE URL)` with real alt text, or `[IMAGE: description, alt text]` as a placeholder when the asset is not available yet.
- The release video as `[VIDEO: YouTube URL]` or the URL on its own line when supplied.
- The contributor credits shortcode as `[wpcredits X.Y]` on its own line.
- Italic props lines as `*Props to ... for proofreading and review.*`

After the post, add two short blocks that are not part of the published copy:

**Post metadata**

- Slug: the code name only for a major release (`mary-lou`); the default from the title otherwise.
- Categories: Releases only for a major release; Development and Releases for betas and RCs; Releases and Security for any release with a security fix; Releases for a maintenance release.
- Tags: `releases` and the version for a major release; `X.Y`, `development`, and `release` for betas and RCs; `minor-releases` and `releases` for minor releases.
- Author: the release lead for a major release, otherwise the person publishing.
- Excerpt: a custom one- or two-sentence excerpt for a major release; the first paragraph for other types.
- Featured image: the jazz artist release artwork for a major release, with alt text; none required for other types.

**Editor notes (not for publication)**

- Placeholders still in the draft, provisional counts, links that need confirmation, and any drift from the type reference.

---

## Release checklist

Run this after the guide's Section 16 review pass and the News format checklist. Fix what fails. A checklist item never authorizes inventing detail; missing evidence calls for a placeholder and an editor note.

- [ ] The release type is correct and the title follows the type reference's pattern exactly (quotes, capitalization, no colon).
- [ ] Every section in the type reference is present, in the reference's order, and no section from another type has crept in.
- [ ] Every standing-copy substitution is made: version, milestone number, previous milestone, dates, schedule link, Beta 1 link, zip URL, WP-CLI command, Playground link, Trac and GitHub query links with the correct date window, HelpHub link, Field Guide and release notes links.
- [ ] Standing copy is otherwise unchanged; the review did not restyle it.
- [ ] Every count is confirmed by the squad or the Security Team, or hedged with "more than" and listed as provisional in the editor notes.
- [ ] Every feature claim matches a dev note, ticket, pull request, Field Guide entry, or squad brief, and the verb matches that source.
- [ ] Nothing describes a future milestone's contents beyond what the squad has said.
- [ ] Security fix lines reproduce the Security Team's wording and credits exactly; no added severity, exploit, or mitigation detail.
- [ ] Every named person is linked to a WordPress.org profile, and the roster, leads, and reporters match the supplied lists.
- [ ] The jazz artist passage is present only if the user supplied the artist; otherwise the placeholder is in place and the title's code name is blank.
- [ ] Dates use "Month D, YYYY"; release dates in betas and RCs are bold and described as scheduled.
- [ ] Links are standard Markdown links; every URL was supplied, verified live, or marked `[LINK NEEDED: ...]`.
- [ ] Headings you wrote are sentence case; standing headings keep their published form.
- [ ] A beta or RC post ends with a haiku and a props placeholder; a major release post has neither; a minor release post has no haiku, and only the maintenance types carry a props line.
- [ ] The post metadata block and the editor notes are present and sit outside the publishable copy.
- [ ] The WordPress.org/news Post Rules and the brand guide are followed wherever this skill does not say otherwise.
