---
name: new-page
description: "Create a new Jekyll Markdown page for this site with correct just-the-docs front matter and navigation order. Use when adding any new page — top-level, child of an existing section, or grandchild."
argument-hint: "What page do you want to create? (e.g. 'a guides page under Operations')"
---

# New Page

Create a new Markdown page with the correct Jekyll front matter for this just-the-docs site.

## References

- [Front matter templates](./references/frontmatter.md)
- [Current nav structure](./references/nav-structure.md)
- [Navigation deep dive](../../docs/just-the-docs-navigation.md)

## Procedure

1. **Clarify placement**
   - Is this a top-level page (root folder) or a child inside an existing section?
   - If child: which section? Check [nav structure](./references/nav-structure.md).

2. **Determine nav_order**
   - Read the front matter of all sibling pages (same folder, same parent).
   - Use the next integer after the current highest `nav_order`. Do not reuse existing values — ties produce unstable ordering.

3. **Choose the file path**
   - Top-level: `<slug>.md` in the project root.
   - Child page: `<section-folder>/<slug>.md`.
   - Use lowercase kebab-case for the filename.

4. **Create the file** using the matching template from [front matter reference](./references/frontmatter.md).

5. **First heading** — add a `# Heading` immediately after the front matter that matches the front matter `title` exactly.

6. **Parent sections** — `has_children: true` is redundant in just-the-docs v0.10+. Do **not** add it unless the parent's `index.md` already has it (leave existing files unchanged).

7. **Confirm** — summarise the file path, title, nav_order, and parent (if any) before finishing.
