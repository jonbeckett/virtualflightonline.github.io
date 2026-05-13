---
name: configure-site
description: "Update _config.yml settings for this Jekyll just-the-docs site. Use when changing the site title, description, color scheme, callout colours, search settings, logo, favicon, footer, aux links, Mermaid support, or any other site-wide configuration."
argument-hint: "What do you want to configure? (e.g. 'add callouts', 'enable dark mode', 'add a logo')"
---

# Configure Site

Update `_config.yml` for this just-the-docs Jekyll site.

## References

- [Full config reference](../../docs/just-the-docs-config.md)
- [Customisation guide](../../docs/just-the-docs-customisation.md)

## Current config file

`_config.yml` in the project root.

## Procedure

1. **Read the current `_config.yml`** before making any changes.

2. **Identify the setting** the user wants to change using [just-the-docs-config.md](../../docs/just-the-docs-config.md).

3. **Edit `_config.yml`** — add or update only the relevant keys. Do not reorganise unrelated settings.

4. **Check for SCSS dependencies**
   - If adding a callout with a custom colour (not one of: `grey-lt`, `grey-dk`, `purple`, `blue`, `green`, `yellow`, `red`), the colour's `000` and `300` SCSS levels must be defined in `_sass/custom/setup.scss`.
   - If adding a logo or favicon, confirm the asset file exists under `assets/`.

5. **Warn about restarts**
   - `_config.yml` changes require restarting `jekyll serve` locally — they are not hot-reloaded.

6. **Confirm** — summarise what was changed and the expected effect.

## Common tasks

### Add callouts

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
    color: yellow
```

### Switch to dark mode

```yaml
color_scheme: dark
```

### Add a logo

```yaml
logo: "/assets/images/logo.png"
```

### Enable Mermaid diagrams

```yaml
mermaid:
  version: "9.1.3"
```

### Enable "Edit on GitHub" footer link

```yaml
gh_edit_link: true
gh_edit_link_text: "Edit this page on GitHub"
gh_edit_repository: "https://github.com/jonbeckett/virtualflightonline.github.io"
gh_edit_branch: "main"
gh_edit_view_mode: "tree"
```
