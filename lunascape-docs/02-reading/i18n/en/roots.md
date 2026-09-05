# Switching documentation roots

A documentation root is the top folder of one set of documents. The INDEX, filtering, checks and translation all work per documentation root.

## How a documentation root is found

Lunascape Docs walks up from the opened Markdown file and uses the nearest folder that matches one of the following as the documentation root.

- A folder containing `lunascape-docs.json` (any folder name)
- A folder named `docs` (add more names with the `lunascapeDocEditor.rootDirectoryNames` setting)

When you run "Lunascape Docs: 仕様書ビューアーを開く" (Open Specification Viewer), the documentation root from the `lunascapeDocEditor.root` setting (default `docs`) opens.

## Switch to another documentation root

When the workspace has several documentation roots, the root name at the far left of the toolbar becomes a drop-down.

1. Press the documentation root name at the far left of the toolbar.
2. Choose a documentation root from the list.
   Its start page is shown and the INDEX switches.

> **Hint**
>
> The names in the list are resolved in this order. They do not change when you switch the display language.
>
> 1. `title` in `lunascape-docs.json`
> 2. `navigation.title` of the root `README.md`, otherwise its H1
> 3. `navigation.title` of the root `index.md`, otherwise its H1
> 4. The folder name (for a standard `docs` folder, the name of its parent folder)

## Open a Markdown file outside any documentation root

Opening a Markdown file that is not inside a documentation root shows its folder as a temporary documentation root. The INDEX lists the Markdown files in that folder and below.

- Press [上のフォルダへ] (Up one folder) in the toolbar to widen the scope to the parent folder inside the workspace.
- Project language settings and batch translation are unavailable in this view. Put a `lunascape-docs.json` in the folder to make it a documentation root and enable them.

## Always open a fixed documentation root

Set `lunascapeDocEditor.rootMode` to `fixed` to always open the documentation root in `lunascapeDocEditor.root`, whichever Markdown file you open.

## Related topics

- [Documentation roots and file conventions](../04-document-tools/structure.md)
- [Project configuration](../04-document-tools/project-configuration.md)
- [VS Code settings](../08-reference/settings.md)
