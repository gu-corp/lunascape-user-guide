# Installing the extension

The VS Code extension "Lunascape Docs" is distributed as a VSIX file.

## Requirements

- VS Code 1.90 or later
- Features that write files — creating documents, organizing the INDEX, saving check settings, translating — work only in a workspace you have marked as trusted in VS Code.

## Install

1. Get the VSIX file. This link always points at the current version.

   [Download lunascape-doc.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-doc.vsix)

2. Open the Extensions view (`⇧⌘X` / `Ctrl+Shift+X`).
3. Choose **Install from VSIX…** from the `…` menu at the top right, and pick the file you downloaded.

## Update

When a newer version is published, the extension fetches and installs it. VS Code offers to reload the window, and that is when you start using it. Your settings and documents are left as they are.

It checks once a day. `lunascapeDocEditor.update.check` changes that.

| Setting | What happens |
|---|---|
| Install a newer version when one is published | The default |
| Tell me, and let me decide each time | A notice appears, and nothing changes until you press **Update** |
| Never check | Nothing happens |

## Check the version

Open "Lunascape Docs" in the Extensions view to see the installed version. You will need it when reporting a problem.

## Related topics

- [Creating your first documents](first-documents.md)
- [Reporting a problem](../07-troubleshooting/report.md)
