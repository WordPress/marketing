# Marketing Team Handbook

Source for the [Marketing Team Handbook](https://make.wordpress.org/marketing/handbook/) on WordPress.org.

Once the Meta team enables the sync, WordPress.org imports the handbook from this directory. Content, title, and slug edits made in the WordPress editor are discarded on the next sync, so all changes go through pull requests here.

## How the sync works

* `manifest.json` lists every page: its URL path (the key), `title`, `slug`, `parent`, `order`, and the Markdown file to import (`markdown_source`).
* WordPress.org fetches the manifest and each Markdown file from the `main` branch on a cron schedule (hourly by default) and creates or updates the matching handbook pages.
* The first line of each file (`# Title`) becomes the page title. Everything after it is the page body.
* Markdown is rendered with Jetpack's GitHub-flavored Markdown parser, then filtered with the same HTML rules as a classic-editor post. Plain Markdown and simple inline HTML work; blocks, scripts, and iframes do not.
* The importer only creates and updates pages. Removing a page from the manifest does not unpublish it on WordPress.org.

## Layout

* `index.md` is the handbook landing page.
* File paths mirror the live URLs. A section with child pages is a folder: `getting-involved/index.md` is the section page and `getting-involved/coffee-breaks.md` is one of its children.
* `README.md` (this file) is not part of the handbook and is not in the manifest.

## Editing a page

* Open a pull request that changes the `.md` file. Keep the `# Title` line as the first line.
* One paragraph per line. Do not hard-wrap text.
* Line breaks inside a paragraph or list item use `<br>`.
* Tables without a header row and `<code>` spans that contain links are written as inline HTML on purpose. Markdown has no equivalent that renders the same way.
* Images: upload to the Make Marketing media library and reference the `make.wordpress.org/marketing/files/...` URL. Do not commit image files here.
* Embeds (WordPress.org posts, YouTube, etc.): put the URL on its own line. WordPress auto-embeds it on the site.
* `#hashtags` are plain text. The site links them to the tag archive on render.
* Glossary terms (P2, Slack, Gutenberg, etc.) are plain text. The site adds the tooltip on render.
* Write in line with the [WordPress Brand Writing Style Guide](resources/style-guide-and-brand-book.md).

## Adding, moving, or removing a page

* Add: create the file, then add a `manifest.json` entry. The key is the URL path below `/handbook/`, `slug` is the last segment of the key, `parent` is the parent's key (or `null` for a top-level section), and `order` sets the position among siblings. Keep `markdown_source` pointing at the file on `main`.
* Move or rename: change the key, `slug`, and `markdown_source` together. Slugs must be lowercase with hyphens; the importer rejects anything else.
* Remove: delete the file and the manifest entry, then ask in the `#meta` Slack channel or on a [Meta Trac](https://meta.trac.wordpress.org/) ticket for the page to be unpublished.
