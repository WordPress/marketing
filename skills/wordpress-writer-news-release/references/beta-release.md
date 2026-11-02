# Beta release posts (Beta 1 and later betas)

Loaded by `wordpress-writer-news-release` for beta milestones only. The first public preview introduces the release and its features; subsequent betas report changes since the previous shipped milestone. The first preview may have a later number, as [6.3 Beta 2](https://wordpress.org/news/2023/06/wordpress-6-3-beta-2/) did. Use the actual number throughout, and never invent a Beta 1 announcement. The section order is the one both 7.2 beta posts used (the release content comes before the general testing paragraphs); the default wording is the wording published for 7.2 Beta 1 and Beta 2, with the count sentence, query link labels, and "Find out what's new" paragraph from 7.1 Beta 4, and punctuation normalized to the brand guide.

**How to read this file.** Blockquotes provide default wording; remove the blockquote in the draft. Apply the [requirements, defaults, and evidence rules](../SKILL.md#requirements-defaults-and-evidence). Bold inside a blockquote is bold in the post. Facts and substitutions still require current evidence; approved security wording and attribution must be preserved. Placeholders: `X.Y` is the version, `N` the beta number, `M` the previous beta number, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

## Facts to collect

- Version, beta number, whether this is the first public preview, and the actual previous shipped milestone (if any); the scheduled final release date; the release schedule post on Make/Core
- Beta zip URL (`https://wordpress.org/wordpress-X.Y-betaN.zip`), WP-CLI command (`wp core update --version=X.Y-betaN`), and a WordPress Playground URL for this beta (`https://playground.wordpress.net/?wp=beta&php=8.3&networking=no&language=&multisite=no`, or the one the squad supplies)
- The "Help test WordPress X.Y" post on Make/Test
- First public preview: the feature list from the squad, with each feature's dev note, Gutenberg release post, ticket, or pull request; the Gutenberg versions merged since the last major, with their "What's new in Gutenberg" links; the event the release launches at, if any
- Subsequent betas: the count of updates and fixes since the previous beta, split into Editor and Core; the Trac query and GitHub commits links for the date window; any highlights the squad wants called out, with their tickets; the first-preview announcement URL and milestone label
- Any supplied haiku or request to omit it; the @usernames of the people who reviewed the post

## Structure

**Required:** availability, production-use warning, testing methods, current release scope or changes, and bug-reporting instructions. **Default order:** opener, how to test, release content, why testing matters, haiku and props. **Conditional:** counts, feature images, Gutenberg version list, and event details. The haiku may be omitted as described in the entry point. Use the first-preview overview for the first public beta regardless of its number; use the subsequent-beta section only when there is a previous build to compare.

### Title (default wording)

`WordPress X.Y Beta N`, unless the brief supplies approved alternative naming. (7.2 Beta 1 appended "is Ready for Download and Testing" and 6.1 appended "Now Available." The bare title is this skill's default.)

### Opener (default wording)

The production-use warning is required; retain the wording below unless the user supplies newer approved wording that preserves its meaning.

> WordPress X.Y Beta N is ready for download and testing!
>
> **This beta release is intended for testing and development** only. Please do not install, run, or test this version of WordPress on production or mission-critical websites. Instead, use a test environment or local site to explore the new features.

### `## How to Test WordPress X.Y Beta N` (default wording)

> You can test WordPress X.Y Beta N in any of the following ways:

| | |
|---|---|
| **WordPress Beta Tester Plugin** | Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin on a WordPress install. Select the "Bleeding edge" channel and "Beta/RC Only" stream. |
| **Direct Download** | Download the [Beta N version (zip)](https://wordpress.org/wordpress-X.Y-betaN.zip) and install it on a WordPress website. |
| **Command Line (WP-CLI)** | Use this [WP-CLI](https://make.wordpress.org/cli/) command: `wp core update --version=X.Y-betaN` |
| **WordPress Playground** | Use a [X.Y Beta N WordPress Playground instance]([Playground URL]) to test the software directly in your browser. No setup required. Just click and go! |

> The scheduled final release date for WordPress X.Y is **Month D, YYYY**. The full [release schedule can be found here]([schedule post URL]). Your help testing Beta and RC versions is vital to making this release as stable and powerful as possible. Thank you to everyone who contributes by testing!

Subsequent betas may add one more default paragraph here, pointing back to the first public preview (7.1 Betas 3 and 4 did; 7.2 Beta 2 did not):

> **Find out what's new in WordPress X.Y**: Read the [FIRST_PREVIEW_LABEL announcement]([FIRST_PREVIEW_URL]) for details and highlights.

### First public preview: `## What's new in WordPress X.Y?` (release-specific)

An overview paragraph that names the release's themes and its headline changes in plain sentences, each saying what the reader can now do. Close the paragraph with the developer and site-owner angle in one sentence.

Then one `###` per feature area, in priority order. Two shapes work, and recent posts used both:

- **Prose shape (7.1 Beta 1):** a sentence-case `###` heading written as a benefit ("Style it your way, on any screen"), one framing sentence, then either short paragraphs or a bulleted list where each item starts with a bold label and a colon ("**Responsive styling**: Define how a block looks at different screen sizes...").
- **Reference shape (7.2 Beta 1):** a `###` heading per feature, one or two paragraphs, an image where supplied, and a closing line **Learn more:** followed by the ticket and pull request links ("[Trac #65869](URL), [GitHub #80388](URL)").

Choose one shape and keep it for the whole post. Typical areas: collaboration or editing, styling and design tools, media, the admin experience, new blocks and block options, internationalization, and a developer section ("Built for developers" or "For developers") that names each API and what it now allows. 7.2 Beta 1 split the areas under two `##` headings ("Editing Experience" and "For Developers") instead of one; either is acceptable, with sentence-case headings.

End the section with the default closing sentence. Append " at [Event name](URL)" when the release launches at an event, and place the event banner image with alt text after it when design supplies one:

> With so much in progress for WordPress X.Y Beta N, this is still only the beginning; expect continued refinement with each Beta and RC release ahead of the final release on **Month D, YYYY**.

### Subsequent betas: `## What's in WordPress X.Y Beta N?` (default wording with substitutions, then release-specific highlights)

> WordPress X.Y Beta N contains **[TOTAL_COUNT]** updates and fixes since [PREVIOUS_MILESTONE], including **[EDITOR_COUNT]** in the Editor and **[CORE_COUNT]** in Core.
>
> Each beta cycle focuses on bug fixes, and more are on the way with your help through testing. You can browse the technical details for all issues addressed since [PREVIOUS_MILESTONE] using these links:
>
> - [GitHub commits for X.Y](https://github.com/WordPress/gutenberg/commits/wp/X.Y?since=YYYY-MM-DD&until=YYYY-MM-DD) since Month D, YYYY
> - [Closed Trac tickets for X.Y](https://core.trac.wordpress.org/query?status=closed&changetime=MM%2FDD%2FYYYY..MM%2FDD%2FYYYY&milestone=X.Y&col=id&col=milestone&col=owner&col=type&col=priority&order=id) since Month D, YYYY

Use the actual previous shipped milestone and its release date, including silent or bundled releases. Confirm the query window and count definitions. Count fields take exact confirmed values or supported lower-bound phrases; omit an unavailable split instead of inventing component counts. When the squad has not supplied counts, drop the count sentence and open with the lead-in 7.2 Beta 2 used: "For technical details on the issues addressed since [PREVIOUS_MILESTONE], see the following links:".

Then, release-specific, one to three short paragraphs or a short `###` subsection on what the squad wants called out: a feature that landed after Beta 1 (7.0 Beta 2 introduced the Connectors screen this way, under a bold lead-in line), a notable fix, or continued work on an API, each with its ticket or pull request. A "**Learn more:**" line listing Trac and GitHub references may close the subsection. When nothing is worth calling out, one sentence saying the beta brings fixes across the editor and Core is enough.

### `## How important is your testing?` (default wording)

> Testing for issues is a critical part of developing any software, and it's a meaningful way for anyone to contribute, whether or not you have experience. [Details on what to test in WordPress X.Y are available here]([Make/Test post URL]).
>
> If you encounter an issue, please share it in the [Alpha/Beta area](https://wordpress.org/support/forum/alphabeta/) of the support forums. If you are comfortable submitting a reproducible bug report, you can do so [via WordPress Trac](https://core.trac.wordpress.org/newticket). You can also check your issue against this list of [known bugs](https://core.trac.wordpress.org/tickets/major).
>
> Curious about testing releases in general and how to get started? Follow along with the [testing initiatives in Make Core](https://make.wordpress.org/test/) and join the [#core-test channel](https://wordpress.slack.com/messages/core-test/) on [Making WordPress Slack](https://wordpress.slack.com/).

The first-preview overview may add this paragraph when the included Gutenberg versions are confirmed, linking their "What's new in Gutenberg" posts. Plugin release notes describe broader plugin scope; they do not establish that every plugin feature ships in WordPress:

> This WordPress X.Y beta includes features previously available in the Gutenberg plugin. Learn more about Gutenberg updates since WordPress [previous major] in the [What's New in Gutenberg](https://make.wordpress.org/core/tag/gutenberg-new/) posts for versions [A](URL), [B](URL), [C](URL), and [D](URL).

### `## A Beta N haiku` (release-specific, default; omit when requested)

Beta 1 uses the heading `## Just for you: a Beta 1 haiku` (published with a trailing colon in 7.0 through 7.2; drop it); later betas use `## A Beta N haiku`. Three lines, italic in recent posts, about the milestone or testing.

Then the props line, italic, as the last line of the post:

> *Props to @username, @username, and @username for proofreading and review.*

When someone else prepared the post or wrote the haiku, say so in the same line ("Props to @a for preparing this post and @b, @c for proofreading and review."). Leave `[@usernames]` as a placeholder until the user supplies them.

## Notes on this type

- Categories: Development and Releases. Tags: `X.Y`, `development`, `release`.
- Section order has moved. 7.0 Beta 1 and 7.1 Betas 1, 3, and 4 placed "How important is your testing?" before the release content; both 7.2 posts placed it after. Follow the 7.2 order above. 7.0 Betas 2, 3, and 5 used an older shape ("How to test this release," "Beta N updates and highlights," and a "now ready for testing" opener) that is not this skill's default.
- 7.2 Beta 1 used Title Case feature headings and appended "is Ready for Download and Testing" to the title. Treat both as one-offs; sentence-case feature headings follow the News rules.
- Posts from 6.3 Beta 2 through 6.8 carried a "Vulnerability bounty doubles" section. It was dropped from 6.9 onward; do not reintroduce it unless the Security Team asks.
- When a beta ships with a minor release's security fixes (7.0 Beta 4 did, in a combined post), see the security reference for the combined pattern.
- Beta 1 posts from 6.0 through 6.5 opened with a testing section under earlier headings ("Keep WordPress bug-free," "How you can help: Testing," "How to help test this release"). Historical wording, not the current default.
