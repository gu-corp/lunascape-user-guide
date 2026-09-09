# Installing the extension

The VS Code extension "Lunascape Docs" is published on the Visual Studio Marketplace.

## Requirements

- VS Code 1.90 or later
- Features that write files — creating documents, organizing the INDEX, saving check settings, translating — work only in a workspace you have marked as trusted in VS Code.

## Install

1. Open the Extensions view (`⇧⌘X` / `Ctrl+Shift+X`) and search for "Lunascape Docs".
   You can also open the [Marketplace page](https://marketplace.visualstudio.com/items?itemName=lunascape.lunascape-doc) directly.
2. Click **Install**.

## Update

Once installed from the Marketplace, new versions update automatically. If you have turned off automatic updates in VS Code, update by hand from **Update** in the Extensions view.

## Check the version

Open "Lunascape Docs" in the Extensions view to see the installed version. You will need it when reporting a problem.

## Installing a `.vsix` directly

If you need to try a release ahead of its Marketplace delivery, or your network cannot reach the Marketplace, you can install a `.vsix` file from the GitHub releases page instead.

1. Open the [releases page](https://github.com/gu-corp/lunascape-docs/releases) and download the `.vsix` file for the version you want.
   If you are signed in to GitHub, the link downloads directly.
2. Install it in one of the following ways.
   - **Drag and drop**: drop the `.vsix` file onto the Extensions view (`⇧⌘X` / `Ctrl+Shift+X`).
   - **Menu**: choose [Install from VSIX…] from the [⋯] menu at the top right of the Extensions view and pick the file.
   - **Command line**: run `code --install-extension <downloaded file>`.
3. If nothing changes after installing, run "Developer: Reload Window" from the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).

A version installed this way does not update itself. Installing from the Marketplace afterward switches it back to automatic updates.

> **Hint**
>
> With the [GitHub CLI](https://cli.github.com/) you can download and install in one go.
>
> ```sh
> gh release download -R gu-corp/lunascape-docs -p '*.vsix' -D /tmp \
>   && code --install-extension /tmp/lunascape-doc-*.vsix
> ```

## Related topics

- [Creating your first documents](first-documents.md)
- [Reporting a problem](../07-troubleshooting/report.md)
