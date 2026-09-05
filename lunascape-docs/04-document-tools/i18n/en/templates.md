# Creating a document from a template

In the [作成] (Create) tab of Document Tools you choose a template, preview the content, and then create a new document.

1. Press [文書ツール] (Document Tools) in the toolbar and open the [作成] (Create) tab.
2. Press [テンプレートから作成] (Create from template) and choose a template.
3. Fill in the input fields (title, summary and so on). Required fields are marked "必須" (Required).
4. Enter the destination as a path relative to the documentation root (for example `03-design/api.md`).
5. Press [プレビュー] (Preview) and review the generated Markdown.
6. Press [この内容で作成] (Create with this content).
   The document is created and shown in the viewer, and the whole documentation root is checked again.

## Available templates

| Template | Content |
|---|---|
| 1ページ文書 (Single-page document) | A short specification, notes or a standalone explanation in one file |
| 仕様書・マニュアル・ヘルプ (Specification, manual, help) | One file with a general section structure suitable for a specification, manual or help |
| Standard Pack templates | When a Standard Pack is selected in `lunascape-docs.json`, the document types allowed by its profile (requirements, design and so on) are added |

> **Note**
>
> - Creation requires a trusted workspace.
> - Existing files are never overwritten. Creation fails if a document with the same name exists at the destination.
> - The destination needs a `.md` or `.mdx` extension. Nothing can be created under `i18n` (where translations live).
> - After changing the input, press [プレビュー] (Preview) again before creating.

> **Hint**
>
> In a project without a documentation folder, create the first set with "Lunascape Docs: テンプレートからドキュメントを作成" (Create documentation from template) in the Command Palette. See [Creating your first documents](../01-introduction/first-documents.md).

## Related topics

- [Using Document Tools](README.md)
- [Changing check rules](rules.md)
