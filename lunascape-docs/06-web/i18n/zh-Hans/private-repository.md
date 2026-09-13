# 阅读非公开仓库

使用 GitHub 登录后，你可以阅读非公开仓库中的文档，但仅限于你拥有读取权限的仓库。Lunascape Docs 从不拥有自己的账号或权限。

## 登录并打开

1. 打开 <https://docs.lunascape.org/>。
   当你指定了非公开文档，或尚未登录时，会显示登录界面。
2. 按 [使用 GitHub 登录]。
   GitHub 的认证界面会在弹出窗口中打开。
3. 登录完成后，按工具栏中的 [打开文档]，然后在 [从可读取的仓库中选择] 里选择要打开的仓库。

> **提示**
>
> - 当前登录的账号名会显示在工具栏中。你也可以从这里执行 [退出登录] 或 [使用其他账号登录]。
> - 列表中显示的，是已安装 GitHub App“Lunascape Docs”的账号（组织或个人）所属仓库中，你拥有读取权限的那些仓库。

## 仓库所有者需进行的设置

如果列表中没有显示目标仓库，则需要由仓库所有者或组织管理员安装 GitHub App“Lunascape Docs”。

- 请求的权限为 Contents（读写）和 Pull requests（读写）。读取用于阅读，写入用于从 Web 发送发布申请（Pull Request）。Lunascape Docs 从不保存文档的内容。
- 安装以账号（组织或个人）为单位。可设置将对象设为“All repositories”（此后创建的仓库也会自动包含），或仅限所选的仓库。

| 场景 | 步骤 |
|---|---|
| 在新的组织或个人账号中引入 | 从[安装页面](https://github.com/apps/lunascape-docs/installations/new)进行 |
| 在已引入的组织中添加目标仓库 | 在组织的 Settings → GitHub Apps → Lunascape Docs → Configure → Repository access 中设置 |

即使为整个组织安装，各成员也只能阅读本人拥有读取权限的仓库。能发送发布申请的，也仅限本人拥有写入权限的仓库。

> **提示**
> - 新安装时，请求的权限会在安装界面上以列表形式显示，按下“Install”即表示已批准。无需其他操作。
> - 对于在权限增加之前就已安装的组织，管理员会收到确认邮件，并在组织的 Settings → GitHub Apps → Lunascape Docs → Configure 顶部显示批准按钮。在批准之前，该组织只能阅读，发送发布申请时会显示“需要授予写入权限”。
> - 当前以何种权限接入，可在同一 Configure 界面中查看。个人账号则为 Settings → Applications → Installed GitHub Apps。
> - 如果误将目标仓库移除或卸载了应用，从[安装页面](https://github.com/apps/lunascape-docs/installations/new)重新安装即可恢复。发布申请的拒绝消息中会附带指向修复界面的链接。
> - 如果仓库一方不想接受发布申请，可在 `lunascape-docs.json` 中写入 `"publish": { "enabled": false }`。阅读不受影响，仍可照常使用。

## 相关主题

- [打开 GitHub 仓库](open-repository.md)
- [Web 版无法打开或无法登录](../07-troubleshooting/web.md)
