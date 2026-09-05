# What Lunascape Docs is

Lunascape Docs turns the Markdown documents in a Git repository into a "specification site" as they are. No build step, documentation server or dedicated database is needed.

## What you can do

| Goal | Main features |
|---|---|
| Read | INDEX (table of contents), in-text links, breadcrumbs, Back/Forward, page outline, filter search |
| View | Tables, code blocks, auto-fitted images, KaTeX math, Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob diagrams, collapsed document-control tables |
| Write | Switch between visual editing and Markdown source; create, duplicate, rename and reorder from the INDEX |
| Check | docs-lint checks, required documents/sections/terms from a Standard Pack, creation from templates |
| Translate | Generate translation proposals per page or in batch, then review before saving |
| Use from AI | A read-only specification tool that VS Code agents can consult |

## Where you can use it

| Surface | Purpose |
|---|---|
| VS Code extension | Read, edit, check and translate the repository on your machine. This help focuses on it |
| Web viewer | Read documents on GitHub (public or private), keep drafts on your device, open a local folder |
| Chromium extension | Opens the Web viewer in a browser tab |
| Lunascape browser | Will embed the same document model |

## Basic principles

- **Markdown is the source of truth.** Documents stay as the Markdown files managed by Git. Lunascape Docs never keeps a converted copy in another format.
- **You decide when to save.** Edits are written to the file only when you press [保存] (Save). Git staging and committing are never automatic.
- **Documents are processed on your device.** Nothing is sent anywhere to read or edit a document. Only translation sends a document, and only after showing you the destination and content and receiving your approval.
- **Translations live under `i18n/<locale>/`.** Default-language documents stay in place; translations use the same relative path under `i18n/en/` and so on.
- **AI only proposes.** Translation proposals are saved after you review the diff. Documents are never rewritten silently.

## Related topics

- [Parts of the screen](screen.md)
- [Installing the extension](install.md)
- [Basic operations](../02-reading/README.md)
