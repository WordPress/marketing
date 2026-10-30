# Release post format history, 6.0 to 7.2

Maintenance notes for `wordpress-writer-news-release`. Not loaded at runtime. This records what the skill's type references are based on, so the next person updating them can see what changed and when. Source: the 121 release posts (plus one live product demo announcement) in the WordPress.org/news Releases category from 6.0 Beta 1 (April 12, 2022) through 7.1.4 (October 28, 2026), pulled from the WordPress.org/news REST API on October 30, 2026.

## What has stayed constant since 6.0

- Every release type has a fixed opener and a fixed closing block, and each type keeps its own section order for several releases at a time.
- Betas and RCs end with a haiku (6.0 Beta 1 is the only exception); majors stopped including one after 6.6; minors never had one.
- Betas, RCs, and most maintenance posts end with a line crediting the people who reviewed the post ("Props to..." since 6.9; "Thank you to the following contributors for collaborating on this post" before that). Majors do not; security posts usually do not.
- Major release titles are `WordPress X.Y "Name"`; the slug is the code name only; the post publishes under the release lead.
- Major posts always include: an artist tribute, a feature walkthrough, "Learn more," the release squad, a contributor thank-you with the `[wpcredits X.Y]` list and translation stats, and a closing invitation to contribute. Accessibility and performance usually get their own sections (7.0 folded them into the features; 6.2 had performance only).
- Minor posts always include: what the release fixes with a Trac query, the update and download paragraph, a contributors section led by "This release was led by," and (for security fixes) a backports paragraph.

## What changed, by cycle

| Cycle | Change |
|---|---|
| 6.0 (2022) | Major opened "Say hello to"; ended with "The WordPress Mission & You" and a haiku. Beta posts titled "Beta N" with "How to Help" and "Some Highlights"; RC titles ended "Now Available for Testing." |
| 6.1 | Beta and RC titles appended "Now Available." Major gained ~20 feature subsections and "Other notes of interest." |
| 6.2 | Titles return to the bare `WordPress X.Y Beta N` and `Release Candidate N` forms. Major feature headings at `####`. |
| 6.3 | A single template adopted for beta and RC posts (documented in the handbook's release cycle guide): title, intro, what's new, ways to contribute, how to get the build, bounty, update your plugin or theme (RC), translate (RC), haiku, credits. Major gained "WordPress is a global software platform" and "Looking toward the future" (one-off). No Beta 1 was published (packaging issue; Beta 2 was the first). |
| 6.4 | Major used "Looking ahead" and a "Get involved" subsection. Beta 1 grew to 2,300 words with per-feature sections. |
| 6.5 | Beta 1 at 3,100 words, the longest. Major split "What's inside" from "What's fresh for developers" and dropped the closing "Looking ahead" section (last used in 6.4). Later betas adopted "How to test this release" and "Beta N updates and highlights." RC posts renamed 6.4's "Ways to contribute" to "How you can contribute," keeping its four subsections (Get involved in testing, Search for vulnerabilities, Update your theme or plugin, Help translate WordPress). The "What's in WordPress X.Y RC1?" heading dates to 6.0. Bounty sections (begun at 6.3 Beta 2) continued through 6.8, skipped by a few late RCs. |
| 6.6 | Major shortened to four features plus Performance and Accessibility, and introduced the "And much more" showcase link and button. Last major with a haiku. Beta 1 introduced "How important is your testing?"; later betas briefly used "If you find an issue" and "The work continues" (one-off). |
| 6.7 | Major opener changed to "Each WordPress release celebrates an artist who has made an indelible mark on the world of music." Major closes with "Get involved"; haiku dropped. Beta 1 adopted "How to Test WordPress X.Y Beta 1" and "What's New in WordPress X.Y Beta 1" alongside "How important is your testing?" |
| 6.8 | Same structure. Beta 1 added a "Caveat on testing in versions older than 5.1" note (one-off). |
| 6.9 | Bounty sections dropped from betas and RCs. RC posts added "Test on your hosting platforms." Major gained bold one-line taglines under feature headings. |
| 7.0 | Beta 1 carried the "intended for testing and development only" disclaimer in the opener. RC1 added "New Features since Beta 1" and a ticket list. Five betas and four RCs; a combined "6.9.3 and 7.0 beta 4" post; RC3 noted the removal of Real Time Collaboration. Major gained a "Developer's toolbox" section. |
| 7.1 | Major settled the heading hierarchy (`##` sections, `###` features, `####` grouped items) and rewrote the contributor paragraph ("Together, their work delivered..."). Beta 1, Betas 3 and 4, and RC1 carried a WordCamp US launch banner. RC1 left out "Help translate WordPress." Minor posts moved to the 7.1.x shapes recorded in the maintenance and security references. |
| 7.2 | Both beta posts placed the release content ("What's new" or "What's in Beta N") before "How important is your testing?"; the beta reference adopts that order. Beta 1 also used Title Case feature headings and appended "is Ready for Download and Testing" to the title (one-offs); Beta 2 returned to the bare title. |

## Posts the references are based on

- Major: 7.1 "Mary Lou" (primary), checked against 7.0, 6.9, 6.8, 6.7.
- Beta 1: 7.2 Beta 1 and 7.1 Beta 1 (primary), 7.0 Beta 1.
- Later betas: 7.2 Beta 2 and 7.1 Beta 4 (primary), 7.0 Beta 2 and Beta 5.
- RC: 7.1 RC1 (primary), 7.0 RC3 for later-RC variants and the translate section, 6.9 RC1 through RC3.
- Maintenance: 7.0.1 (primary), 6.9.1, 6.8.1, 6.8.2.
- Maintenance and security: 7.1.3 (primary), 7.1.1.
- Security: 7.1.4 and 7.1.2 (primary), 7.0.2 for the per-branch backports list, 6.9.2.
- Fast-follow and combined: 6.9.3 and 7.0 Beta 4, 6.9.4.

## Updating the references

When a new release publishes with a structural change that holds for two consecutive posts of the same type, update that type's reference and add a row above. One-off variations stay in the notes at the end of each reference. The Releases category (https://wordpress.org/news/category/releases/) lists every post for comparison.
