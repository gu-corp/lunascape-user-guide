# Basic operations

The basic operations from opening the documents to reaching the page you want to read.

## Open the documents

1. Open the repository in VS Code.
2. Run "Lunascape Docs: 仕様書ビューアーを開く" (Open Specification Viewer) from the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).
   The nearest documentation root (the `docs` folder by default) is found and its start page is shown.

> **Hint**
>
> - Right-click a Markdown file in the Explorer and choose [Lunascape Docs: 仕様書ビューアーで開く] (Open in Specification Viewer) to start from that file.
> - Opening a Markdown file that belongs to no documentation root shows its folder as a temporary documentation root.

## Move between pages

| Action | How |
|---|---|
| Open from the table of contents | Press a document name in the INDEX on the left |
| Follow a link | Press a link in the text. It opens in the same view |
| Go through the history | [戻る] (Back) and [進む] (Forward) in the toolbar, or `Alt`+`←` / `Alt`+`→` |
| Return to the start page | [仕様書トップ] (Home) in the toolbar |
| Go up one level | [親INDEX] (Parent INDEX) in the toolbar, or an item in the breadcrumbs |
| Move within the page | Press a heading in "このページ" (This page) on the right |

## Find a document

Type a word into [文書を絞り込み] (Filter documents) above the INDEX to show only the documents whose names match. Clear the field to show everything again.

## Refresh the content

When you save a Markdown file in the VS Code editor, the view updates automatically. After changing files with an external tool, press [再読み込み] (Reload) in the toolbar.

> **Note**
>
> - External links (`https://` and so on) open in your default browser. Links to files outside the documentation root do not open.
> - Documents are processed on your device. Nothing is sent anywhere in order to read a document.

## Related topics

- [Using the INDEX](index-panel.md)
- [Switching documentation roots](roots.md)
- [Editing a document](../03-editing/README.md)
