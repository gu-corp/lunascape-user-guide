# What the Web viewer does

The Web viewer of Lunascape Docs is available at <https://docs.gu-group.com/>. Without installing anything, you can read documents on GitHub as if they were a website.

## Features

| Feature | Description |
|---|---|
| Public repositories | Opens the documents of a public GitHub repository without signing in |
| Private repositories | After signing in with GitHub, opens the repositories you have read access to |
| Local folders | [ローカルフォルダの文書を開く] (Open documents in a local folder) opens a folder on your device (supported browsers only) |
| Reading | INDEX, links, history, filtering, page outline, language switching and theme switching, the same as in VS Code |
| Diagrams and math | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose and KaTeX math |
| Drafts | Edit documents and keep the changes as drafts on your device. Nothing is written to the repository |
| Deep links | A URL can name the repository and the page, so a specific page can be opened directly |

## Differences from the VS Code extension

- Document checks, creation from templates, translation proposals and organizing from the INDEX are not available in the Web viewer.
- TikZ figures are not rendered.
- Edits are not written to the repository; they become drafts on your device. "Publish request", which sends drafts as a pull request, is implemented but not enabled on the public viewer. To change the repository, edit with the VS Code extension or in a local clone.

## Related topics

- [Opening a GitHub repository](open-repository.md)
- [Reading a private repository](private-repository.md)
- [Keeping drafts](drafts.md)
