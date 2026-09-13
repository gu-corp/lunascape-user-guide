# Параметри VS Code

У параметрах VS Code (`⌘,` / `Ctrl+,`) знайдіть «Lunascape Docs», щоб змінити наведені нижче пункти. Усі вони є особистими параметрами користувача й ніколи не зберігаються в документах проєкту.

## Корінь документації

| Параметр | Значення | За замовчуванням | Призначення |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` автоматично вибирає корінь документації, найближчий до відкритого файлу Markdown, а якщо файл не належить до жодного — тимчасово відкриває батьківську папку. `fixed` завжди відкриває корінь документації, указаний у `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Масив рядків | `["docs"]` | Назви папок, які в режимі `auto` автоматично виявляються як корінь документації. Папка з файлом `lunascape-docs.json` виявляється незалежно від назви. Якщо у файлі `lunascape-docs.json` у корені репозиторію є `defaultFolder` або `roots`, перевагу мають вони |
| `lunascapeDocEditor.root` | Шлях | `docs` | Корінь документації відносно робочої області для режиму `fixed` або для відкриття командою |
| `lunascapeDocEditor.startPage` | Шлях | `README.md` | Початкова сторінка відносно кореня документації |
| `lunascapeDocEditor.title` | Рядок | `Lunascape Docs` | Замінює назву вкладки документа. На назву вибраного кореня документації не впливає |
| `lunascapeDocEditor.ignoredDirectories` | Масив рядків | `["99-archive"]` | Назви папок, які виключаються з INDEX |

## Відображення

| Параметр | Значення | За замовчуванням | Призначення |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` — біле тло, `auto` — відповідно до колірної схеми VS Code |
| `lunascapeDocEditor.locale` | Мовний тег | Немає | Ваша особиста мова документа, якій надається перевага, коли вона доступна. Мову оригіналу документа проєкту не змінює |
| `lunascapeDocEditor.documentMetadata.compact` | Логічне значення | `true` | Згортає таблицю керування документом одразу після H1 у рядок «Відомості про документ» |
| `lunascapeDocEditor.tree.showFileNames` | Логічне значення | `false` | Показує в INDEX імена файлів замість назв документів |
| `lunascapeDocEditor.tree.showDocumentIcons` | Логічне значення | `false` | Показує в INDEX піктограми документів |
| `lunascapeDocEditor.tree.showFolderIcons` | Логічне значення | `false` | Показує в INDEX піктограми папок |
| `lunascapeDocEditor.tree.showItemCounts` | Логічне значення | `false` | Показує в INDEX кількість елементів безпосередньо в папці |
| `lunascapeDocEditor.tree.showGuides` | Логічне значення | `true` | Показує в INDEX напрямні лінії рівнів вкладеності |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Відстань між рядками в INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Логічне значення | `true` | Закриває INDEX лише першого разу, коли є лише один документ |

## Редагування

| Параметр | Значення | За замовчуванням | Призначення |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Подання редагування, доки ви його не перемкнули. Перевагу має подання, яке використовувалося востаннє |
| `lunascapeDocEditor.editor.showEditButton` | Логічне значення | `true` | Показує [Редагувати] у правому нижньому куті тексту |

## Діаграми

| Параметр | Значення | За замовчуванням | Призначення |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Середовище виконання для малювання TikZ. `bundled` — вбудоване схвалене середовище (у поточній версії дистрибутива не постачається), `workspace` — `node-tikzjax` 1.0.5 у корені надійної робочої області (лише для розробки та оцінювання), `disabled` — не малює нічого |

## Застарілі параметри

| Параметр | Що використовувати натомість |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` у `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` у `lunascape-docs.json` |

Особисті параметри не можуть перевизначити мови проєкту.

## Пов'язані теми

- [Змінення параметрів відображення](../02-reading/display-settings.md)
- [Налаштування проєкту](../04-document-tools/project-configuration.md)
