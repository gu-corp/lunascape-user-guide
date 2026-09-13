# Настройки на VS Code

Потърсете „Lunascape Docs“ в настройките на VS Code (`⌘,` / `Ctrl+,`), за да промените следните елементи. Всички те са лични настройки и не се записват в документите на проекта.

## Коренна папка на документацията

| Настройка | Стойности | По подразбиране | Действие |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` избира автоматично най-близката коренна папка на документацията спрямо отворения файл на Markdown, а ако файлът не принадлежи на никоя, отваря временно родителската папка. `fixed` отваря винаги коренната папка, зададена в `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Масив от низове | `["docs"]` | Имената на папки, които се откриват автоматично като коренни папки на документацията в режим `auto`. Папка с `lunascape-docs.json` се открива независимо от името си. Ако `lunascape-docs.json` в корена на хранилището съдържа `defaultFolder` или `roots`, те имат предимство |
| `lunascapeDocEditor.root` | Път | `docs` | Коренната папка на документацията спрямо работното пространство — за режим `fixed` и при отваряне чрез командата |
| `lunascapeDocEditor.startPage` | Път | `README.md` | Началната страница спрямо коренната папка на документацията |
| `lunascapeDocEditor.title` | Низ | `Lunascape Docs` | Замества заглавието на раздела с документа. Не влияе върху името в избора на коренна папка на документацията |
| `lunascapeDocEditor.ignoredDirectories` | Масив от низове | `["99-archive"]` | Имената на папки, които се изключват от INDEX |

## Изглед

| Настройка | Стойности | По подразбиране | Действие |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` използва бял фон, а `auto` следва цветовата схема на VS Code |
| `lunascapeDocEditor.locale` | Езиков етикет | Няма | Личният ви език на документа, който се предпочита, когато е наличен. Не променя изходния език на проекта |
| `lunascapeDocEditor.documentMetadata.compact` | Булева стойност | `true` | Свива таблицата за управление на документа след H1 в реда „Информация за документа“ |
| `lunascapeDocEditor.tree.showFileNames` | Булева стойност | `false` | Показва в INDEX имената на файловете вместо имената на документите |
| `lunascapeDocEditor.tree.showDocumentIcons` | Булева стойност | `false` | Показва икони на документите в INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Булева стойност | `false` | Показва икони на папките в INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Булева стойност | `false` | Показва в INDEX броя на елементите непосредствено в папката |
| `lunascapeDocEditor.tree.showGuides` | Булева стойност | `true` | Показва в INDEX водещи линии за нивата |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Разстоянието между редовете в INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Булева стойност | `true` | Затваря INDEX само първия път, когато документът е само един |

## Редактиране

| Настройка | Стойности | По подразбиране | Действие |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Изгледът за редактиране, докато не превключите. Последно използваният изглед има предимство |
| `lunascapeDocEditor.editor.showEditButton` | Булева стойност | `true` | Показва [Редактиране] долу вдясно в текста |

## Диаграми

| Настройка | Стойности | По подразбиране | Действие |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Средата за изчертаване на TikZ. `bundled` използва вградената одобрена среда (не е включена в текущата разпространявана версия), `workspace` използва `node-tikzjax` 1.0.5 в корена на надеждно работно пространство (само за разработка и оценка), а `disabled` не изчертава нищо |

## Настройки, които не се препоръчват

| Настройка | Използвайте вместо това |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` в `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` в `lunascape-docs.json` |

Личните настройки не могат да заменят езиците на проекта.

## Свързани теми

- [Промяна на настройките на изгледа](../02-reading/display-settings.md)
- [Настройки на проекта](../04-document-tools/project-configuration.md)
