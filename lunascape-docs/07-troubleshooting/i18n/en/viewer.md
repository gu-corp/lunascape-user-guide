# Documents do not appear

## "開けるMarkdownまたはdocsフォルダが見つかりません" (No Markdown or docs folder to open) is shown

- The workspace has no `docs` folder, or uses a different name.
  - Put a `lunascape-docs.json` in the folder to make it a documentation root regardless of its name.
  - Or add the folder name to the `lunascapeDocEditor.rootDirectoryNames` setting.
- If there are no documents yet, create them with "Lunascape Docs: テンプレートからドキュメントを作成" (Create documentation from template).
- Alternatively, open a Markdown file in the editor and run "Lunascape Docs: 仕様書ビューアーで開く" (Open in Specification Viewer).

## A document is missing from the INDEX

- Check that the extension is `.md`, `.markdown` or `.mdx`.
- These folders are not shown: folders starting with `.`, `node_modules`, and folders listed in `ignoredDirectories` (default `99-archive`).
- Translations under `i18n/` are not listed separately. Switch to them from the language menu.
- If a file you just added is missing, press [再読み込み] (Reload).
- You may be looking at another documentation root. Check the root name at the far left of the toolbar.

## Pressing a folder shows nothing

The folder's `README.md` is a "configuration-only descriptor" with front matter but no body. Expand the folder in the INDEX and choose a document inside it.

## The wrong documentation root opens

- With `lunascapeDocEditor.rootMode` set to `fixed`, the root in `lunascapeDocEditor.root` always opens.
- With `auto`, the documentation root nearest to the opened Markdown file is chosen. Switch with the drop-down at the far left of the toolbar.

## The documentation root has an unexpected name

The name is resolved from `title` in `lunascape-docs.json` → `navigation.title` of the root `README.md` → its H1 → `index.md` → the folder name. Set `title` to fix it.

## The INDEX disappeared

- In a documentation root with only one document, the INDEX closes itself once. Reopen it with the column icon in the toolbar, and turn the behavior off with [文書が1件なら自動的に隠す] (Auto-hide for a single document) in [表示設定] (Display settings).
- On a narrow screen, open it with [INDEXを開く] (Open INDEX, three lines) to the left of [戻る] (Back).

## A link does not open

- "リンク先が見つかりません" (Link target not found): the target file does not exist. Check internal links with [チェック] (Check) in Document Tools.
- "安全でない、または未対応のリンクを開きませんでした" (An unsafe or unsupported link was not opened): links outside the documentation root, or with a scheme other than `https://` or `mailto:`, do not open.

## The wrong language is shown

- Check the language of the current page and how it was determined in the language menu.
- The display language you chose last is remembered. Choose the default language again in the language menu.
- If the personal `lunascapeDocEditor.locale` setting is set, that language's translation is preferred.

## Related topics

- [Switching documentation roots](../02-reading/roots.md)
- [Documentation roots and file conventions](../04-document-tools/structure.md)
