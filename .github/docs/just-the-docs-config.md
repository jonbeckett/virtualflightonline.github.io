# just-the-docs: Configuration (_config.yml)

Full reference for `_config.yml` options specific to just-the-docs, with examples relevant to this site.

## Minimum viable config

```yaml
title: Site Title
remote_theme: just-the-docs/just-the-docs
url: "https://owner.github.io"
```

## Current site config

```yaml
title: Virtual Flight Online
description: Your online home for virtual flight simulation
remote_theme: just-the-docs/just-the-docs
url: "https://virtualflightonline.github.io"
aux_links:
  "GitHub":
    - "https://github.com/jonbeckett/virtualflightonline.github.io"
footer_content: "&copy; Virtual Flight Online"
color_scheme: light
back_to_top: true
back_to_top_text: "Back to top"
search_enabled: true
```

## Color schemes

```yaml
color_scheme: light    # default
color_scheme: dark
color_scheme: my-scheme  # custom SCSS color scheme in _sass/color_schemes/
```

## Logo and favicon

```yaml
logo: "/assets/images/logo.png"
favicon_ico: "/assets/images/favicon.ico"
```

Place images under `assets/images/`. If the favicon is at `/favicon.ico`, you don't need to set this.

## Search

```yaml
search_enabled: true   # default

search:
  heading_level: 2           # Split pages into sections at h2 (1–6)
  previews: 3                # Max search result previews
  preview_words_before: 5
  preview_words_after: 10
  tokenizer_separator: /[\s/]+/
  rel_url: true              # Show relative URL in results
  button: false              # Floating search button
  focus_shortcut_key: 'k'    # Ctrl+K / Cmd+K to focus search
```

## Navigation sidebar

```yaml
nav_enabled: true    # Set false to hide sidebar site-wide
nav_sort: case_insensitive  # Make alphabetical sort ignore case
```

## Heading anchor links

```yaml
heading_anchors: true   # Hover anchors on h1–h6 (default: true)
```

## Back to top

```yaml
back_to_top: true
back_to_top_text: "Back to top"
```

## Aux links (top-right navigation)

```yaml
aux_links:
  "Label":
    - "https://example.com"
aux_links_new_tab: false   # Open in new tab (default: false)
```

## Footer

```yaml
footer_content: "Copyright &copy; 2025"

# "Edit on GitHub" link in footer
gh_edit_link: true
gh_edit_link_text: "Edit this page on GitHub"
gh_edit_repository: "https://github.com/owner/repo"
gh_edit_branch: "main"
gh_edit_view_mode: "tree"   # or "edit" to open directly in editor

# "Last modified" timestamp (requires last_modified_date in front matter)
last_edit_timestamp: true
last_edit_time_format: "%b %e %Y"
```

## Callouts

Callouts must be declared in `_config.yml` before they can be used in Markdown.

```yaml
callouts:
  note:
    title: Note
    color: purple
  warning:
    title: Warning
    color: red
  important:
    title: Important
    color: blue
  new:
    title: New
    color: green
  highlight:
    color: yellow     # no title = untitled callout
```

Predefined colors: `grey-lt`, `grey-dk`, `purple`, `blue`, `green`, `yellow`, `red`.  
Custom colors require SCSS in `_sass/custom/setup.scss`.

## Mermaid diagrams

```yaml
mermaid:
  version: "9.1.3"   # from https://cdn.jsdelivr.net/npm/mermaid/
```

## Collections

To add a document collection as a separate nav group:

```yaml
collections:
  guides:
    permalink: "/:collection/:path/"
    output: true

just_the_docs:
  collections:
    guides:
      name: Guides
      nav_fold: true   # Start collapsed
```

Collections are namespaced: a page in one collection cannot be a child of a page in another, or of a normal page.

## Google Analytics

```yaml
ga_tracking: "G-XXXXXXXXXX"
ga_tracking_anonymize_ip: true
```

## Front matter defaults

Apply layout or other values to all pages without repeating in each file:

```yaml
defaults:
  - scope:
      path: ""
    values:
      layout: default
```

Note: The `github-pages` gem's `jekyll-default-layout` plugin already applies `default` to all pages automatically — you usually don't need this.
