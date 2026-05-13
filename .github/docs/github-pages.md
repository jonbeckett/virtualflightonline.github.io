# GitHub Pages

GitHub Pages is a static site hosting service that automatically builds and publishes a Jekyll site from a repository.

## Site types

| Type | Repository name | Default URL |
| --- | --- | --- |
| User/org site | `<owner>.github.io` | `https://<owner>.github.io` |
| Project site | any name | `https://<owner>.github.io/<repo>` |

This site (`virtualflightonline.github.io`) is a **user site**: the repo name matches `<owner>.github.io`, so it publishes at the root URL with no path prefix.

## How publishing works

1. You push to the default branch (usually `main`).
2. GitHub Pages detects the push and triggers a Jekyll build.
3. The built `_site/` output is deployed to the CDN.
4. The live site updates within a minute or two.

No GitHub Actions workflow is needed for standard Jekyll sites using the `github-pages` gem — GitHub Pages handles the build automatically.

> **Note:** GitHub Actions is the newer recommended approach for more complex build pipelines, but for a standard Jekyll + remote theme site, the classic branch-based deployment is simpler and sufficient.

## Required files

| File | Purpose |
| --- | --- |
| `_config.yml` | Jekyll configuration — must exist |
| `index.md` or `index.html` | Home page — must exist at the root |
| `Gemfile` | Only needed for local development, not required on GitHub Pages |

## The github-pages gem

The `github-pages` gem bundles the specific versions of Jekyll and plugins used by GitHub Pages. Using it locally ensures your local build matches production exactly.

```ruby
# Gemfile
gem "github-pages", group: :jekyll_plugins
```

Run `bundle update github-pages` periodically to stay in sync with what GitHub Pages uses.

## Remote themes

GitHub Pages supports `remote_theme:` as an alternative to `theme:` (which only supports built-in themes). Remote themes load directly from a public GitHub repo:

```yaml
# _config.yml
remote_theme: just-the-docs/just-the-docs
```

You also need the `jekyll-remote-theme` plugin:

```ruby
# Gemfile
gem "jekyll-remote-theme"
```

## Allowed plugins

GitHub Pages allows a fixed set of plugins. Any plugin gem not on the list is silently ignored (it won't cause a build failure, but it also won't run).

Always-on plugins (cannot be disabled):
- `jekyll-coffeescript`
- `jekyll-default-layout`
- `jekyll-gist`
- `jekyll-github-metadata`
- `jekyll-optional-front-matter`
- `jekyll-paginate`
- `jekyll-readme-index`
- `jekyll-relative-links`
- `jekyll-titles-from-headings`

These mean, for example, that pages without front matter will still render, relative links between `.md` files work automatically, and page titles can be inferred from headings.

## Debugging build errors

GitHub Pages will email the repo owner on build failure. You can also see build status under the repository **Settings → Pages** tab. Build errors are also visible in the Actions tab if the repository uses the Pages deployment source via Actions.

The best way to debug is to reproduce locally:

```bash
bundle exec jekyll build --verbose
```

## Custom domains

To use a custom domain:
1. Add a `CNAME` file to the root of the repo containing the domain name.
2. Configure the DNS records with your registrar (CNAME or A records pointing to GitHub's IPs).
3. Set the custom domain in **Settings → Pages**.

## What GitHub Pages cannot do

- Run arbitrary Ruby plugins (only the allowlist)
- Execute server-side code (it is a static host)
- Use Jekyll features that require `safe: false`
- Build from private repos on the free plan
