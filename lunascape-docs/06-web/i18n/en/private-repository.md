# Reading a private repository

After signing in with GitHub, you can read the documents of private repositories, limited to those you have read access to. Lunascape Docs never has accounts or permissions of its own.

## Sign in and open

1. Open <https://docs.gu-group.com/>.
   When you name a private document or are not signed in yet, the sign-in screen appears.
2. Press [GitHub でログイン] (Sign in with GitHub).
   The GitHub authorization screen opens in a pop-up.
3. After signing in, press the GitHub button in the toolbar and choose the repository under [読めるリポジトリから選ぶ] (Choose from readable repositories).

> **Hint**
>
> - The signed-in account is shown in the toolbar, where you can also [ログアウト] (Sign out) or [別のアカウントでログイン] (Sign in with another account).
> - The list shows the repositories of the accounts (organizations or users) where the GitHub App "Lunascape Docs" is installed, limited to those you can read.

## Setup by the repository owner

If the repository does not appear in the list, the repository owner or an organization administrator must install the GitHub App "Lunascape Docs".

- The only permission requested is Contents: Read.
- The app is installed per account (organization or user). Choose "All repositories" (which includes repositories created later) or only selected repositories.

| Situation | Steps |
|---|---|
| Installing on a new organization or user account | Use the [installation page](https://github.com/apps/lunascape-docs/installations/new) |
| Adding repositories in an organization that already has it | Organization Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Even when the app is installed for a whole organization, each member sees only the repositories they can read.

## Related topics

- [Opening a GitHub repository](open-repository.md)
- [The Web viewer cannot open or sign in](../07-troubleshooting/web.md)
