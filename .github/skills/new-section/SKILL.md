---
name: new-section
description: "Create a new top-level navigation section for this Jekyll site — a new folder, a parent index page, and optionally one or more child pages. Use when adding a new group of related pages that needs its own sidebar heading."
argument-hint: "What section do you want to create? (e.g. 'a Guides section with two child pages')"
---

# New Section

Create a new top-level navigation section (folder + `index.md`) with optional child pages.

## References

- [Front matter templates](../new-page/references/frontmatter.md)
- [Current nav structure](../new-page/references/nav-structure.md)
- [Navigation deep dive](../../docs/just-the-docs-navigation.md)

## Procedure

1. **Agree on section title and folder name**
   - Folder name must be lowercase kebab-case (e.g. `guides/`).
   - The `title` in `index.md` front matter is what child pages reference as `parent` — it must match exactly.

2. **Determine nav_order for the section**
   - Read all root-level `.md` files and their `nav_order` values.
   - Check [nav structure](../new-page/references/nav-structure.md) for a quick reference.
   - Use the next integer after the current highest top-level `nav_order`. Do not reuse values.

3. **Create the section index** at `<folder>/index.md`

   ```yaml
   ---
   title: Section Title
   nav_order: N
   ---
   ```

   Follow with a `# Section Title` heading and an overview paragraph.

   > `has_children: true` is redundant in just-the-docs v0.10.0+ — do not add it.

4. **Create child pages** (if requested)
   - Each child lives at `<folder>/<slug>.md`.
   - Use child page front matter: `parent` must exactly match the section `title`.
   - Assign sequential `nav_order` values starting from 1.
   - See [front matter reference](../new-page/references/frontmatter.md).

5. **Update the nav-structure reference** at [nav-structure.md](../new-page/references/nav-structure.md) to reflect the new section and any child pages.

6. **Confirm** — summarise the folder, section title, nav_order, and any child pages created.
