# Command list

Type "Lunascape Docs" into the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`) to run the following commands.

| Command | Function |
|---|---|
| Lunascape Docs: 仕様書ビューアーを開く (Open Specification Viewer) | Opens the nearest documentation root in the viewer. Reading, editing, checking and translating all happen in this view |
| Lunascape Docs: 仕様書ビューアーで開く (Open in Specification Viewer) | Shows the Markdown file that is open in the editor in the viewer |
| Lunascape Docs: テンプレートからドキュメントを作成 (Create documentation from template) | Creates an initial set of documents in a project without a documentation folder |
| Lunascape Docs: 文書ルートを検証 (Validate documentation root) | Checks the whole documentation root with docs-lint and shows the results in Document Tools and the Problems panel |
| Lunascape Docs: 翻訳に使うツールを選択… (Select the translation tool) | Reopens the picker for the tool that drafts translations (a VS Code language model, or the Claude CLI) |
| Lunascape Docs: ヘルプを開く (Open Help) | Opens this help guide |

## From the Explorer

Right-click a `.md`, `.markdown` or `.mdx` file in the Explorer and choose [Lunascape Docs: 仕様書ビューアーで開く] (Open in Specification Viewer).

> **Hint**
>
> To show Markdown files in Lunascape Docs whenever you open them normally, add an editor association to the workspace settings.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## Walkthrough

The walkthrough "Lunascape Docsを始める" (Get started with Lunascape Docs), found under the [Help] menu → "Welcome" in VS Code, lets you try creating documents, opening the viewer, the help and the AI tool in order.

## Related topics

- [Basic operations](../02-reading/README.md)
- [Keyboard shortcuts](../08-reference/keyboard.md)
