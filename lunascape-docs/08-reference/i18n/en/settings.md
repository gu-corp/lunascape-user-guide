# VS Code settings

Search for "Lunascape Docs" in the VS Code settings (`⌘,` / `Ctrl+,`) to change the following. All of them are personal settings and are never saved into project documents.

## Documentation root

| Setting | Values | Default | Function |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` picks the documentation root nearest to the opened Markdown file and opens its parent folder temporarily when it belongs to none. `fixed` always opens the root in `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Array of strings | `["docs"]` | Folder names discovered as documentation roots in `auto` mode. A folder with `lunascape-docs.json` is discovered regardless of its name. A `defaultFolder` or `roots` in the `lunascape-docs.json` at the top of the repository takes precedence |
| `lunascapeDocEditor.root` | Path | `docs` | The workspace-relative documentation root for `fixed` mode and for the open command |
| `lunascapeDocEditor.startPage` | Path | `README.md` | The start page relative to the documentation root |
| `lunascapeDocEditor.title` | String | `Lunascape Docs` | Overrides the document tab title. It does not affect the documentation-root selector |
| `lunascapeDocEditor.ignoredDirectories` | Array of strings | `["99-archive"]` | Folder names excluded from the INDEX |

## Display

| Setting | Values | Default | Function |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` uses a white background; `auto` follows the VS Code theme |
| `lunascapeDocEditor.locale` | Language tag | None | Your preferred document language, used when available. It never changes the project's canonical language |
| `lunascapeDocEditor.documentMetadata.compact` | Boolean | `true` | Collapses the document-control table after the H1 into a "Document information" row |
| `lunascapeDocEditor.tree.showFileNames` | Boolean | `false` | Shows file names instead of document titles in the INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolean | `false` | Shows document icons in the INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolean | `false` | Shows folder icons in the INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolean | `false` | Shows the number of direct children of each folder |
| `lunascapeDocEditor.tree.showGuides` | Boolean | `true` | Shows guide lines for nesting |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Row spacing of the INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolean | `true` | Closes the INDEX once when there is only one document |

## Editing

| Setting | Values | Default | Function |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | The editing view used until you switch. The view used last takes precedence |
| `lunascapeDocEditor.editor.showEditButton` | Boolean | `true` | Shows [編集] (Edit) at the bottom right of the document |

## Diagrams

| Setting | Values | Default | Function |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | The TikZ rendering runtime. `bundled` uses an approved bundled runtime (not included in the current distributed build), `workspace` uses `node-tikzjax` 1.0.5 at the root of a trusted workspace (development and evaluation only), `disabled` renders nothing |

## Translation

| Setting | Values | Default | Function |
|---|---|---|---|
| `lunascapeDocEditor.translation.provider` | `auto` / `vscode` / `claude` | `auto` | The provider used for translation |
| `lunascapeDocEditor.translation.model` | String | None | The name or ID of a VS Code language model. Not applied to the Claude CLI |

## Deprecated settings

| Setting | Use instead |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` in `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` in `lunascape-docs.json` |

Personal settings cannot override the project languages.

## Related topics

- [Changing display settings](../02-reading/display-settings.md)
- [Project configuration](../04-document-tools/project-configuration.md)
