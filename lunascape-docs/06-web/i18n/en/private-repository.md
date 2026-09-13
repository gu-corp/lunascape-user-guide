# Reading a private repository

After signing in with GitHub, you can read the documents of private repositories, limited to those you have read access to. Lunascape Docs never has accounts or permissions of its own.

## Sign in and open

1. Open <https://docs.lunascape.org/>.
   When you name a private document or are not signed in yet, the sign-in screen appears.
2. Press [GitHub でログイン] (Sign in with GitHub).
   The GitHub authorization screen opens in a pop-up.
3. After signing in, press [文書を開く] (Open documents) in the toolbar and choose the repository under [読めるリポジトリから選ぶ] (Choose from readable repositories).

> **Hint**
>
> - The signed-in account is shown in the toolbar, where you can also [ログアウト] (Sign out) or [別のアカウントでログイン] (Sign in with another account).
> - The list shows the repositories of the accounts (organizations or users) where the GitHub App "Lunascape Docs" is installed, limited to those you can read.

## Setup by the repository owner

If the repository does not appear in the list, the repository owner or an organization administrator must install the GitHub App "Lunascape Docs".

- The permissions requested are Contents (read and write) and Pull requests (read and write). Reading is for viewing; writing is for sending a pull request from the web. Lunascape Docs never stores the documents.
- The app is installed per account (organization or user). Choose "All repositories" (which includes repositories created later) or only selected repositories.

| Situation | Steps |
|---|---|
| Installing on a new organization or user account | Use the [installation page](https://github.com/apps/lunascape-docs/installations/new) |
| Adding repositories in an organization that already has it | Organization Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Even when the app is installed for a whole organization, each member sees only the repositories they can read, and can send a pull request only to repositories they can write to.

> **Tips**
> - On a new installation the requested permissions are listed on the install screen, and pressing "Install" approves them. Nothing else is needed.
> - An organization that installed the app before a permission was added gets an email to its administrators and an approval button at the top of Organization Settings → GitHub Apps → Lunascape Docs → Configure. Until it approves, that organization can read but a pull request answers that write permission is needed.
> - The same Configure page shows which permissions are in effect. For a personal account it is Settings → Applications → Installed GitHub Apps.
> - If repository access was narrowed by mistake or the app uninstalled, installing again from the [installation page](https://github.com/apps/lunascape-docs/installations/new) puts it back. A refused pull request links to the page where it is fixed.
> - A repository that should not take pull requests from the viewer writes `"publish": { "enabled": false }` in `lunascape-docs.json`. Reading is unaffected.

## Related topics

- [Opening a GitHub repository](open-repository.md)
- [The Web viewer cannot open or sign in](../07-troubleshooting/web.md)
