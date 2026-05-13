# Jekyll Fundamentals

Jekyll is a static site generator. It reads Markdown (and HTML) source files, processes them through Liquid templates and layouts, then outputs a complete static `_site/` directory. GitHub Pages runs this build automatically on every push.

## Directory structure

```
project/
├── _config.yml          # Site-wide settings (parsed at build time, not at runtime)
├── _data/               # YAML/JSON/CSV files accessible as site.data.*
├── _includes/           # Partial HTML fragments ({% include file.html %})
├── _layouts/            # Page wrapper templates (front matter: layout: name)
├── _sass/               # SCSS partials imported into the main stylesheet
├── _site/               # Build output — never commit this, add to .gitignore
├── .jekyll-cache/       # Build cache — add to .gitignore
├── assets/              # CSS, JS, images — copied verbatim to _site/
├── Gemfile              # Ruby dependencies (github-pages gem)
└── *.md / *.html        # Content pages with front matter
```

Files and folders beginning with `.`, `_`, `#` or `~` are **not** output to `_site/` unless explicitly included. This means `.github/` is never part of the built site.

## Front matter

Every page that Jekyll should process must start with a YAML front matter block:

```yaml
---
title: My Page
layout: default
nav_order: 3
---
```

Pages without front matter are copied to `_site/` as-is (static assets). Front matter can be defaulted for entire directories using `defaults:` in `_config.yml`.

## _config.yml

Site-wide settings. Changes require a full restart of `jekyll serve` — they are not hot-reloaded.

```yaml
title: My Site
description: A short description
url: "https://example.github.io"
remote_theme: just-the-docs/just-the-docs

# Front matter defaults (apply layout to all pages automatically)
defaults:
  - scope:
      path: ""
    values:
      layout: default
```

## Liquid templating

Liquid is used inside layouts and includes, not normally in page Markdown. Key syntax:

```liquid
{{ variable }}            # Output a value
{% if condition %}        # Conditional block
{% for item in list %}    # Loop
{% include file.html %}   # Include a partial
{{ page.title }}          # Access front matter
{{ site.title }}          # Access _config.yml value
```

## Gemfile and local development

The `Gemfile` pins the `github-pages` gem, which bundles the exact Jekyll version and plugins that GitHub Pages uses.

```ruby
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
group :jekyll_plugins do
  gem "jekyll-remote-theme"
end
```

```bash
bundle install          # Install gems (first time / after Gemfile changes)
bundle exec jekyll serve  # Serve at http://localhost:4000 with live reload
bundle exec jekyll build  # Build _site/ without serving
```

## What does and doesn't build on GitHub Pages

GitHub Pages forces these Jekyll settings (cannot be overridden):
- `safe: true` — no arbitrary plugins
- `lsi: false`
- `incremental: false`
- `highlighter: rouge`
- `kramdown` with `mathjax` math engine

Allowed plugins are those included in the `github-pages` gem. See https://pages.github.com/versions for the full list. Custom plugins that are not on the allowlist will be silently ignored.

## Syntax highlighting

Use fenced code blocks with a lowercase language identifier:

````markdown
```python
def hello():
    return "world"
```
````

Rouge is the highlighter. Language identifiers must be lowercase.

## .gitignore recommendations

```
_site/
.jekyll-cache/
.jekyll-metadata
.bundle/
vendor/
```
