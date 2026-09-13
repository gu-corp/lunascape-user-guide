# 文档不显示

## 显示“找不到可打开的 Markdown 或 docs 文件夹”

- 工作区中没有 `docs` 文件夹，或者使用了 `docs` 以外的名称。
  - 把 `lunascape-docs.json` 放入该文件夹后，无论名称如何，都会被识别为文档根目录。
  - 或者，在设置 `lunascapeDocEditor.rootDirectoryNames` 中添加该文件夹名。
- 如果还没有文档，请用“Lunascape Docs: 从模板创建文档”来创建。
- 也可以先在编辑器中打开 Markdown 文件，再执行“Lunascape Docs: 在规格书查看器中打开”。

## 文档没有出现在 INDEX 中

- 确认扩展名为 `.md`、`.markdown` 或 `.mdx`。
- 以下文件夹不会显示：以 `.` 开头的文件夹、`node_modules`、在 `ignoredDirectories` 中指定的文件夹（默认为 `99-archive`）。
- `i18n/` 下的翻译版不会单独显示在 INDEX 中。请从语言菜单切换。
- 刚添加的文件没有显示时，请按 [重新加载]。
- 也可能正在查看另一个文档根目录。请确认工具栏最左端的文档根目录名称。

## 按下文件夹后什么也不显示

该文件夹的 `README.md` 是只有 front matter、没有正文的“仅用于配置的描述文件”。请在 INDEX 中展开该文件夹，选择其中的文档。

## 打开了非预期的文档根目录

- 设置 `lunascapeDocEditor.rootMode` 为 `fixed` 时，始终打开 `lunascapeDocEditor.root`。
- 为 `auto` 时，会选择离所打开的 Markdown 文件最近的文档根目录。可用工具栏最左端的下拉菜单切换。

## 文档根目录的名称与预期不符

名称按以下顺序确定：`lunascape-docs.json` 的 `title` → 根 `README.md` 的 `navigation.title` → 其 H1 → `index.md` → 文件夹名。想要固定名称时，请设置 `title`。

## INDEX 消失了

- 在只有 1 个文档的文档根目录中，INDEX 仅在首次时自动关闭。可用工具栏的分栏显示图标打开。也可以在 [显示设置] 的 [只有一个文档时自动隐藏] 中关闭该行为。
- 屏幕较窄时，请从 [返回] 左侧的 [打开 INDEX]（三条横线）打开。

## 按下链接也打不开

- “找不到链接目标”：链接指向的文件不存在。可用文档工具的 [检查] 确认内部链接。
- “未打开不安全或不支持的链接”：指向文档根目录之外，或 `https://`、`mailto:` 以外协议的链接不会打开。

## 显示的语言与预期不符

- 在语言菜单中确认当前页面的语言及其依据。
- 上次选择的界面语言会被记住。请在语言菜单中重新选择默认语言。
- 如果设置了个人设置 `lunascapeDocEditor.locale`，则优先显示该语言的翻译版。

## 相关项目

- [切换文档根目录](../02-reading/roots.md)
- [文档根目录与文件规范](../04-document-tools/structure.md)
