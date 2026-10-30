# Beta release posts (Beta 1 and later betas)

Loaded by `wordpress-writer-news-release` for beta milestones only. Beta 1 introduces the release and its features; Beta 2 and later are short and report what changed since the previous beta. The section order is the one both 7.2 beta posts used (the release content comes before the general testing paragraphs); the standing copy is the wording published for 7.2 Beta 1 and Beta 2, with the count sentence, query link labels, and "Find out what's new" paragraph from 7.1 Beta 4, and punctuation normalized to the brand guide.

**How to read this file.** Standing copy appears in blockquotes: reproduce it without the blockquote, with only the marked substitutions. Bold inside a blockquote is bold in the post. Placeholders: `X.Y` is the version, `N` the beta number, `M` the previous beta number, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

## Facts to collect

- Version and beta number; the scheduled final release date; the release schedule post on Make/Core
- Beta zip URL (`https://wordpress.org/wordpress-X.Y-betaN.zip`), WP-CLI command (`wp core update --version=X.Y-betaN`), and a WordPress Playground URL for this beta (`https://playground.wordpress.net/?wp=beta&php=8.3&networking=no&language=&multisite=no`, or the one the squad supplies)
- The "Help test WordPress X.Y" post on Make/Test
- Beta 1: the feature list from the squad, with each feature's dev note, Gutenberg release post, ticket, or pull request; the Gutenberg versions merged since the last major, with their "What's new in Gutenberg" links; the event the release launches at, if any
- Beta 2 and later: the count of updates and fixes since the previous beta, split into Editor and Core; the Trac query and GitHub commits links for the date window; any highlights the squad wants called out, with their tickets; the Beta 1 post URL
- The haiku, or permission to write one; the @usernames of the people who reviewed the post

## Structure

The order is the same for every beta: opener, how to test, what is in the release or the beta, why testing matters, haiku.

### Title (standing)

`WordPress X.Y Beta N`. Nothing else. (7.2 Beta 1 appended "is Ready for Download and Testing" and 6.1 appended "Now Available." Neither is the pattern; keep the bare title.)

### Opener (standing)

> WordPress X.Y Beta N is ready for download and testing!
>
> **This beta release is intended for testing and development** only. Please do not install, run, or test this version of WordPress on production or mission-critical websites. Instead, use a test environment or local site to explore the new features.

### `## How to Test WordPress X.Y Beta N` (standing)

> You can test WordPress X.Y Beta N in any of the following ways:

| | |
|---|---|
| **WordPress Beta Tester Plugin** | Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin on a WordPress install. Select the "Bleeding edge" channel and "Beta/RC Only" stream. |
| **Direct Download** | Download the [Beta N version (zip)](https://wordpress.org/wordpress-X.Y-betaN.zip) and install it on a WordPress website. |
| **Command Line (WP-CLI)** | Use this [WP-CLI](https://make.wordpress.org/cli/) command: `wp core update --version=X.Y-betaN` |
| **WordPress Playground** | Use a [X.Y Beta N WordPress Playground instance]([Playground URL]) to test the software directly in your browser. No setup required. Just click and go! |

> The scheduled final release date for WordPress X.Y is **Month D, YYYY**. The full [release schedule can be found here]([schedule post URL]). Your help testing Beta and RC versions is vital to making this release as stable and powerful as possible. Thank you to everyone who contributes by testing!

Beta 2 and later may add one more standing paragraph here, pointing back to Beta 1 (7.1 Betas 3 and 4 did; 7.2 Beta 2 did not):

> **Find out what's new in WordPress X.Y**: Read the [Beta 1 announcement]([Beta 1 URL]) for details and highlights.

### Beta 1: `## What's new in WordPress X.Y?` (release-specific)

An overview paragraph that names the release's themes and its three to five headline changes in plain sentences, each saying what the reader can now do. Close the paragraph with the developer and site-owner angle in one sentence.

Then one `###` per feature area, in priority order. Two shapes work, and recent posts used both:

- **Prose shape (7.1 Beta 1):** a sentence-case `###` heading written as a benefit ("Style it your way, on any screen"), one framing sentence, then either short paragraphs or a bulleted list where each item starts with a bold label and a colon ("**Responsive styling**: Define how a block looks at different screen sizes...").
- **Reference shape (7.2 Beta 1):** a `###` heading per feature, one or two paragraphs, an image where supplied, and a closing line **Learn more:** followed by the ticket and pull request links ("[Trac #65869](URL), [GitHub #80388](URL)").

Choose one shape and keep it for the whole post. Typical areas: collaboration or editing, styling and design tools, media, the admin experience, new blocks and block options, internationalization, and a developer section ("Built for developers" or "For developers") that names each API and what it now allows. 7.2 Beta 1 split the areas under two `##` headings ("Editing Experience" and "For Developers") instead of one; either is acceptable, with sentence-case headings.

End the section with the standing closing sentence. Append " at [Event name](URL)" when the release launches at an event, and place the event banner image with alt text after it when design supplies one:

> With so much in progress for WordPress X.Y Beta 1, this is still only the beginning; expect continued refinement with each Beta and RC release ahead of the final release on **Month D, YYYY**.

### Beta 2 and later: `## What's in WordPress X.Y Beta N?` (standing with substitutions, then release-specific highlights)

> WordPress X.Y Beta N contains more than **[N]** updates and fixes since the Beta M release, including **[N]** in the Editor and **[N]** in Core.
>
> Each beta cycle focuses on bug fixes, and more are on the way with your help through testing. You can browse the technical details for all issues addressed since Beta M using these links:
>
> - [GitHub commits for X.Y](https://github.com/WordPress/gutenberg/commits/wp/X.Y?since=YYYY-MM-DD&until=YYYY-MM-DD) since Month D, YYYY
> - [Closed Trac tickets for X.Y](https://core.trac.wordpress.org/query?status=closed&changetime=MM%2FDD%2FYYYY..MM%2FDD%2FYYYY&milestone=X.Y&col=id&col=milestone&col=owner&col=type&col=priority&order=id) since Month D, YYYY

The date window runs from the previous beta's release date to this beta's release date; the "since" date is the previous beta's date. When the squad has not supplied counts, drop the count sentence and open with the lead-in 7.2 Beta 2 used: "For technical details on the issues addressed since Beta M, see the following links:".

Then, release-specific, one to three short paragraphs or a short `###` subsection on what the squad wants called out: a feature that landed after Beta 1 (7.0 Beta 2 introduced the Connectors screen this way, under a bold lead-in line), a notable fix, or continued work on an API, each with its ticket or pull request. A "**Learn more:**" line listing Trac and GitHub references may close the subsection. When nothing is worth calling out, one sentence saying the beta brings fixes across the editor and Core is enough.

### `## How important is your testing?` (standing)

> Testing for issues is a critical part of developing any software, and it's a meaningful way for anyone to contribute, whether or not you have experience. [Details on what to test in WordPress X.Y are available here]([Make/Test post URL]).
>
> If you encounter an issue, please share it in the [Alpha/Beta area](https://wordpress.org/support/forum/alphabeta/) of the support forums. If you are comfortable submitting a reproducible bug report, you can do so [via WordPress Trac](https://core.trac.wordpress.org/newticket). You can also check your issue against this list of [known bugs](https://core.trac.wordpress.org/tickets/major).
>
> Curious about testing releases in general and how to get started? Follow along with the [testing initiatives in Make Core](https://make.wordpress.org/test/) and join the [#core-test channel](https://wordpress.slack.com/messages/core-test/) on [Making WordPress Slack](https://wordpress.slack.com/).

Beta 1 adds a fourth standing paragraph, listing every Gutenberg version merged since the previous major, each linked to its "What's new in Gutenberg" post where one exists:

> WordPress X.Y will include new features that were previously only available in the Gutenberg plugin. Learn more about Gutenberg updates since WordPress [previous major] in the [What's New in Gutenberg](https://make.wordpress.org/core/tag/gutenberg-new/) posts for versions [A](URL), [B](URL), [C](URL), and [D](URL).

### `## A Beta N haiku` (release-specific)

Beta 1 uses the heading `## Just for you: a Beta 1 haiku` (published with a trailing colon in 7.0 through 7.2; drop it); later betas use `## A Beta N haiku`. Three lines, italic in recent posts, about the milestone or testing.

Then the props line, italic, as the last line of the post:

> *Props to @username, @username, and @username for proofreading and review.*

When someone else prepared the post or wrote the haiku, say so in the same line ("Props to @a for preparing this post and @b, @c for proofreading and review."). Leave `[@usernames]` as a placeholder until the user supplies them.

## Notes on this type

- Categories: Development and Releases. Tags: `X.Y`, `development`, `release`.
- Section order has moved. 7.0 Beta 1 and 7.1 Betas 1, 3, and 4 placed "How important is your testing?" before the release content; both 7.2 posts placed it after. Follow the 7.2 order above. 7.0 Betas 2, 3, and 5 used an older shape ("How to test this release," "Beta N updates and highlights," and a "now ready for testing" opener) that is retired.
- 7.2 Beta 1 used Title Case feature headings and appended "is Ready for Download and Testing" to the title. Treat both as one-offs; sentence-case feature headings follow the News rules.
- Posts from 6.3 Beta 2 through 6.8 carried a "Vulnerability bounty doubles" section. It was dropped from 6.9 onward; do not reintroduce it unless the Security Team asks.
- When a beta ships with a minor release's security fixes (7.0 Beta 4 did, in a combined post), see the security reference for the combined pattern.
- Beta 1 posts from 6.0 through 6.5 opened with a testing section under earlier headings ("Keep WordPress bug-free," "How you can help: Testing," "How to help test this release"). Retired.
