# Major release post ("WordPress X.Y")

The general availability post for a major release. Loaded by `wordpress-writer-news-release` for this type only. The structure below is the one 7.1 used; every major since 6.7 shares it, except that 7.0 folded its accessibility and performance work into the feature sections. The standing copy is the wording published for 7.1, with punctuation normalized to the brand guide and the two link-text forms noted below taken from 6.7 through 7.0.

**How to read this file.** Standing copy appears in blockquotes: reproduce it without the blockquote, with only the marked substitutions. Bold inside a blockquote is bold in the post. Placeholders: `X.Y` is the version, `X-Y` its slug form, `Name` the jazz artist's code name, `Month D, YYYY` a date, and `[...]` a value to supply. Sections marked **release-specific** are written from the sources.

## Facts to collect

- Version, release date, download URL (`https://wordpress.org/wordpress-X.Y.zip`), and the feature showcase URL (`https://wordpress.org/download/releases/X-Y/`)
- The jazz artist (confidential until release day) and sourced biographical facts
- The priority feature list from the release squad, with each feature's dev note, Field Guide entry, or pull request
- Developer-facing changes, accessibility work, and performance work, each with a source
- Release video URL and feature images with alt text, from the design contributors
- Release notes URL (`https://wordpress.org/documentation/wordpress-version/version-X.Y/`, with a dot; the minor release pages use hyphens) and Field Guide URL
- Squad roster with roles and WordPress.org profile URLs
- Contributor count, first-time contributor count, count of enhancements and fixes, and the number of locales fully translated on day one, each with room below the real figure
- Whether the post should thank hosts that ran pre-release tests (7.0 did)

## Structure

### Title (standing)

`WordPress X.Y "Name"` with the code name in double quotes. No colon, nothing else.

### Featured image (release-specific)

The release artwork featuring the jazz artist, placed at the top of the post. Alt text names the release ("WordPress X.Y release edition featured image") or describes the artwork.

### Opening: the artist tribute (release-specific, with a standing first sentence)

> Each WordPress release celebrates an artist who has made an indelible mark on the world of music. [WordPress X.Y](https://wordpress.org/download/releases/X-Y/), code-named "Name," honors [description of the artist], [artist's full name].

Then one or two short paragraphs about the artist, written from sourced facts: what they played, what they changed, one concrete detail that makes them particular. End with one sentence that connects a quality of the artist to the release ("That combination of reinvention and collaboration inspired WordPress 7.1."). An optional closing line may link to the artist's music ("Let the range of [Artist's music](URL) carry you through everything X.Y offers.").

When the artist has not been supplied, replace this whole section with `[JAZZ ARTIST PASSAGE: supplied on release day]` and leave the code name blank in the title.

### `## Welcome to WordPress X.Y!` (heading standing, paragraph release-specific)

One paragraph that leads with the two to four biggest user-facing changes, each in a sentence that says what the reader can now do. Close the paragraph by pointing into the post ("These are just the highlights. Read on to see everything WordPress X.Y has to offer."). This paragraph is where the News rule to lead with the biggest change is satisfied.

Then the download button (standing):

`Button: [Download WordPress X.Y](https://wordpress.org/wordpress-X.Y.zip)`

### `## What's inside` (release-specific)

A short framing paragraph on the themes of the release. When a release video exists, add the standing lead-in and the embed:

> Here's a closer look at what's new in this release, starting with the release video:

Then one `###` per feature, in priority order. Each feature section is:

1. A sentence-case `###` heading written as a benefit or an action ("Apply responsive styles," "A new way to crop," "Inline notes with mentions and rich text").
2. A bold one-line tagline on its own line ("**Style your content your way, on every screen.**").
3. One or two short paragraphs: what it is, what the reader can now do, where it lives.
4. An image with alt text, when supplied.

Group small related items under one `###` with `####` subheadings (7.1 did this for new blocks and block-level options). Keep the section to roughly six to ten features; everything else belongs in "And much more" via the showcase link.

### `## Developer's toolbox` (release-specific, with a standing tagline)

> **Advanced tools for building your way.**

Then two to four short paragraphs on the APIs and tools that changed, each naming the API and what it now allows, with function names and `theme.json` keys in inline code. Link dev notes where supplied.

### `## Accessibility` (release-specific)

One to three short paragraphs on the accessibility work in the release, naming the specific screens or functions improved. End on what the changes do for people using assistive technology. Give a count only when the squad supplied one.

### `## Performance improvements` (release-specific)

One to three short paragraphs on the performance changes: what now runs where, what loads later, what is cached. Name the mechanism; do not claim a speed figure the squad did not supply.

Include both sections whenever the squad supplies the material; 6.7 through 6.9 and 7.1 did, and 7.0 covered the work inside its feature sections instead.

### `## And much more` (standing)

7.1 published this heading with an exclamation point; 6.6 through 7.0 did not. Use it without.

> For a comprehensive overview of everything new and improved in WordPress X.Y, visit the feature showcase website.

`Button: [Check out what's new in X.Y](https://wordpress.org/download/releases/X-Y/)`

### `## Learn more about WordPress X.Y` (standing)

> [Learn WordPress](https://learn.wordpress.org/) is a free resource for new and experienced WordPress users. Learn is stocked with how-to videos on using various features in WordPress, [interactive workshops](https://learn.wordpress.org/social-learning/) for exploring topics in-depth, and lesson plans for diving deep into specific areas of WordPress.
>
> Read the [WordPress X.Y Release Notes](https://wordpress.org/documentation/wordpress-version/version-X.Y/) for information on installation, enhancements, fixed issues, release contributors, learning resources, and the list of file changes.
>
> Explore the [WordPress X.Y Field Guide]([Field Guide URL]). Learn about the changes in this release with detailed developer notes to help you build with WordPress.

### `## The X.Y release squad` (standing intro, release-specific list)

> Every release comes to you from a dedicated team of enthusiastic contributors who help keep things on track and moving smoothly. The team that has led X.Y is a cross-functional group of contributors who are always ready to champion ideas, remove blockers, and resolve issues.

Then a bulleted list, one role per line, in the roster's order, with every name linked to a WordPress.org profile. Roles used recently: Release Lead, Release Coordination, Tech Leads, Triage Leads, Test Leads. Earlier releases also listed Core and Editor Tech Leads, Documentation Leads, Design Lead, Performance Lead, and Default Theme Design and Development Leads when a default theme shipped. Use the roles the roster gives.

- Release Lead: [Name](https://profiles.wordpress.org/slug/)
- Release Coordination: [Name](URL), [Name](URL)
- Tech Leads: [Name](URL), [Name](URL)
- Triage Leads: [Name](URL), [Name](URL)
- Test Leads: [Name](URL), [Name](URL)

### `## Thank you, contributors` (standing with substitutions)

> The mission of WordPress is to [democratize publishing](https://wordpress.org/about/) and embody the [freedoms that come with open source](https://opensource.org/osd-annotated). A global and diverse community of people collaborating to strengthen the software supports this effort.

(Link text as 6.7 through 7.0 published it; 7.1 linked only "democratize" and only "support" in the forums line below.)
>
> WordPress X.Y reflects the tireless efforts and passion of more than [N] contributors from all over the world. This release also welcomed over [N] first-time contributors!
>
> Together, their work delivered more than [N] enhancements and fixes, helping make WordPress X.Y a stable and polished release for everyone. It's another great example of what the WordPress open source community can accomplish when people come together to build, test, and improve the software.

`[wpcredits X.Y]`

> More than [N locales have fully translated WordPress X.Y](https://translate.wordpress.org/stats/) into their language, making this one of the most translated releases ever on day one. Community translators are working hard to ensure more translations are on their way. Thank you to everyone who helps make WordPress available in 200+ languages.

Keep "making this one of the most translated releases ever on day one" only when the locale count supports it; 6.9 and 7.0 dropped the clause.

Optional, when the squad wants hosts thanked (7.0 did):

> Thank you to the [more than N web hosts](https://make.wordpress.org/hosting/test-results/) that have tested pre-release versions for WordPress X.Y, helping ensure that WordPress and hosting platforms are fully compatible, free of errors, and optimized for the best possible user experience.

Always last in this section:

> Last but not least, thanks to the volunteers who contribute to the [support forums](https://wordpress.org/support/forums/) by answering questions from WordPress users worldwide.

### `## Get involved` (standing)

> Participation in WordPress goes far beyond coding. And learning more and getting involved is easy. Discover the teams that come together to [Make WordPress](https://make.wordpress.org/) and use [this interactive tool](https://make.wordpress.org/contribute/) to help you decide which is right for you.

This is the last section. No haiku, no props line, no sign-off.

## Notes on this type

- The post publishes under the release lead's name. Slug is the code name only. Category: Releases. Tags: `releases` and the version. Write a custom excerpt that names the version, the code name, and the main themes in one or two sentences.
- Feature headings in 6.7 through 7.0 mixed `##` and `###`; 7.1 settled on `##` for the top-level sections listed here and `###` for features. Follow 7.1.
- Majors through 6.6 ended with a haiku (dropped in 6.7). 6.0, 6.1, 6.3, and 6.4 carried a closing "Looking ahead," "Looking toward the future," or "The WordPress Mission & You" section (last used in 6.4). Do not reintroduce either.
- The older opener ("Say hello to WordPress X.Y") is retired. The current opener is the "Each WordPress release celebrates an artist" sentence.
- Images: the featured image, then one image per feature where available. Alt text describes what the screenshot shows ("Command palette showing the ability to navigate across different parts of the site").
