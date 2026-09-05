# The Web viewer cannot open or sign in

## Signed in, but the repository is not in the list

The GitHub App "Lunascape Docs" is not installed on that account, or the repository is not included. Ask the repository owner or an organization administrator to install it as described in [Reading a private repository](../06-web/private-repository.md).

## Cannot get past the sign-in screen

- You do not have read access to the repository. Ask the repository owner to grant access.
- "このサイトには GitHub ログインが設定されていません" (GitHub sign-in is not configured for this site): a self-hosted viewer has no sign-in service configured. An administrator needs to set one up.

## The sign-in pop-up does not open

The browser blocked the pop-up. Allow pop-ups for this site and try again.

## "ログインが切れています" (Your sign-in has expired) is shown

The sign-in has expired. Press [GitHub でログイン] (Sign in with GitHub) again.

## A public repository returns 404

- Check the `owner/repo@ref/dir` form.
- Branch names containing `/` cannot be specified.

## Loading stops working after a while

Without signing in, the GitHub API rate limit (60 requests per hour) applies. When "回数制限に達しました" (Rate limit reached) is shown, wait a while or sign in with [GitHub でログイン] (Sign in with GitHub).

## "このサイトからは、このリポジトリを表示できません" (This site cannot show this repository) is shown

To open a repository from a self-hosted viewer, the site's URL must be added to `viewer.origins` in the repository's `lunascape-docs.json`.

## Opening `index.html` shows nothing

It does not work when opened directly via `file://`. Serve it over HTTP, or use the VS Code extension.

## An exported site says "lunascape-docs-manifest.json が見つかりません" (manifest not found)

Deploy the complete output of `npm run export:web`, including the manifest, as is.

## Drafts cannot be saved

- "IndexedDB を開けません" (Cannot open IndexedDB) / "他のタブで使用中です" (In use by another tab): caused by the browser's private mode or by another tab showing the same site. Use a normal window and close the other tabs.
- Drafts are stored per device and browser. They do not carry over to another device.

## Related topics

- [Opening a GitHub repository](../06-web/open-repository.md)
- [Keeping drafts](../06-web/drafts.md)
