# Documentation roots and file conventions

The rules Lunascape Docs follows to find documents and build the INDEX. The file system itself is the source of truth, so no ledger or build configuration is needed.

## Documentation root

- The nearest `docs` folder, or a folder containing `lunascape-docs.json`, becomes the documentation root.
- With a `lunascape-docs.json`, the folder does not have to be named `docs`.
- Opening a Markdown file outside any documentation root shows its folder as a temporary documentation root.

## Files shown in the INDEX

- `.md`, `.markdown` and `.mdx` files are shown. New files always appear, even without front matter or navigation metadata.
- Folders starting with `.`, `node_modules`, and the folders listed in `ignoredDirectories` (default `99-archive`) are not shown.
- Everything under `i18n/` is treated as translations and is not listed separately in the INDEX.

## Folder landing pages

- A `README.md` (or `index.md` when there is no README) with body content is the landing page of its folder. Pressing the folder name in the INDEX opens it.
- A `README.md` that consists only of front matter, with no body, is a "configuration-only descriptor" and is not shown as a page. Use it when a folder only needs a title or order.
- When both `README.md` and `index.md` exist, `README.md` takes precedence.

## Default language and translations

- Default-language (canonical) documents stay in place.
- A translation goes into an `i18n/<locale>/` folder beside the document, under the same file name. Rebuilding the folder structure under `i18n/` is not recognized.
- That is the only location a translation is resolved from. The same file placed anywhere else is an orphan that no document claims as its translation.

```text
docs/
  lunascape-docs.json
  README.md                  ← landing page of the root (start page)
  i18n/en/README.md          ← its English translation
  01-product/
    README.md                ← landing page of the folder
    requirements.md
    i18n/en/README.md        ← the English translations of the two above
    i18n/en/requirements.md
  99-archive/                ← excluded from the INDEX by default
```

## About `_meta.json`

Nextra's `_meta.json` is not used for navigation. Existing files are neither modified nor deleted. A future explicit import/export feature will be the only thing that handles them.

## Related topics

- [Setting navigation metadata](navigation-metadata.md)
- [Project configuration](project-configuration.md)
- [Switching documentation roots](../02-reading/roots.md)
