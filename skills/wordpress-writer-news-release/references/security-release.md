# Security release posts (X.Y.Z, security fixes only)

Loaded by `wordpress-writer-news-release` for minor releases whose only changes are security fixes, and for two related shapes: a **security-related fast-follow** addressing a regression or incomplete fix after a security release, and a **combined security/beta post**. A maintenance-only fast-follow without that security connection uses the maintenance reference. An ordinary release with both bug fixes and security fixes uses the maintenance reference; use the fast-follow variant here when its explanatory purpose applies. The structure is the one used from 6.9.2 through 7.1.4; the default wording is the wording published for 7.1.4 and 7.1.2, with punctuation normalized to the brand guide.

**How to read this file.** Blockquotes provide default wording; remove the blockquote in the draft. Apply the [requirements, defaults, and evidence rules](../SKILL.md#requirements-defaults-and-evidence). Bold inside a blockquote is bold in the post. Facts and substitutions still require current evidence; approved security wording and attribution must be preserved. Placeholders: `X.Y.Z` is the version, `X.Y` the major it belongs to, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

Security posts are usually written with, or by, the Security Team. Everything about a vulnerability (its description, severity, reporter credit, affected versions, backport status, advisory links, and whether forced updates were enabled) comes from the Security Team's notes and is reproduced as supplied. Add nothing from other sources.

## Facts to collect

- Version and release date; the zip URL (`https://wordpress.org/wordpress-X.Y.Z.zip`) or the download page (`https://wordpress.org/download/`); the HelpHub version page
- The Security Team's summary line for the release (how many fixes, and the severity wording if they gave one), the vulnerability list with reporter credits in their wording, and whether the WordPress.org team enabled forced updates
- Backport status: the oldest eligible branch, confirmed support policy, which branches receive the fix, which minor versions shipped for older branches, and whether an in-progress beta also received the fix
- CVE and GHSA advisory links, when the Security Team supplies them
- The release leads with profile URLs, and the contributor list with profile URLs, from the Security Team
- The next major version and its planned date, if the Security Team wants it mentioned
- For a fast-follow release: the earlier release's post URL, the Security Team's description of the regression and its cause, and who helped find and fix it

## Structure: security release

**Required:** version, approved security summary and update guidance, download/update instructions, and supplied reporter attribution. **Defaults:** the section order and contributor acknowledgment below. **Conditional:** detailed vulnerability list, advisories, backport specifics, next-major schedule, and contribution invitation depend on the Security Team's material. Mark required but unresolved facts without inventing detail. Retain the bold update guidance below unless the team supplies newer approved wording.

### Title (default wording)

`WordPress X.Y.Z Release`. Most recent security releases (6.8.3 through 7.1.2) used this form; 7.1.4 and 6.5.5 used the bare `WordPress X.Y.Z`, and 6.0.3 and 6.2.2 used `WordPress X.Y.Z Security Release`. Any of the three is acceptable when the Security Team prefers it; default to the first.

### Opener (default wording with substitutions)

The first sentence is the Security Team's summary line. Recent forms:

- "This security release features fixes for multiple issues."
- "This security release features a fix for a critical severity security vulnerability."
- "The X.Y.Z security release addresses one critical and one high severity security issue."

> [Security Team summary line.]
>
> **Because this is a security release, it is recommended that you update your sites immediately.**
>
> You can [download WordPress X.Y.Z from WordPress.org](https://wordpress.org/wordpress-X.Y.Z.zip), or visit your WordPress Dashboard, click "Updates", and then click "Update Now". If you have sites that support automatic background updates, the update process will begin automatically.

7.1.2 and 7.1.4 linked the download page (`https://wordpress.org/download/`) instead of the zip; either works. When forced updates were enabled, the Security Team's sentence follows the bold line, as 7.0.2 did: "Due to the severity, the WordPress.org team have enabled forced updates via the auto-update system for sites running affected versions."

Optional default paragraphs, when the Security Team wants them:

> WordPress X.Y.Z is a short-cycle release. The next major release will be [version NEXT_MAJOR_VERSION]([NEXT_MAJOR_SCHEDULE_URL]), currently planned for [Month D].
>
> For more information, please visit the [WordPress X.Y.Z HelpHub site](https://wordpress.org/documentation/wordpress-version/version-X-Y-Z/).

### `## Security updates included in this release` (default lead-in, approved descriptions and attribution)

Use the singular heading `## Security update included in this release` for one fix.

> The security team would like to thank the following people and organizations for responsibly reporting vulnerabilities, and allowing them to be fixed in this release:

- [Issue as the Security Team describes it], reported by [Name](URL) ([organization]).

One item per vulnerability, in the Security Team's order and wording. Credits take the forms the team uses: "reported by [Name](URL)", "reported by Name of the WordPress Security Team", "reported by [Organization](URL)", "independently discovered by A and B", "reported as a team by A, B, and C". For a single fix, the section may be one paragraph instead of a list: "The security team would like to thank [Name](URL) for responsibly disclosing that [issue as described]."

### `## Thank you to these WordPress contributors` (default wording with substitutions)

> This release was led by [Name](https://profiles.wordpress.org/slug/) and [Name](https://profiles.wordpress.org/slug/). WordPress X.Y.Z would not have been possible without the contributions of the following people:

Then the contributor list as one paragraph: linked names, alphabetized, comma-separated, as supplied. 6.8.3 through 7.0.3 opened the second sentence with "In addition to the security researchers mentioned above," and 7.0.2 said "significant contributions"; 7.1.2 and 7.1.4 dropped both. When the Security Team names people who gave significant input, the lead sentence may carry it ("led by Name, with significant input from Name and Name").

### `## CVE and GHSA references` (release-specific, only when supplied)

> Further details can be found in the advisory: [CVE-YYYY-NNNNN / GHSA-xxxx-xxxx-xxxx](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-xxxx-xxxx-xxxx).

For several advisories, use a bulleted list of the same links with no lead-in sentence.

### `## Backports` (conditional; confirmed facts required)

> As a courtesy, the security fixes [BACKPORT_STATUS] to eligible branches through [OLDEST_ELIGIBLE_BRANCH]. [CONFIRMED_SUPPORT_POLICY]

Use the Security Team's confirmed scope and status. `[BACKPORT_STATUS]` is "have been backported" only for completed work, or "are being backported" for work in progress. Add a progress sentence only if supported. When branches differ, use the team's per-branch list of affected branches, released versions, and pending fixes. Never infer the oldest eligible branch or support policy from an older post. If these facts are unavailable, leave `[BACKPORT DETAILS TO CONFIRM]` and identify the gap in editor notes.

Mention a concurrent beta only when the team confirms its actual version and included fixes. Do not claim it contains every fix if only some apply.

### `## How to contribute` (default wording, optional)

Recent security posts end at "Backports" or "CVE and GHSA references." Include the contribute paragraph from the maintenance reference only when the Security Team wants it.

For a standalone security release, no haiku or props line by default. The combined variant below includes props.

## Structure: security-related fast-follow release

Use this explanation for a confirmed follow-up to a security release, not every rapidly shipped maintenance release. Examples: [6.9.3](https://wordpress.org/news/2026/03/wordpress-6-9-3-and-7-0-beta-4/) followed 6.9.2 the same day; 6.9.4 completed security fixes the next day. Title: `WordPress X.Y.Z Release`. The opening is release-specific and follows this order:

1. A link to the earlier release and what it addressed ("[WordPress 6.9.2 was released earlier today](URL) and addressed 10 security issues.").
2. What was reported and what caused it, in the Security Team's words, with the cause explained plainly and without blame.
3. The confirmed decision and responsible team. Name the Security Team as decision-maker only when the supplied evidence does.
4. The approved update guidance, with the confirmed reason; use this example only when its claims apply: "As always, **it is recommended that you update your sites to the latest version of WordPress immediately.** This ensures your site is protected by all available security fixes in [earlier version] and that you will not be affected by the bug fixed in X.Y.Z."
5. Thanks to those who reported, narrowed down, and fixed the issue, naming and linking the people the Security Team credits.
6. The default download and HelpHub paragraphs.

When a fast-follow re-applies fixes that were not fully applied (6.9.4 did, the day after 6.9.2 and 6.9.3), it adds a "Security updates included in this release" list naming the fixes it completes, in the Security Team's wording.

## Structure: combined security-related minor release and beta post

When security fixes ship in a minor release and a new beta on the same day, one post can cover both (6.9.3 and 7.0 Beta 4, published as "WordPress 6.9.3 and 7.0 beta 4"). Title: `WordPress X.Y.Z and NEXT_MAJOR_VERSION Beta N`, with "Beta" capitalized as the other beta titles have it. The minor release section comes first, as above. Then:

`## WordPress NEXT_MAJOR_VERSION Beta N`

Explain why the beta was packaged from the supplied evidence. Name its actual version, applicable security fixes, and confirmed schedule; add a schedule-change note only when a change is confirmed. Do not carry forward the example's five-beta schedule or infer the next major version.

Load the [beta reference](beta-release.md) for the production-use warning and testing methods, substituting this beta's exact download, command, and Playground target. Keep stable-site update guidance in the minor-release section and testing-only guidance in the beta section. Add `## Beta N updates and highlights` with the supported changes since the actual previous shipped milestone. Counts are optional when unavailable. Close with a testing invitation and supplied props or a reviewer placeholder, unless omitted by the user. No haiku by default in this combined variant.

## Notes on this type

- Categories: Releases and Security. Tags: `minor-releases`, `releases`.
- Several posts (6.5.5, 6.9.2, 6.9.4, 7.0.2 as an H2; 7.0.3 and 7.0.4 as an H1) opened with a "WordPress X.Y.Z is now available" heading inside the body. Do not add a heading above the opener; the title is the heading.
- Never describe how a vulnerability could be exploited, estimate how many sites are affected, or add mitigation steps. The bold update line and the backports paragraph are the guidance.
- Preserve supplied credit links, including short WordPress.org profiles, external URLs, and unlinked reporter names. Do not normalize attribution to a different identity or URL for stylistic consistency.
