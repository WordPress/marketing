# Maintenance release posts (X.Y.Z)

Loaded by `wordpress-writer-news-release` for minor releases that contain bug fixes: a **maintenance release** (bug fixes only) and a **maintenance and security release** (bug fixes plus security fixes). A minor release with security fixes only uses the security reference instead. The structure is the one used from 6.8.1 through 7.1.3; the standing copy is the wording published for 7.0.1 (maintenance) and 7.1.3 (maintenance and security), with punctuation normalized to the brand guide.

**How to read this file.** Standing copy appears in blockquotes: reproduce it without the blockquote, with only the marked substitutions. Bold inside a blockquote is bold in the post. Placeholders: `X.Y.Z` is the version, `X.Y` the major it belongs to, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

## Facts to collect

- Version and release date; the zip URL (`https://wordpress.org/wordpress-X.Y.Z.zip`); the HelpHub version page (`https://wordpress.org/documentation/wordpress-version/version-X-Y-Z/`; maintenance posts through 7.0.1 linked the older `/support/wordpress-version/` path, which redirects there)
- The count of Core bugs fixed, with the Trac milestone query (`https://core.trac.wordpress.org/query?resolution=fixed&milestone=X.Y.Z&group=component&col=id&col=summary&col=milestone&col=owner&col=type&col=status&col=priority&order=priority`), and the count of Block Editor fixes with the changeset or backport pull request
- Two or three areas the fixes touch, as the release leads describe them ("the block editor, multisite, and REST API")
- The minor release's RC post on Make/Core
- The next major version and its scheduled date (and launch event, if any), or the Make/Core version page (`https://make.wordpress.org/core/X-Y/`)
- The release leads with profile URLs, and the alphabetized contributor list with profile URLs, from the release squad
- For a maintenance and security release: the vulnerability list with reporter credits, exactly as the Security Team supplied it, and backport status
- Any special notice the squad wants included (6.8.2 announced the end of security updates for 4.1 through 4.6 in its own section)
- The @usernames of the people who proofread the post

## Structure: maintenance release

### Title (standing)

`WordPress X.Y.Z Maintenance Release`.

### Opener (standing with substitutions)

> **WordPress X.Y.Z is now available!**
>
> This minor release includes fixes for [N] bugs [throughout Core]([Trac milestone query]) and the [Block Editor]([changeset or pull request URL]), addressing issues affecting multiple areas of WordPress including [area], [area], and [area]. For a full list of bug fixes, please refer to the [release candidate announcement]([Make/Core RC post URL]).
>
> WordPress X.Y.Z is a short-cycle maintenance release. The next major version of WordPress will be [X.Y+1]; it is scheduled for release on Month D, YYYY at [Event name](URL).
>
> If you have sites that support automatic background updates, the update process will begin automatically.
>
> You can [download WordPress X.Y.Z from WordPress.org](https://wordpress.org/wordpress-X.Y.Z.zip), or visit your WordPress Dashboard, click "Updates", and then click "Update Now". For more information on this release, please [visit the HelpHub site](https://wordpress.org/documentation/wordpress-version/version-X-Y-Z/).

When the next major has a date but no launch event, end the sentence at the date. When the count is split by source, the first sentence may read "includes fixes for [N Core tickets]([query]) and [N Block Editor issues]([pull request])" as 6.8.2 did.

### Special notice (release-specific, optional)

A `##` section with a plain heading naming the notice, one or two sentences, and a link to the full announcement. Only when the squad asks for it.

### `## Thank you to these WordPress contributors` (standing with substitutions)

> This release was led by [Name](https://profiles.wordpress.org/slug/) and [Name](https://profiles.wordpress.org/slug/).
>
> WordPress X.Y.Z would not have been possible without the contributions of the following people. Their asynchronous coordination to deliver maintenance fixes into a stable release is a testament to the power and capability of the WordPress community.

Then the contributor list as one paragraph: linked names, alphabetized, separated by commas, as the squad supplies it.

### `## How to contribute` (standing)

> To get involved in WordPress core development, head over to Trac, [pick a ticket](https://core.trac.wordpress.org/report/6), and join the conversation in the [#core](https://wordpress.slack.com/archives/C02RQBWTW) channel. Need help? Check out the [Core Contributor Handbook](https://make.wordpress.org/core/handbook/).

Then the props line, italic, as the last line:

> *Props to @username and @username for proofreading.*

## Structure: maintenance and security release

### Title (standing)

`WordPress X.Y.Z Maintenance and Security Release`.

### Opener (standing with substitutions)

> This security and maintenance release features [N] security fixes and [[N] bug fixes]([Trac milestone query]).
>
> **Because this is a security release, it is recommended that you update your sites immediately.**
>
> You can [download WordPress X.Y.Z from WordPress.org](https://wordpress.org/wordpress-X.Y.Z.zip), or visit your WordPress Dashboard, click "Updates", and then click "Update Now". If you have sites that support automatic background updates, the update process will begin automatically.

Two optional standing paragraphs follow when the squad wants them (7.1.1 had both; 7.1.3 had neither):

> WordPress X.Y.Z is a short-cycle release. The next major release will be [version X.Y+1](https://make.wordpress.org/core/X-Y/) and is currently planned for [Month].
>
> For more information, please visit the [WordPress X.Y.Z HelpHub site](https://wordpress.org/documentation/wordpress-version/version-X-Y-Z/).

When the bug fixes are split by source, the first sentence reads "features [N bug fixes on Core]([query]), [N bug fixes for the Block Editor]([pull request]), and [N] security fixes," as 7.1.1 did.

### `## Security updates included in this release` (standing lead-in, release-specific list)

> The security team would like to thank the following people and organizations for responsibly reporting vulnerabilities, and allowing them to be fixed in this release:

- [Issue as the Security Team describes it], reported by [Name](URL) ([organization]).

One item per vulnerability, in the Security Team's order and wording, with the credit exactly as supplied. Where the reporter is a Security Team member, the credit reads "reported by Name of the WordPress Security Team." Add a sentence after the list only when the Security Team supplies one (6.9.2 noted a coordinated fix with an external library's maintainer).

### `## Thank you to these WordPress contributors` (standing with substitutions)

> This release was led by [Name](https://profiles.wordpress.org/slug/).
>
> WordPress X.Y.Z would not have been possible without the contributions of the following people. Their asynchronous coordination to deliver maintenance and security fixes into a stable release is a testament to the power and capability of the WordPress community.

Then the contributor list as one paragraph: linked names, alphabetized, comma-separated.

### `## Backports` (standing)

> As a courtesy, the security fixes are being backported, where necessary, to all branches eligible to receive security fixes (currently through 4.7). As a reminder, **only the most recent version of WordPress is actively supported**. The backports are in progress and will ship as they become ready.

Use "the security fix is being backported" for a single fix. When the backports have already shipped, use "were backported" and drop the last sentence. Confirm the oldest eligible branch with the Security Team; it has been 4.7 since 2025.

### `## How to contribute` (standing)

Same paragraph as the maintenance release, then the props line when the user supplies reviewers.

## Notes on this type

- Categories: Releases for a maintenance release; Releases and Security for a maintenance and security release. Tags: `minor-releases`, `releases`.
- Keep the whole post short. The opening paragraphs, the contributor section, and the contribute paragraph are the entire post for a maintenance release.
- The opener's shape (a count of fixes linked to a Trac query, plus a link to the RC post) dates back to 6.0.1. Earlier posts described the release in a few free sentences; from 6.8.1 the opener is the fixed form above. Do not list individual bug fixes unless the squad asks for a highlight.
- 6.9.2 folded the backports paragraph into the security section without a heading. Use the order above, which 7.1.1 and 7.1.3 both followed.
- Some posts wrote the next release date as "19 August 2026." Use "August 19, 2026" (guide Section 9).
