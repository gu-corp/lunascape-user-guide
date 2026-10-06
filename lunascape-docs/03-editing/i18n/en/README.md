# Editing a document

Documents can be edited right inside the viewer. The editor has a visual view, where you edit what you see, and a Markdown source view; one button switches between them.

## Start editing

Press any of the following. They all open the same editor.

- [編集] (Edit) at the bottom right of the document
- [⋯] (More actions) at the top right of the document → [編集] (Edit)
- The INDEX item menu → [編集] (Edit)

## Edit

1. Edit the text directly.
   The toolbar at the top of the editor offers the paragraph format (body, headings 1–4, quote, code), [太字] (Bold), [斜体] (Italic), [箇条書き] (Bulleted list), [番号付きリスト] (Numbered list), [リンク] (Link), [表を挿入] (Insert table), [画像サイズ] (Image size), [元に戻す] (Undo) and [やり直す] (Redo).
2. To edit the Markdown source directly, press [Markdown].
   Press it again to return to the visual view. The view you used last is remembered and restored the next time you press [編集] (Edit).
3. Press [保存] (Save), or Ctrl+S / ⌘S.
   The Markdown file is written and the viewer returns to reading mode. To stop editing and go back to what was last saved, press [編集取り消し] (Discard edits).

## Always start in the editor (edit mode)

Press [編集モード] (Edit mode) on the toolbar to turn it on: from then on every document opens in the editor, the way a notepad does. Use it when you are writing rather than reading.

- While it is on, [保存] (Save) does not close the editor. [編集取り消し] (Discard edits) returns to what was last saved and keeps the editor open.
- Press it again to turn it off and return to reading mode. The choice is remembered per user.
- It is not shown on a documentation root that cannot be written to, such as a read-only GitHub source.

## Unsaved edits

Edits you have not saved are kept on this device automatically. Moving to another document, or closing the tab or window, does not lose them.

- [未保存] (Unsaved) in the editor means the text differs from what was last saved.
- The next time you open the same document, it resumes from the kept edits and says so. If the document itself has changed since, it says that too; [編集取り消し] (Discard edits) returns to the latest version.
- The kept edits go away with [保存] (Save) or [編集取り消し] (Discard edits). Nothing has been saved, so they do not appear in Git or among drafts.

> **Note**
>
> - Saving only writes the file. Git staging and committing are never automatic.
> - Math and diagrams such as Mermaid, TikZ and Vega-Lite are shown rendered in the visual view. Switch to [Markdown] to change their content.
> - Documents containing MDX-specific syntax (components, `import` and so on) are edited in the Markdown view only, to protect that syntax.
> - Front matter (the block between `---` lines at the top) is preserved when you edit in the visual view.

> **Hint**
>
> - [VS Codeで開く] (Open in VS Code) opens the file in the normal text editor. Saving there updates the viewer automatically.
> - To hide the [編集] (Edit) button, turn off [編集ボタン] (Edit button) in [表示設定] (Display settings). To hide it for the whole project, set `editor.showEditButton` to `false` in `lunascape-docs.json`.
> - The default initial view (visual or Markdown) is set by `lunascapeDocEditor.editor.defaultMode` or by `editor.defaultMode` in `lunascape-docs.json`.

## Related topics

- [Creating and organizing documents and folders](organize.md)
- [Sizing images](images.md)
- [Writing math](math.md)
- [Writing diagrams and charts](diagrams.md)
