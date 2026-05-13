# Front Matter Templates

## Top-level page

```yaml
---
title: Page Title
nav_order: N
---
```

## Section index (parent with child pages)

```yaml
---
title: Section Title
nav_order: N
---
```

> `has_children: true` is **not required** in just-the-docs v0.10.0+. Parent pages are detected automatically from child `parent` references. Omit it on new pages.

## Child page

```yaml
---
title: Child Page Title
parent: Section Title
nav_order: N
---
```

## Grandchild page

For unlimited depth, just chain `parent` values. `grand_parent` is only needed when two sections have a page with the same title.

```yaml
---
title: Grandchild Title
parent: Parent Title
nav_order: N
---
```

## Home page (special — do not replicate)

```yaml
---
title: Welcome
layout: home
nav_order: 1
---
```

## Optional front matter fields

```yaml
nav_exclude: true      # hide from sidebar (useful for 404, drafts)
search_exclude: true   # exclude from search index
has_toc: false         # suppress auto child-page list at bottom of parent
nav_enabled: false     # hide sidebar on this page only
```

## Key rules

- `parent` must **exactly match** the `title` of the parent page — case-sensitive, character-for-character.
- `nav_order` is scoped within a parent — child values do not conflict with top-level values.
- Never duplicate `nav_order` values within the same parent level — ties cause unstable ordering.
- Omit `layout` for regular content pages — just-the-docs applies `default` automatically.
- The first `# Heading` after the front matter should match `title` exactly.
