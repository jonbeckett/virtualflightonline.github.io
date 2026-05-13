# just-the-docs: Navigation

just-the-docs builds its left sidebar navigation entirely from page front matter. There is no manually maintained nav config file.

## How navigation is built

Every `.md` file with a `title` in its front matter is automatically included in the sidebar. Pages without a `title` are excluded.

The navigation is built from three front matter fields: `title`, `parent`, and `nav_order`.

## Top-level pages

A page with no `parent` is a top-level navigation item.

```yaml
---
title: About
nav_order: 2
---
```

Top-level pages must have unique titles.

## Child pages

Set `parent` to the exact `title` of the parent page. The match is case-sensitive string comparison — it must be character-for-character identical.

```yaml
---
title: Transmitter for MSFS
parent: Operations
nav_order: 2
---
```

Child pages of the same parent must have unique titles. They do **not** need unique titles relative to other sections.

## Parent pages (sections)

A parent page does not need any special marker — having a child page reference its title is enough. The theme adds an expand/collapse chevron automatically.

```yaml
---
title: Operations
nav_order: 6
---
```

> `has_children: true` was required in older versions of just-the-docs but is **redundant from v0.10.0 onwards**. It is harmless to include for backwards compatibility but is not needed for the sidebar to work correctly.

## Grandchild and deeper pages (unlimited depth)

From v0.10.0 the nav supports unlimited depth. Just chain `parent` values:

```yaml
---
title: Line Numbers
parent: Code
---
```

```yaml
---
title: Code
parent: UI Components
---
```

```yaml
---
title: UI Components
nav_order: 3
---
```

> `grand_parent` is still supported for disambiguation when titles are not unique across sections, but can usually be omitted.

## nav_order

`nav_order` controls the order within a level. It is scoped: child `nav_order` values do not conflict with top-level `nav_order` values.

- Lower numbers appear first.
- Values can be integers, floats, or strings.
- Pages with numeric `nav_order` always appear before pages with string or missing `nav_order`.
- Pages with equal `nav_order` values have unstable (unpredictable) ordering — avoid ties.
- If `nav_order` is omitted, pages sort alphabetically by `title`.

## Excluding pages from navigation

```yaml
---
title: 404
nav_exclude: true
permalink: /404
---
```

`nav_exclude: true` hides the page from the sidebar. It does not prevent the page being accessed directly by URL, nor does it remove it from breadcrumbs or child-page lists.

Child pages are automatically excluded when their parent is excluded.

## Disabling the child-page table of contents

By default, parent pages show an auto-generated list of links to their children at the bottom of the page. To suppress it:

```yaml
---
title: Operations
has_toc: false
---
```

## Minimal layout (no sidebar)

To render a page without the navigation sidebar:

```yaml
---
layout: minimal
title: Landing Page
---
```

The `minimal` layout keeps breadcrumbs and child-page lists but removes the sidebar entirely.

## Disabling nav globally

In `_config.yml`:

```yaml
nav_enabled: false
```

Individual pages can re-enable it with `nav_enabled: true` in front matter.

## Search exclusion

```yaml
---
title: Private notes
search_exclude: true
---
```
