# Install the extension

The VS Code extension "Lunascape Docs" is distributed internally. It is not on the Marketplace, so you install it from a `.vsix` file taken from the release page.

## Requirements

- VS Code 1.90 or later
- Features that write — creating documents, organizing from the INDEX, saving check settings, translating — work only in a workspace you have marked as trusted in VS Code.

## Install

1. Open the [release page](https://github.com/gu-corp/lunascape-docs/releases) and download the latest `.vsix` file.
   If you are signed in to GitHub, the link downloads it directly.
2. Install it in one of these ways.
   - **Drag and drop**: drop the `.vsix` file onto the Extensions view in VS Code (`⇧⌘X` / `Ctrl+Shift+X`).
   - **Menu**: from [⋯] at the top right of the Extensions view, choose [Install from VSIX…] and pick the file.
   - **Command line**: run `code --install-extension <the downloaded file>`.
3. If nothing changes after installing, run "Developer: Reload Window" from the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).

> **Tip**
>
> With the [GitHub CLI](https://cli.github.com/) the download and the install are one command.
>
> ```sh
> gh release download -R gu-corp/lunascape-docs -p '*.vsix' -D /tmp \
>   && code --install-extension /tmp/lunascape-doc-*.vsix
> ```

## Update

The extension does not update itself. When a new version is published, install it again the same way. It installs over the old one, so there is no need to uninstall first.

## Check the version

Open "Lunascape Docs" in the Extensions view to see the installed version. You will need it when reporting a problem.

## Related topics

- [Create your first documents](first-documents.md)
- [Report a problem](../07-troubleshooting/report.md)
