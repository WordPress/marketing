# Release candidate posts (RC1 and later RCs)

Loaded by `wordpress-writer-news-release` for release candidate milestones only. RC1 asks theme and plugin authors, hosts, and translators to finish their work; confirm the actual string-freeze milestone from current cycle evidence. RC2 and later report what changed and repeat the calls to contribute. The structure is the one used from 6.9 RC1 through 7.1 RC1; the default wording is the wording published for 7.1 RC1, with the fuller "Get involved in testing" paragraphs, the "Reaching this phase" line, and the "Help translate WordPress" section from 7.0 RC3, and punctuation normalized to the brand guide.

**How to read this file.** Blockquotes provide default wording; remove the blockquote in the draft. Apply the [requirements, defaults, and evidence rules](../SKILL.md#requirements-defaults-and-evidence). Bold inside a blockquote is bold in the post. Facts and substitutions still require current evidence; approved security wording and attribution must be preserved. Placeholders: `X.Y` is the version, `X-Y` its slug form, `N` the RC number, `M` the previous milestone, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

## Facts to collect

- Version and RC number; the scheduled final release date; the release schedule post on Make/Core (and the updated schedule post, if the date moved)
- RC zip URL (`https://wordpress.org/wordpress-X.Y-RCN.zip`), WP-CLI command (`wp core update --version=X.Y-RCN`), and a WordPress Playground URL for this RC
- The count of updates and fixes since the previous milestone, split into Editor and Core; the Trac query and GitHub commits links for the date window
- The first-preview announcement URL and actual milestone label (usually Beta 1), the dev notes tag URL (`https://make.wordpress.org/core/tag/dev-notes+X-Y/`), and the Field Guide URL (published around RC1)
- RC1: features added since the first public preview and confirmed in this build, each with its changeset, ticket, or pull request; a short list of notable tickets and pull requests the squad wants called out
- Later RCs: anything the squad wants noted (a feature removed from the release, a changed date, a host testing effort), with its Make/Core post
- The "Help test WordPress X.Y" post on Make/Test; the hosts to thank, if any
- The confirmed hard string-freeze milestone, translation availability, and supporting cycle announcement
- Any supplied haiku or request to omit it; the @usernames of the people who reviewed the post

## Structure

**Required:** availability, production-use warning, testing methods, supported changes, and bug-reporting instructions. **Defaults:** contribution, compatibility, hosting, and translation invitations. **Conditional:** counts and their split, new-feature/ticket lists, freeze announcements, host thanks, and event assets. A haiku is the default unless omitted by the user.

### Title (default wording)

`WordPress X.Y Release Candidate N`, unless the brief supplies approved alternative naming.

### Opener (default wording)

The production-use warning is required; retain the wording below unless newer approved wording preserves its meaning.

The ordinal is spelled out: first, second, third, fourth.

> The [ORDINAL] Release Candidate ("RCN") for WordPress X.Y is ready for download and testing!
>
> **This version of the WordPress software is still under development**. Please do not install, run, or test this version of WordPress on production or mission-critical websites. Instead, it's recommended to evaluate RCN on a test server and site.

RC2 and later may add, before the table:

> Reaching this phase of the release cycle is an important milestone. As always, testing remains crucial to ensure that everything in WordPress X.Y is the best it can be.

### How to test (default wording; no heading)

> WordPress X.Y RCN can be tested using any of the following methods:

| | |
|---|---|
| **Plugin** | Install and activate the [WordPress Beta Tester](https://wordpress.org/plugins/wordpress-beta-tester/) plugin on a WordPress install. (Select the "Bleeding edge" channel and "Beta/RC Only" stream.) |
| **Direct Download** | Download the [RCN version (zip)](https://wordpress.org/wordpress-X.Y-RCN.zip) and install it on a WordPress website. |
| **Command Line** | Use this [WP-CLI](https://make.wordpress.org/cli/) command: `wp core update --version=X.Y-RCN` |
| **WordPress Playground** | Use the [WordPress Playground instance]([Playground URL]) to test the software directly in your browser. No setup required. Just click and go! |

> The scheduled final release date for WordPress X.Y is **Month D, YYYY**. The full [release schedule can be found here]([schedule post URL]). Your help testing Beta and RC versions is vital to making this release as stable and powerful as possible. Thank you to everyone who contributes by testing!
>
> Please continue checking the [Make WordPress Core blog](https://make.wordpress.org/core/) for [X.Y-related posts](https://make.wordpress.org/core/tag/X-Y) in the coming weeks for more information.

### `## What's in WordPress X.Y RCN?` (default wording with substitutions, then release-specific)

> WordPress X.Y RCN contains **[TOTAL_COUNT] updates** and fixes since [PREVIOUS_MILESTONE], including **[EDITOR_COUNT] in the Editor** and **[CORE_COUNT] in Core**.
>
> For an overview of what's new in WordPress X.Y, read the [FIRST_PREVIEW_LABEL announcement]([FIRST_PREVIEW_URL]) and the [WordPress X.Y Dev Notes](https://make.wordpress.org/core/tag/dev-notes+X-Y/). For a comprehensive summary, see the [WordPress X.Y Field Guide]([Field Guide URL]).
>
> You can also explore the technical details of all issues addressed since [PREVIOUS_MILESTONE] using the links below:
>
> - [GitHub commits for X.Y](https://github.com/WordPress/gutenberg/commits/wp/X.Y?since=YYYY-MM-DD&until=YYYY-MM-DD) since Month D, YYYY
> - [Closed Trac tickets for X.Y](https://core.trac.wordpress.org/query?status=closed&changetime=MM%2FDD%2FYYYY..MM%2FDD%2FYYYY&milestone=X.Y&col=id&col=milestone&col=owner&col=type&col=priority&order=id) since Month D, YYYY

Use the actual previous shipped milestone, including silent builds, for the comparison and query window. Counts accept exact confirmed values or supported lower bounds. If counts are unavailable, omit the count sentence and retain the verified change links; if only a total is known, omit the split.

RC1 may then add either of these release-specific lists when the squad supplies relevant items:

`### New Features since Beta 1`

- [Feature name](changeset, ticket, or pull request URL): one sentence on what it adds.

Each item links the feature name to its source and describes it in one plain sentence ("New APIs for registering icons and icon collections in Core, ready for plugins to extend."). Include only features confirmed in the target build, after checking any required backport, later removal, or reversion. If the first preview was not Beta 1, update the heading to name it. Do not add items to meet a quota.

Then, with the default lead-in:

> Want to look deeper into the details and technical notes for this release? These tickets and pull requests are just some of the latest updates:

- [#GB-NNNNN](https://github.com/WordPress/gutenberg/pull/NNNNN): ticket title as the squad gives it
- [#NNNNN](https://core.trac.wordpress.org/ticket/NNNNN): ticket title as the squad gives it

Gutenberg pull requests are labeled `#GB-NNNNN`; Trac tickets are `#NNNNN`. Use the relevant items chosen by the squad; no fixed count is required.

RC2 and later replace those lists with whatever the squad wants noted, in one short paragraph each, with a bold lead-in label where the note changes what readers should expect ("**Note**: [Real Time Collaboration will not be included](URL) in the 7.0 release and will be re-evaluated during the 7.1 release cycle."). When nothing needs noting, the default paragraphs above are the whole section.

### `## How you can contribute` (default wording)

> WordPress is open source software made possible by a passionate community of people collaborating on and contributing to its development. The resources below outline various ways you can help the world's most popular open source web platform, regardless of your technical expertise.

### `### Get involved in testing` (default wording)

> Testing for issues is crucial to the development of any software. It's also a meaningful way for anyone to contribute.
>
> Your help testing the WordPress X.Y RCN version is key to ensuring that the final release is the best it can be. While testing the upgrade process is essential, trying out new features is equally important. This [detailed guide]([Make/Test post URL]) will walk you through testing features in WordPress X.Y.
>
> If you encounter a potential bug or issue, please report it to the [Alpha/Beta area](https://wordpress.org/support/forum/alphabeta/) of the support forums or directly to [WordPress Trac](https://core.trac.wordpress.org/newticket) if you are comfortable writing a reproducible bug report. You can also check your issue against a list of [known bugs](https://core.trac.wordpress.org/tickets/major).
>
> Curious about testing releases in general? Follow along with the [testing initiatives in Make Core](https://make.wordpress.org/test/) and join the [#core-test channel](https://wordpress.slack.com/messages/core-test/) on [Making WordPress Slack](https://wordpress.slack.com/).

An optional default line for newcomers may follow the detailed-guide paragraph: "For those new to testing, follow [this general testing guide](https://make.wordpress.org/test/handbook/get-setup-for-testing/) for more details on getting set up."

### `### Update your theme or plugin` (default wording)

> For plugin and theme authors, your products play an integral role in extending the functionality and value of WordPress for all users.
>
> Thanks for continuing to test your themes and plugins with the WordPress X.Y beta releases. With RC1, you'll want to conclude your testing and update the *"Tested up to"* version in your [plugin's readme file](https://developer.wordpress.org/plugins/wordpress-org/how-your-readme-txt-works/) to X.Y.
>
> If you find compatibility issues, please post detailed information to the [support forum](https://wordpress.org/support/forum/alphabeta/).

In RC2 and later, the second paragraph begins "If you haven't yet, make sure to conclude your testing and update..." instead of "With RC1, you'll want to conclude...".

### `### Test on your hosting platforms` (default wording)

> Web hosts provide vital infrastructure for supporting WordPress and its users. Testing on hosting systems helps inform the development process while ensuring that WordPress and hosting platforms are fully compatible, free of errors, optimized for the best possible user experience, and that updates roll out to customer sites without issue.
>
> Want to test WordPress on your hosting system? [Get started with configuring distributed hosting tests here](https://make.wordpress.org/hosting/test-results-getting-started/). Thank you to all [web hosts who help test WordPress](https://make.wordpress.org/hosting/test-results/)!

When the squad wants specific hosts thanked for a particular effort, add one sentence naming them before the "Want to test" paragraph, as 7.0 RC3 did.

### `## Help translate WordPress` (default wording)

> Do you speak a language other than English? ¿Español? Français? Русский? 日本語? हिन्दी? বাংলা? मराठी? ಕನ್ನಡ? You can [help translate WordPress](https://translate.wordpress.org/projects/wp/dev/).

Include this invitation by default. Add a freeze or availability announcement only from current cycle evidence, for example:

> [CONFIRMED_FREEZE_MILESTONE] marks the [hard string freeze](https://make.wordpress.org/polyglots/handbook/glossary/#hard-freeze) point of the [X.Y release cycle]([release candidate phase post URL]).

Use past tense if the freeze occurred at an earlier milestone. Do not say every RC starts a new freeze. If strings are not yet available, state the confirmed availability date or milestone; if unknown, omit that claim and flag it in editor notes.

### `## An RCN haiku` (release-specific, default; omit when requested)

Three lines, italic in recent posts. Then the props line, italic, as the last line of the post:

> *Props to @username, @username, and @username for proofreading and review.*

Leave `[@usernames]` as a placeholder until the user supplies them. An event banner image with alt text may follow the props line when the release launches at an event and design supplies one.

## Notes on this type

- Categories: Development and Releases. Tags: `X.Y`, `development`, `release`; recent posts also used `release candidates`.
- Heading levels for the contribute subsections have varied between `##` and `###` from post to post. Use `##` for "How you can contribute," "Help translate WordPress," and the haiku, and `###` for the three subsections under "How you can contribute," as 7.0 RC3 did.
- Posts from 6.3 RC3 through 6.8 carried a "Search for vulnerabilities" subsection on the doubled bounty (a few late RCs in that span skipped it). It was dropped from 6.9 onward; do not reintroduce it unless the Security Team asks.
- 6.0 RC2 and RC3 appended "(RC2) Now Available for Testing" to the title and 6.1 appended "(RC1) Now Available." Retired. The "What's in WordPress X.Y RC1?" heading and the four contribute subsections date back to 6.0 and 6.4 respectively and are current.
