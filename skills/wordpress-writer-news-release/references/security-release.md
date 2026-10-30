# Security release posts (X.Y.Z, security fixes only)

Loaded by `wordpress-writer-news-release` for minor releases whose only changes are security fixes, and for two related shapes: a **fast-follow release** that fixes a regression introduced by a release published hours or a day earlier, and a **combined post** that announces a minor release and a beta together. A release with both bug fixes and security fixes uses the maintenance reference. The structure is the one used from 6.9.2 through 7.1.4; the standing copy is the wording published for 7.1.4 and 7.1.2, with punctuation normalized to the brand guide.

**How to read this file.** Standing copy appears in blockquotes: reproduce it without the blockquote, with only the marked substitutions. Bold inside a blockquote is bold in the post. Placeholders: `X.Y.Z` is the version, `X.Y` the major it belongs to, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

Security posts are usually written with, or by, the Security Team. Everything about a vulnerability (its description, severity, reporter credit, affected versions, backport status, advisory links, and whether forced updates were enabled) comes from the Security Team's notes and is reproduced as supplied. Add nothing from other sources.

## Facts to collect

- Version and release date; the zip URL (`https://wordpress.org/wordpress-X.Y.Z.zip`) or the download page (`https://wordpress.org/download/`); the HelpHub version page
- The Security Team's summary line for the release (how many fixes, and the severity wording if they gave one), the vulnerability list with reporter credits in their wording, and whether the WordPress.org team enabled forced updates
- Backport status: which branches receive the fix, which minor versions shipped for older branches, and whether an in-progress beta also received the fix
- CVE and GHSA advisory links, when the Security Team supplies them
- The release leads with profile URLs, and the contributor list with profile URLs, from the Security Team
- The next major version and its planned date, if the Security Team wants it mentioned
- For a fast-follow release: the earlier release's post URL, the Security Team's description of the regression and its cause, and who helped find and fix it

## Structure: security release

### Title (standing)

`WordPress X.Y.Z Release`. Most recent security releases (6.8.3 through 7.1.2) used this form; 7.1.4 and 6.5.5 used the bare `WordPress X.Y.Z`, and 6.0.3 and 6.2.2 used `WordPress X.Y.Z Security Release`. Any of the three is acceptable when the Security Team prefers it; default to the first.

### Opener (standing with substitutions)

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

Optional standing paragraphs, when the Security Team wants them:

> WordPress X.Y.Z is a short-cycle release. The next major release will be [version X.Y+1](https://make.wordpress.org/core/X-Y/), currently planned for [Month D].
>
> For more information, please visit the [WordPress X.Y.Z HelpHub site](https://wordpress.org/documentation/wordpress-version/version-X-Y-Z/).

### `## Security updates included in this release` (standing lead-in, release-specific list)

Use the singular heading `## Security update included in this release` for one fix.

> The security team would like to thank the following people and organizations for responsibly reporting vulnerabilities, and allowing them to be fixed in this release:

- [Issue as the Security Team describes it], reported by [Name](URL) ([organization]).

One item per vulnerability, in the Security Team's order and wording. Credits take the forms the team uses: "reported by [Name](URL)", "reported by Name of the WordPress Security Team", "reported by [Organization](URL)", "independently discovered by A and B", "reported as a team by A, B, and C". For a single fix, the section may be one paragraph instead of a list: "The security team would like to thank [Name](URL) for responsibly disclosing that [issue as described]."

### `## Thank you to these WordPress contributors` (standing with substitutions)

> This release was led by [Name](https://profiles.wordpress.org/slug/) and [Name](https://profiles.wordpress.org/slug/). WordPress X.Y.Z would not have been possible without the contributions of the following people:

Then the contributor list as one paragraph: linked names, alphabetized, comma-separated, as supplied. 6.8.3 through 7.0.3 opened the second sentence with "In addition to the security researchers mentioned above," and 7.0.2 said "significant contributions"; 7.1.2 and 7.1.4 dropped both. When the Security Team names people who gave significant input, the lead sentence may carry it ("led by Name, with significant input from Name and Name").

### `## CVE and GHSA references` (release-specific, only when supplied)

> Further details can be found in the advisory: [CVE-YYYY-NNNNN / GHSA-xxxx-xxxx-xxxx](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-xxxx-xxxx-xxxx).

For several advisories, use a bulleted list of the same links with no lead-in sentence.

### `## Backports` (standing, or release-specific when versions differ)

> As a courtesy, the security fixes were backported to all branches eligible to receive security fixes (currently through 4.7). As a reminder, **only the most recent version of WordPress is actively supported**. The backports are in progress and will ship as they become ready.

Use "the security fix was backported" for a single fix, and drop the last sentence when the backports have shipped. When an in-progress beta also received the fixes, add: "WordPress X.Y Beta N has also been released, containing all applicable fixes." When branches are affected differently, replace the paragraph with the Security Team's bulleted list, one branch per item, as 7.0.2 did ("WordPress 6.9 is affected by both vulnerabilities. Version 6.9.5 has been released containing fixes for both.").

### `## How to contribute` (standing, optional)

Recent security posts end at "Backports" or "CVE and GHSA references." Include the contribute paragraph from the maintenance reference only when the Security Team wants it.

No haiku, no props line.

## Structure: fast-follow release

A release that fixes a regression from a release published hours or a day earlier (6.9.3 followed 6.9.2 the same day; 6.9.4 followed the next day). Title: `WordPress X.Y.Z Release`. The opening is release-specific and follows this order:

1. A link to the earlier release and what it addressed ("[WordPress 6.9.2 was released earlier today](URL) and addressed 10 security issues.").
2. What was reported and what caused it, in the Security Team's words, with the cause explained plainly and without blame.
3. The decision: "As a result, the Security Team has decided to address this in a fast follow X.Y.Z release."
4. The standing bold update line, with the reason: "As always, **it is recommended that you update your sites to the latest version of WordPress immediately.** This ensures your site is protected by all available security fixes in [earlier version] and that you will not be affected by the bug fixed in X.Y.Z."
5. Thanks to those who reported, narrowed down, and fixed the issue, naming and linking the people the Security Team credits.
6. The standing download and HelpHub paragraphs.

When a fast-follow re-applies fixes that were not fully applied (6.9.4 did, the day after 6.9.2 and 6.9.3), it adds a "Security updates included in this release" list naming the fixes it completes, in the Security Team's wording.

## Structure: combined minor release and beta post

When security fixes ship in a minor release and a new beta on the same day, one post can cover both (6.9.3 and 7.0 Beta 4, published as "WordPress 6.9.3 and 7.0 beta 4"). Title: `WordPress X.Y.Z and X.Y+1 Beta N`, with "Beta" capitalized as the other beta titles have it. The minor release section comes first, as above. Then:

`## WordPress X.Y+1 Beta N`

One paragraph that names the next major and its planned date, then why the beta was packaged ("The next major release of WordPress will be [version X.Y+1](https://make.wordpress.org/core/X-Y/), which is planned for Month D, YYYY. The Security Team has decided to package a new beta release (X.Y+1 Beta N) to keep everyone protected from the patched vulnerabilities, including the dedicated members of the community focusing their time and effort on testing the upcoming release."). Then a bold sentence on how the schedule changes, with the next milestone's date ("**This will be an additional beta release in the X.Y+1 release cycle.** The schedule will remain the same going forward, but with five total beta releases instead of the previously planned four. The next X.Y+1 beta release is still scheduled for [day, Month D]."). Then the beta disclaimer and the how-to-test table from the beta reference, then `## Beta N updates and highlights` with the counts sentence and query links from the beta reference, noting that the beta contains the security patches. Close with "As always, a successful release depends on your confirmation during testing. So please download and test!" and the props line. No haiku.

## Notes on this type

- Categories: Releases and Security. Tags: `minor-releases`, `releases`.
- Several posts (6.5.5, 6.9.2, 6.9.4, 7.0.2 as an H2; 7.0.3 and 7.0.4 as an H1) opened with a "WordPress X.Y.Z is now available" heading inside the body. Do not add a heading above the opener; the title is the heading.
- Never describe how a vulnerability could be exploited, estimate how many sites are affected, or add mitigation steps. The bold update line and the backports paragraph are the guidance.
- Where profile links use the short form (`https://w.org/@username`), keep whichever form the supplied list uses; do not mix forms in one list.
