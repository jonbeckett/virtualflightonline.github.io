# Virtual Flight Online — GitHub Pages Site

## Project Overview

This is a Jekyll static site hosted on GitHub Pages using the [just-the-docs](https://just-the-docs.com/) remote theme. All content is written in Markdown. The site is built automatically by GitHub Pages on every push to the default branch.

Key files:
- `_config.yml` — site title, theme, aux links, footer, colour scheme, search
- `Gemfile` — pins `github-pages` gem and plugins for local development
- `index.md` — home page (uses `layout: home`)

## Site Structure

Top-level pages live in the project root. Sections are sub-folders that each contain an `index.md` as the section parent, with sibling Markdown files as children.

```
root/
  index.md                 # home page (nav_order: 1)
  about.md                 # nav_order: 2
  community.md             # nav_order: 3
  codex.md                 # nav_order: 4
  airline.md               # nav_order: 5
  operations/
    index.md               # section parent (nav_order: 6, has_children: true)
    transmitter.md         # nav_order: 1
    transmitter-msfs.md    # nav_order: 2
    transmitter-xplane.md  # nav_order: 3
    transmitter-server.md  # nav_order: 4
    live-radar.md          # nav_order: 5
```

## Front Matter Conventions

### Top-level page
```yaml
---
title: Page Title
nav_order: N
---
```

### Section index (parent with child pages)
```yaml
---
title: Section Title
nav_order: N
---
```

> `has_children: true` is **redundant from just-the-docs v0.10.0 onwards** — parent pages are detected automatically. Do not add it to new pages. Leave it on existing pages that already have it.

### Child page
```yaml
---
title: Child Page Title
parent: Section Title
nav_order: N
---
```

### Grandchild page

From v0.10.0, unlimited nav depth is supported. Just chain `parent` references. `grand_parent` is only needed when titles are not unique across sections.

```yaml
---
title: Grandchild Title
parent: Parent Title
nav_order: N
---
```

### Home page
```yaml
---
title: Welcome
layout: home
nav_order: 1
---
```

### Optional front matter fields
```yaml
nav_exclude: true      # hide from sidebar (404 pages, drafts)
search_exclude: true   # exclude from search index
has_toc: false         # suppress auto child-page list on parent pages
nav_enabled: false     # hide sidebar on this specific page
```

## Navigation Rules

- `nav_order` is an integer; lower numbers appear first in the sidebar.
- `nav_order` is scoped to the parent — child values don't conflict with top-level values.
- The `title` in front matter **must exactly match** the `parent` value in child pages — just-the-docs uses case-sensitive string matching.
- Never duplicate `nav_order` values within the same level — ties cause unstable build ordering.
- Always read sibling front matter before assigning a new `nav_order`.

## Reference documentation

Detailed reference docs live in `.github/docs/`:

| File | Contents |
| --- | --- |
| [jekyll-fundamentals.md](.github/docs/jekyll-fundamentals.md) | Directory structure, front matter, Liquid, _config.yml, local dev |
| [github-pages.md](.github/docs/github-pages.md) | Deployment, allowed plugins, remote themes, constraints |
| [just-the-docs-navigation.md](.github/docs/just-the-docs-navigation.md) | nav_order, parent/child depth, nav_exclude, has_toc |
| [just-the-docs-config.md](.github/docs/just-the-docs-config.md) | All _config.yml options with examples |
| [just-the-docs-ui-components.md](.github/docs/just-the-docs-ui-components.md) | Callouts, tables, code blocks, labels, buttons, Mermaid |
| [just-the-docs-customisation.md](.github/docs/just-the-docs-customisation.md) | SCSS overrides, custom color schemes, include overrides |

## File Naming

- Lowercase kebab-case for all files and folders: `new-page.md`, `my-section/`.
- Child pages live inside the section folder alongside the `index.md`.

## Writing Style

- Use sentence case for headings.
- Keep the front matter `title` and the first `# Heading` on the page consistent.
- Tables use `|` pipe format with a header separator row.
- Avoid raw HTML unless required for embeds or callouts; prefer just-the-docs callout syntax.
- Link to other pages using relative Markdown paths (e.g. `[Transmitter](operations/transmitter.md)`).

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`. GitHub Pages uses the `github-pages` gem to match the production build environment. `_config.yml` changes require a server restart — they are not hot-reloaded.
