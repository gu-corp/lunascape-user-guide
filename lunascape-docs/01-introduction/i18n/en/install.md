# Installing the extension

The VS Code extension "Lunascape Docs" is distributed internally. It is not on the Marketplace, so you install it from a `.vsix` file downloaded from the releases page.

## Requirements

- VS Code 1.90 or later
- Features that write files — creating documents, organizing the INDEX, saving check settings, translating — work only in a workspace you have marked as trusted in VS Code.

## Install

1. Open the [releases page](https://github.com/gu-corp/lunascape-docs/releases) and download the latest `.vsix` file.
   If you are signed in to GitHub, the link downloads directly.
2. Install it in one of the following ways.
   - **Drag and drop**: drop the `.vsix` file onto the Extensions view (`⇧⌘X` / `Ctrl+Shift+X`).
   - **Menu**: choose [Install from VSIX…] from the [⋯] menu at the top right of the Extensions view and pick the file.
   - **Command line**: run `code --install-extension <downloaded file>`.
3. If nothing changes after installing, run "Developer: Reload Window" from the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).

> **Hint**
>
> With the [GitHub CLI](https://cli.github.com/) you can download and install in one go.
>
> ```sh
> gh release download -R gu-corp/lunascape-docs -p '*.vsix' -D /tmp \
>   && code --install-extension /tmp/lunascape-doc-*.vsix
> ```

## Update

The extension does not update itself. When a new version is released, install it again with the same steps. It installs over the existing version, so you do not need to uninstall first.

## Check the version

Open "Lunascape Docs" in the Extensions view to see the installed version. You will need it when reporting a problem.

## Related topics

- [Creating your first documents](first-documents.md)
- [Reporting a problem](../07-troubleshooting/report.md)
