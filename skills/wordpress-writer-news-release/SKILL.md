---
name: wordpress-writer-news-release
description: >-
  Draft or revise WordPress.org/news version release announcements, including
  major (GA), beta, release candidate, maintenance, security, and combined
  release posts, using release-specific sources and the WordPress brand review.
---

# WordPress Writer: News Release

Draft a WordPress.org/news release announcement using the release-type reference as the default structure. Preserve wording explicitly designated as approved boilerplate, while verifying every factual assertion and substitution. Adapt conditional sections to the release, and flag conflicts between the template and current authoritative evidence.
Read both shared references and the applicable release-type reference. Shared voice and mechanics live in those references; this skill owns release-specific decisions.

1. **WordPress Brand Writing Style Guide:** voice, tone, terminology, grammar, structure, the banned lists, and the review pass.
   - Local: [WordPress Brand Writing Style Guide](../../shared/references/wordpress-brand-writing-style-guide.md)
   - Canonical: https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-brand-writing-style-guide.md
   - Raw Markdown to fetch: https://raw.githubusercontent.com/WordPress/marketing/main/shared/references/wordpress-brand-writing-style-guide.md
2. **WordPress.org/news Post Rules:** everything specific to a News post.
   - Local: [WordPress.org/news Post Rules](../../shared/references/wordpress-news-post-rules.md)
   - Canonical: https://github.com/WordPress/marketing/blob/main/shared/references/wordpress-news-post-rules.md
   - Raw Markdown to fetch: https://raw.githubusercontent.com/WordPress/marketing/main/shared/references/wordpress-news-post-rules.md
3. **The reference for the release type** you are writing, from this skill's `references/` directory. Load only the references needed for the selected format; a combined post may need two:
   - [Major release](references/major-release.md): the "WordPress X.Y" general availability post
   - [Beta release](references/beta-release.md): the first public preview and subsequent betas
   - [Release candidate](references/release-candidate.md): RC1 and every later RC
   - [Maintenance release](references/maintenance-release.md): maintenance, and maintenance and security
   - [Security release](references/security-release.md): security-only, security-related fast-follow, and combined security/beta posts

Resolve local paths relative to this `SKILL.md`. Use the two shared references from the same local checkout when available. If either is unavailable, fetch both canonical raw URLs for this run; do not mix local and published references. If you cannot retrieve the complete pair, say so and ask for the missing material before drafting.

**Precedence:** this skill and its type references override both shared references wherever they differ; the News Post Rules override the guide; the guide applies wherever all are silent. The places this skill knowingly departs from the News Post Rules and the guide are listed under "Where release posts differ."

---

## Identify the release type

Choose by purpose and contents, then retain the actual version and milestone number. The reference provides a default title, section order, and wording; length follows the available material.

| Purpose and contents | Reference and variant |
|---|---|
| Major release, generally available | Major release |
| First public preview of a release, usually Beta 1 | Beta: first-preview overview, even if numbered Beta 2 or later |
| Subsequent beta | Beta: changes since the previous shipped milestone |
| First or subsequent release candidate | Release candidate: RC1 or later-RC variant |
| Minor release with bug fixes only | Maintenance |
| Minor release with bug fixes and security fixes | Maintenance and security |
| Minor release with security fixes only | Security |

- **Fast-follow is a modifier, not a security classification.** An ordinary regression fix uses the maintenance reference (6.7.1 is an example). A follow-up addressing a security release's regression or incomplete fix uses the security reference's fast-follow variant. Explain the connection from the supplied evidence; do not invent new vulnerabilities or security urgency.
- **Combined security/beta announcement:** load the security reference's combined variant and the beta reference for testing instructions. Keep the stable and prerelease versions, audiences, and actions distinct. For other combinations, compose the relevant formats from the brief rather than assuming a security event.
- **Skipped or silent milestones:** identify the first public preview and the previous shipped build from current release evidence, not numbering or the last News post alone. 6.3 began with Beta 2; some builds appear only on Make/Core or within another announcement. Use their actual names in links, counts, and date windows.
- This skill targets News. A minor release's RC announcement belongs on Make/Core. For an unplanned milestone, use the publication destination already supplied; clarify only when it is genuinely uncertain.

---

## Inputs

Use the type reference's facts list as a research checklist. Read supplied material and retrieve relevant public sources before asking for missing information. Ask when an unresolved choice changes the draft's direction, such as which release or audience it covers. A missing date, count, link, roster, or asset need not block supported sections: use a descriptive placeholder or omit an optional claim, and list the publication requirements in editor notes. Never present placeholders or provisional facts as verified.

Choose authority by the claim:

- **Release squad and current release records:** priorities, schedule, roster, counts, and confirmation that a feature is included in the target build. Recheck provisional figures before publication.
- **Make/Core, release notes, and Field Guide:** release-specific technical scope, schedules, dev notes, and minor-release RC summaries.
- **Trac and GitHub:** implementation evidence, target-branch inclusion, changesets, backports, and reversions. A merged Gutenberg change alone does not establish inclusion in WordPress.
- **Security Team:** approved vulnerability descriptions, severity, reporter attribution, affected branches, backport status, and advisories. These take precedence for security claims; do not expand them from other sources.
- **Prior announcements:** continuity and format examples, not authority for current facts. Find them in the [Releases archive](https://wordpress.org/news/category/releases/) and relevant Make/Core announcements. Do not carry forward rosters, dates, or feature scope without checking.
- **Release process:** [Marketing and Communications Release Cycle Guide](../../handbook/resources/marketing-communications-release-cycle-guide.md), also [published on Make/Marketing](https://make.wordpress.org/marketing/handbook/resources/marketing-communications-release-cycle-guide/). Consult the relevant section when process details matter.

### The jazz artist (major releases only)

The release's jazz artist is confidential until the post publishes and is shared with the writer a few days before release day. Draft the tribute only when the user supplies the artist. Otherwise leave `[JAZZ ARTIST PASSAGE: supplied on release day]` in place of the opening paragraphs and the title's code name. Never guess, infer, or research a likely artist. When the artist is supplied, biographical facts come from the user or from a reputable reference you fetched during the run; keep the passage to two or three short paragraphs and end it with one sentence that connects the artist to the release.

---

## Requirements, defaults, and evidence

- **Required:** facts must match current authoritative evidence; prerelease posts must warn against production use; security updates must convey the approved update guidance and preserve supplied attribution. A template never overrides factual accuracy or the user's explicit instructions.
- **Approved boilerplate:** retain wording explicitly approved for this release, including Security Team descriptions and credits. Make only authorized substitutions. If approved wording conflicts with newer evidence, flag the conflict and use a placeholder for the disputed assertion until resolved.
- **Default wording and structure:** blockquotes in the references are reusable drafting defaults drawn from published examples, not proof of approval or permanent facts. Keep familiar wording where it fits. Adapt it for accuracy, the brief, or the applicable variant; avoid gratuitous restyling. Format-specific defaults may retain the familiar announcement phrases identified below.
- **Conditional:** include sections only when their stated conditions apply and supporting material exists. Feature grouping and length follow the release; there is no feature quota. Honor requested omissions such as a haiku.
- **Release-specific:** write feature descriptions and summaries from evidence using the shared guide. Security descriptions and credits remain approved attribution, not fresh promotional writing.
- **Drift check:** compare the latest relevant announcement with the reference. Record material differences and explain useful adaptations in editor notes. Neither a recent post nor an old template automatically overrides current evidence or the brief.

---

## Workflow

1. **Select the format** by purpose and contents; load the applicable references.
2. **Research and record evidence:** source and confirmation status for each count, date, link, name, and operational claim; target-build inclusion and qualifications for each feature. Record the actual previous milestone and first-preview announcement. Mark unresolved publication requirements without blocking independent drafting.
3. **Draft** using the applicable defaults, approved wording, and supported sections. Compare recent examples for continuity.
4. **Review separately** using guide Section 16, then the News checklist and this skill's checklist. Provide the reviewer the evidence, format decisions, conditional omissions, and approved wording. Apply the release-specific overrides throughout the review.
5. **Return the corrected draft for human review**, metadata, and concise non-public editor notes covering unresolved facts, placeholders, and material adaptations. Distinguish an early draft from one whose publication requirements have been verified.

---

## Writing rules specific to release posts

### Versions, milestones, and counts

- Use the actual version and milestone consistently: "WordPress X.Y Beta 2," "WordPress X.Y RC1," and "WordPress X.Y.Z." Only major GA posts have a jazz code name. Do not infer the next major by arithmetic.
- Apply guide Section 9 for dates and numbers. In prerelease copy, bold the final release date and describe it as scheduled or planned.
- Use exact confirmed counts, or a supported lower bound when the squad confirms that phrasing is appropriate. "More than 100" requires evidence of a total above 100. Rounding an unverified count does not verify it; omit it or use `[COUNT TO CONFIRM]`.
- Record what each count measures and its milestone window. Check totals against component counts when they measure the same set; do not equate commits, tickets, fixes, and contributors. Bold counts in the beta/RC count sentence as shown in the reference.

### Features and highlights

- Each feature gets what it is, what the reader can now do, and where it lives (Site Editor, post editor, dashboard, `theme.json`, an API). Lead with the user outcome in user-facing sections and with the API or mechanism in the developer section.
- Confirm that the feature is included in the target WordPress build using release-specific notes, a current squad confirmation, or target-branch inclusion with any required backport. Check later removals, reversions, and changes in scope. A merged Gutenberg pull request, roadmap item, or earlier beta announcement alone is insufficient. Use "adds" or "now supports" only for capabilities available in that build; keep unconfirmed plans in editor notes. State prerequisites and experimental or opt-in status when they affect what readers can do.
- Do not promise what a future milestone will contain. A beta post says what is in that beta; later changes are "expected" only when the squad has said so.
- Link each feature to its dev note, ticket, or pull request where the type reference asks for it. A "Learn more:" line lists references as "Trac #NNNNN" and "GitHub #NNNNN"; give the ticket type and number, not the ticket title. (The RC1 ticket list is the one place that pairs each number with its title.)

### Security fixes

- One list item per vulnerability, in the order and wording the Security Team supplied: the issue as described, then "reported by" and the credit exactly as given (person, organization, link). Keep the Security Team's severity words; add none.
- Never add exploit detail, affected-version analysis, or mitigation advice beyond what the Security Team supplied. The "update immediately" line and the backports paragraph carry the guidance.
- CVE and GHSA references appear only when the Security Team supplies the advisory links.

### People and credits

- Use the supplied WordPress.org profiles and name forms for the release squad and contributor roster; mark missing links for confirmation. Security reporter attribution is an exception: preserve supplied external links, organizations, and unlinked names exactly. Do not invent or substitute profiles. Use the roster's role labels.
- Major release credits use the `[wpcredits X.Y]` shortcode in place of a typed list. Minor release credits are a comma-separated, alphabetized list of linked names supplied by the release squad.
- Beta, RC, and maintenance posts normally credit reviewers by @username in an italic props line. Use supplied reviewers or a placeholder; honor an explicit omission and the combined-post variant.

### Haiku

- Include a haiku by default in standalone beta and RC posts; omit it when requested or when the selected combined variant excludes it. Major and minor releases do not use one. A drafting request authorizes writing the default haiku; no separate permission is needed.
- Three lines, roughly five, seven, and five syllables, about the milestone or testing. Keep it plain and universally acceptable: no puns on people's names, no in-jokes, nothing that needs cultural context. Credit a contributor-written haiku in the props line as the reference shows.

### Where release posts differ

These are the deliberate departures from the News Post Rules and the guide, so the review pass does not "correct" them:

- **Openings:** use the selected type's default opener. Major releases open with the artist tribute, then the "Welcome to WordPress X.Y!" summary that leads with the biggest changes. Betas, RCs, and minors normally open with availability, scope, or an explanation of the release, as their variant shows. This overrides the News rule to lead with the version and the biggest change.
- **Exclamation points** in default openers and the "Welcome to WordPress X.Y!" heading stay.
- **Headings:** default headings retain the reference's form, including Title Case where shown; adapt milestone labels to the actual release. New headings you write (feature H3s and H4s) are sentence case with no final punctuation, per the News rules.
- **Links** use standard Markdown in the editorial handoff. This replaces the News rules' bold-plus-URL convention. Bold is used for the one-line feature taglines, the counts, the dates, and the bold lines in the templates.
- **Lists and tables** are routine in this format: the how-to-test table, query link lists, security fix lists, the squad list, and feature bullets in beta posts.
- **Credits:** the squad section, the contributors section, and the props line are part of the format and are not a "credits section" in the sense the News rules discourage.
- **Haiku** in beta and RC posts.
- **Default wording** may retain familiar announcement phrases where the reference supplies them; this exception never exempts factual assertions from verification or overrides current approved wording.

---

## Output format

Return Markdown for an editorial handoff to the block editor. Button labels, asset placeholders, and shortcodes still need the corresponding blocks during CMS preparation:

- Title on the first line as `# Title`, then the body.
- Headings as `##`, `###`, and `####`, following the selected structure without skipped levels.
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

- Unresolved publication requirements, placeholders, provisional figures, links to confirm, and material adaptations or conflicts with the reference. Preserve supplied conditional omissions in the review handoff.

---

## Release checklist

Run this after the guide's Section 16 review pass and the News format checklist. Fix what fails. A checklist item never authorizes inventing detail; missing evidence calls for a placeholder and an editor note.

- [ ] Routing matches the announcement's purpose and contents, including first-preview, fast-follow, and combined variants. The title retains the actual milestone and approved naming.
- [ ] All required components and applicable conditional sections are present. User-requested omissions and justified structural adaptations survive review; no unsupported sections were added to satisfy the template.
- [ ] Applicable substitutions are correct or explicitly marked: versions, actual previous milestone, first-preview link, dates, downloads, commands, Playground build, query windows, and release documentation.
- [ ] Approved wording and security attribution are preserved. Reusable wording has been checked for current factual accuracy, including backport branches/status and translation milestones.
- [ ] Counts have confirmed values or supported lower bounds and compatible units/windows. Unverified counts remain placeholders or are omitted with an editor note.
- [ ] Each feature is confirmed in the target build; later removals and qualifications are reflected. Future plans are not presented as shipped capabilities.
- [ ] Security descriptions, severity, reporter credits, and advisory links match the Security Team's supplied material; no new vulnerability or mitigation claims were added.
- [ ] Squad/contributor identities match supplied rosters. Security credits retain supplied external links or unlinked names; missing roster profiles are flagged rather than invented.
- [ ] The jazz passage and code name appear only when supplied by the user; otherwise the placeholders remain.
- [ ] Links, dates, and heading levels follow the applicable defaults and shared mechanics. Unverified links are marked; syntactically plausible URLs are not claimed as verified.
- [ ] Haiku and props follow the selected variant and the user's instructions; review has not reintroduced an omitted haiku or invented reviewers.
- [ ] Metadata and editor notes are outside the publishable draft, and unresolved publication requirements are visible.
- [ ] The shared guide and News rules apply wherever this skill does not override them.
