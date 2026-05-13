# just-the-docs: Customisation

How to change colours, styles, layouts, and includes without forking the theme.

## SCSS overrides (recommended approach)

The theme exposes two SCSS override points:

### 1. `_sass/custom/setup.scss` — variables and functions

Use this to define custom SCSS variables before any CSS is emitted — typically for custom callout colours.

```scss
// _sass/custom/setup.scss
$pink-000: #f77ef1;
$pink-300: #dd2cd4;
```

Do **not** put CSS rules here.

### 2. `_sass/custom/custom.scss` — custom CSS rules

Use this to override specific CSS classes or add new styles.

```scss
// _sass/custom/custom.scss

// Example: print styles
@media print {
  .side-bar,
  .page-header { display: none; }
  .main-content { max-width: auto; margin: 1em; }
}

// Example: widen the content area
.main-content {
  max-width: 1000px;
}
```

## Color schemes

### Built-in

```yaml
# _config.yml
color_scheme: light   # default
color_scheme: dark
```

### Custom scheme

Create `_sass/color_schemes/my-scheme.scss`. Override theme variables:

```scss
// _sass/color_schemes/my-scheme.scss
$body-background-color: #1a1a2e;
$body-text-color: #e0e0e0;
$link-color: $blue-000;
```

Available variables are in the theme's `_sass/support/_variables.scss`. Use the GitHub source to browse them: https://github.com/just-the-docs/just-the-docs/blob/main/_sass/support/_variables.scss

Enable the scheme:

```yaml
# _config.yml
color_scheme: my-scheme
```

Note: custom schemes implicitly extend `light`. To base on `dark`:

```scss
@import "./color_schemes/dark";
// ... your overrides
```

## Override includes

Copy the theme's include file into your own `_includes/` directory and edit it. Jekyll gives your copy precedence over the theme's.

| Include | Purpose |
| --- | --- |
| `_includes/footer_custom.html` | Content at the bottom of every page |
| `_includes/head_custom.html` | Extra `<meta>`, `<link>`, `<script>` before `</head>` |
| `_includes/header_custom.html` | Content between the search bar and aux links |
| `_includes/nav_footer_custom.html` | Content at the bottom of the sidebar |
| `_includes/toc_heading_custom.html` | Heading above the child-page TOC list |
| `_includes/search_placeholder_custom.html` | Search bar placeholder text |

### Example: custom footer

```html
<!-- _includes/footer_custom.html -->
<p>&copy; Virtual Flight Online. Built with Jekyll and just-the-docs.</p>
```

### Example: custom head (e.g. analytics, fonts)

```html
<!-- _includes/head_custom.html -->
<link rel="preconnect" href="https://fonts.googleapis.com">
```

### Example: custom TOC heading

```html
<!-- _includes/toc_heading_custom.html -->
<h2 class="text-delta">In this section</h2>
```

## Layouts

### default

Used by almost all pages. Includes sidebar, breadcrumbs, header, footer, child-page TOC.

### minimal

No sidebar. Useful for landing pages or pages that don't need navigation.

```yaml
---
layout: minimal
title: Landing Page
---
```

### home

Extends `default`. Used for the home page (set `layout: home` in front matter).

### Disabling the sidebar on specific pages

```yaml
---
layout: default
nav_enabled: false
---
```

Or globally in `_config.yml`:

```yaml
nav_enabled: false
```

Then selectively re-enable:

```yaml
---
nav_enabled: true
---
```

## Repo layout best practices

```
project/
├── _config.yml
├── Gemfile
├── .gitignore             # include _site/, .jekyll-cache/, .bundle/, vendor/
├── index.md               # home page (layout: home)
├── about.md               # top-level pages
├── <section>/
│   ├── index.md           # section parent
│   ├── child-page.md      # child pages
│   └── sub-section/
│       ├── index.md       # grandchild section
│       └── leaf-page.md
├── assets/
│   └── images/            # images referenced from pages
├── _sass/
│   └── custom/
│       ├── setup.scss     # SCSS variables (create if customising)
│       └── custom.scss    # CSS overrides (create if customising)
└── _includes/             # only create files you are overriding
```

Keep `.github/` for Copilot instructions, skills, prompts, and docs. Jekyll ignores it (dotfiles are excluded from `_site/`).
