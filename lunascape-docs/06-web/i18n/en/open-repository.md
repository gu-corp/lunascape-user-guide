# Opening a GitHub repository

In the Web viewer you open documents by naming a GitHub repository. Public repositories need no sign-in.

## Open from the screen

1. Open <https://docs.gu-group.com/>.
2. Press the GitHub button in the toolbar ([GitHubのドキュメントを開く] (Open documents on GitHub)).
3. Enter the repository under [リポジトリを直接指定] (Specify a repository) and press [開く] (Open).
   When you are signed in to GitHub, you can also pick from a list under [読めるリポジトリから選ぶ] (Choose from readable repositories).

## Open by URL

The `source` URL parameter names the repository and the documentation root. Share the address and others open the same documents.

```text
https://docs.gu-group.com/?source=github:owner/repo@main/docs
```

| What to specify | Form |
|---|---|
| Repository only (root of the default branch) | `github:owner/repo` |
| A branch or tag | `github:owner/repo@main` |
| The documentation root folder | `github:owner/repo@main/docs` |
| A GitHub URL as is | `https://github.com/owner/repo/tree/main/docs` |

To open a specific page directly, append `#/` and the path relative to the documentation root.

```text
https://docs.gu-group.com/?source=github:owner/repo@main/docs#/01-product/vision.md
```

The part after `#/` updates as you navigate, so you can copy a link from the address bar at any time. The browser's Back and Forward buttons work too.

> **Note**
>
> - Without signing in, the GitHub API rate limit (60 requests per hour) applies. For repositories with many documents or repeated reading, sign in with [GitHub でログイン] (Sign in with GitHub).
> - Branch names containing `/` (such as `feature/xxx`) cannot be specified.
> - Documents are loaded with the reader's own GitHub permissions. People without read access do not see them.

## Open documents in a local folder

Press [ローカルフォルダの文書を開く] (Open documents in a local folder) in the toolbar and choose a folder on your device. Files are processed inside the browser and never sent anywhere. This works in browsers that support folder selection (Chrome, Edge and others).

## Related topics

- [Reading a private repository](private-repository.md)
- [The Web viewer cannot open or sign in](../07-troubleshooting/web.md)
