# Cannot edit, save or reorder

## There is no [編集] (Edit) button

- [編集ボタン] (Edit button) in [表示設定] (Display settings) is off. Turn it on, or use [⋯] → [編集] (Edit) at the top right of the document, or [編集] (Edit) in the INDEX item menu.
- The same applies when `editor.showEditButton` in `lunascape-docs.json` is `false`.
- Editing is unavailable while the help is shown. Close the help.

## Cannot switch to the visual view

"この文書にはMDX構文があるため通常の編集画面へ切り替えられません" (This document contains MDX syntax and cannot be opened in the visual editor): documents with MDX-specific syntax (components, `import` and so on) are edited in the Markdown view only, to protect that syntax.

## Cannot edit math or a diagram directly

The visual view shows rendered output. Press [Markdown] in the editor and edit the source.

## Cannot reorder or drag

- Reordering is unavailable while filtering, while editing a document, and while another INDEX operation is in progress.
- In an untrusted workspace, the create, organize and delete actions are unavailable. Trust the workspace in VS Code.
- "INDEXが更新されています。もう一度ドラッグしてください" (The INDEX has been updated; drag again): another change was just applied. Repeat the operation.
- The start page (the root `README.md`) cannot be moved.

## "未保存の変更があります" (There are unsaved changes) is shown

The target file is being edited in the VS Code editor. Save or discard the changes first, then try again.

## Cannot rename

The following names cannot be used.

- Names starting with `.`, `i18n`, and Windows reserved names (`CON` and so on)
- Names ending with a period or a space, and names containing control characters or characters not allowed in file names
- Names that already exist in the same folder (including names that differ only in letter case)
- Document names without a Markdown extension

## Saved changes do not show up in Git or are not committed

Lunascape Docs only writes the file. It never stages or commits in Git. Check the Source Control view in VS Code and commit as needed.

## Related topics

- [Editing a document](../03-editing/README.md)
- [Creating and organizing documents and folders](../03-editing/organize.md)
- [Changing the document order](../03-editing/reorder.md)
