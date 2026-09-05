# Setting navigation metadata

The name and order shown in the INDEX are written in each document's YAML front matter. Documents are shown even without it, using the heading (H1) and file-name order.

## Document name and order

Write the following at the top of the document.

```yaml
---
navigation:
  title: Getting started
  order: 200
---
```

| Field | Meaning |
|---|---|
| `navigation.title` | The name shown in the INDEX. When omitted, the H1 is used, then the file name |
| `navigation.order` | An integer that determines the order, ascending. When omitted, a stable default order (by file name) applies |

> **Hint**
>
> - Give `order` values in steps of 100, such as 100, 200, 300, so that you can insert 150 between them later.
> - Missing, invalid or duplicate `order` values never hide a document.
> - Reordering in the INDEX writes `navigation.order` for you; there is no need to write it by hand.

## Folder name and order

A folder's name and order belong to the front matter of its `README.md` (or `index.md` when there is no README). The landing page does not need body content.

```yaml
---
navigation:
  title: Product planning
  order: 100
---
```

A folder without a landing page uses its folder name and the default order. When a title change or a reorder in the INDEX requires it, a front-matter-only `README.md` is created. Reading alone never creates a file.

## Translations

- The order and the role of a folder (landing page or configuration-only) are decided by the default-language document alone.
- A translation may override `navigation.title` only. When the canonical document has body content, the translation's H1 is also used as the name.
- A translation on its own never adds a page.

## Child sorting and collapsing

`navigation.children.sort` and `navigation.children.defaultCollapsed` in a folder's landing page are defined for controlling how its direct children are sorted and whether they start collapsed. Reading and editing them in VS Code is planned.

## Related topics

- [Changing the document order](../03-editing/reorder.md)
- [Documentation roots and file conventions](structure.md)
