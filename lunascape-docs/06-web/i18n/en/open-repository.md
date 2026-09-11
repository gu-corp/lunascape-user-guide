# Opening a GitHub repository

In the Web viewer you open documents by naming a GitHub repository. Public repositories need no sign-in.

## Open from the screen

1. Open <https://docs.lunascape.org/>.
2. Press [文書を開く] (Open documents), the folder icon in the toolbar.
3. Enter the repository under [リポジトリを直接指定] (Specify a repository) and press [開く] (Open).
   When you are signed in to GitHub, you can also pick from a list under [読めるリポジトリから選ぶ] (Choose from readable repositories).

> **Tip**
>
> - The GitHub mark beside it opens the document you are reading on github.com. It does not open documents here.

## Open by URL

The address names the repository and the document in the order they appear in the repository, so it reads like the GitHub URL for the same file.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| What to specify | Form |
|---|---|
| Repository only (default branch) | `/github/owner/repo` |
| A document inside the repository | `/github/owner/repo/docs/01-product/vision.md` |
| A branch or tag | append `?ref=v1.2.0` |

The address changes as you navigate. Press [この文書を共有] (Share this document) in the toolbar to hand someone a link to the page you are reading. The browser's Back and Forward buttons work too.

The older `?source=` form still opens, and is rewritten to the new one once it has.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Note**
>
> - Without signing in, the GitHub API rate limit (60 requests per hour) applies. For repositories with many documents or repeated reading, sign in with [GitHub でログイン] (Sign in with GitHub).
> - Branch names containing `/` (such as `feature/xxx`) can be named with `?ref=` in the address form above. The `?source=` form cannot express them.
> - Documents are loaded with the reader's own GitHub permissions. People without read access do not see them.

## Open documents in a local folder

Press [文書を開く] (Open documents) in the toolbar, then [ローカルフォルダの文書を開く] (Open documents in a local folder) below the list, and choose a folder on your device. Files are processed inside the browser and never sent anywhere. This works in browsers that support folder selection (Chrome, Edge and others).

## Related topics

- [Reading a private repository](private-repository.md)
- [The Web viewer cannot open or sign in](../07-troubleshooting/web.md)
