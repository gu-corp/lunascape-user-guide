# 打开 GitHub 仓库

在 Web 版中，通过指定 GitHub 仓库来打开文档。公开仓库无需登录。

## 从界面打开

1. 打开 <https://docs.lunascape.org/>。
2. 按工具栏中的 [打开文档]（文件夹图标）。
3. 在 [直接指定仓库] 中输入仓库，然后按 [打开]。
   已登录 GitHub 时，也可以在 [从可读取的仓库中选择] 的列表中选取。

> **提示**
>
> - 旁边的 GitHub 图标会在 github.com 上打开你正在阅读的文档，它不是打开文档的操作。

## 通过 URL 打开

地址就是把仓库和文档的位置按原样排列而成。路径是文档在仓库中的位置，因此与 GitHub 的 URL 排列一致。

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| 指定内容 | 写法 |
|---|---|
| 仅仓库（默认分支） | `/github/owner/repo` |
| 仓库中的文档 | `/github/owner/repo/docs/01-product/vision.md` |
| 指定分支或标签 | 在末尾加上 `?ref=v1.2.0` |

翻页时地址也会随之改变。按工具栏中的 [分享此文档]，即可把当前阅读页面的链接交给他人。浏览器的 [返回] [前进] 也可以使用。

以往的 `?source=` 形式仍可照常打开，打开后会改写为新的形式。

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **注意**
>
> - 未登录时，会受到 GitHub API 的使用限制（每小时 60 次）。文档较多的仓库或反复浏览时，请 [使用 GitHub 登录]。
> - 含 `/` 的分支名（如 `feature/xxx`）可以用上述地址形式中的 `?ref=` 指定，`?source=` 形式无法书写。
> - 文档以阅读者的 GitHub 权限加载。没有读取权限的人不会看到。

## 打开本地文件夹中的文档

按工具栏中的 [打开文档]，再从列表下方的 [打开本地文件夹中的文档] 选择设备内的文件夹。文件在浏览器中处理，不会发送到外部。可在支持文件夹选择的浏览器（Chrome、Edge 等）中使用。

## 相关项目

- [浏览非公开仓库](private-repository.md)
- [Web 版无法打开或无法登录](../07-troubleshooting/web.md)
