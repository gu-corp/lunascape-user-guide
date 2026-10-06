# Opening a GitHub repository

In the Web viewer you can open a GitHub repository and read it as it is, without cloning it. Public repositories need no sign-in.

## Open from the screen

1. Press [文書を開く] (Open documents), the folder icon in the toolbar. The Open documents screen appears.
2. Choose where to look in the list on the left.

   | Place | What it lists |
   |---|---|
   | [すべて] (All) | Everything below, with what you opened recently first |
   | [最近開いた] (Recently opened) | The repositories and folders you have opened |
   | [おすすめ] (Featured) | The manuals the site features |
   | [GitHub のリポジトリ] (GitHub repositories) | When you are signed in to GitHub, the repositories you can read |
   | [このパソコン] (This computer) | Folders on this device |

3. Press [開く] (Open) on the row you want. Type in [文書名・リポジトリ名で絞り込み] (Filter by document or repository) at the top to narrow the rows.

For a repository that is not listed, use [owner/repo を入力して開く] (Open owner/repo) on the left.

> **Tip**
>
> - The GitHub repositories listed are those the GitHub App "Lunascape Docs" is installed on and that you can read. If one is missing, ask its owner to add the App.

## Check where a document is

The small icon near the left of the toolbar (the location chip) shows where the document you are reading is.

| Icon | Location |
|---|---|
| The GitHub mark | Read from GitHub. Nothing is stored on this device |
| A folder | A folder on this device |

Press the icon to see the location, its status, and what you can do from there, such as [GitHub で見る] (View on GitHub) and [リンクをコピー] (Copy link).

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

Press [文書を開く] (Open documents) in the toolbar, then [ローカルフォルダの文書を開く] (Open documents in a local folder) on the left, and choose a folder on your device. Files are processed inside the browser and never sent anywhere. This works in browsers that support folder selection (Chrome, Edge and others).

## Related topics

- [Reading a private repository](private-repository.md)
- [The Web viewer cannot open or sign in](../07-troubleshooting/web.md)
