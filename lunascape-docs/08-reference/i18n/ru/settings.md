# Настройки VS Code

Найдите «Lunascape Docs» в настройках VS Code (`⌘,` / `Ctrl+,`), чтобы изменить следующие параметры. Все они являются персональными настройками и не сохраняются в документах проекта.

## Корень документации

| Настройка | Значения | По умолчанию | Действие |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` автоматически выбирает ближайший к открытому файлу Markdown корень документации, а если файл не принадлежит ни одному из них — временно открывает родительскую папку. `fixed` всегда открывает корень документации, указанный в `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Массив строк | `["docs"]` | Имена папок, которые в режиме `auto` автоматически распознаются как корни документации. Папка с файлом `lunascape-docs.json` распознается независимо от имени. Если в файле `lunascape-docs.json` в корне репозитория указаны `defaultFolder` или `roots`, приоритет имеют они |
| `lunascapeDocEditor.root` | Путь | `docs` | Корень документации относительно рабочей области — для режима `fixed` и при открытии из команды |
| `lunascapeDocEditor.startPage` | Путь | `README.md` | Начальная страница относительно корня документации |
| `lunascapeDocEditor.title` | Строка | `Lunascape Docs` | Переопределяет заголовок вкладки документа. На имя выбранного корня документации не влияет |
| `lunascapeDocEditor.ignoredDirectories` | Массив строк | `["99-archive"]` | Имена папок, исключаемых из INDEX |

## Отображение

| Настройка | Значения | По умолчанию | Действие |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` — белый фон, `auto` — следует цветовой схеме VS Code |
| `lunascapeDocEditor.locale` | Языковой тег | Нет | Ваш предпочитаемый язык документа, используемый при его наличии. Исходный язык проекта не изменяется |
| `lunascapeDocEditor.documentMetadata.compact` | Логическое значение | `true` | Сворачивает таблицу управления документом сразу после H1 в строку «Сведения о документе» |
| `lunascapeDocEditor.tree.showFileNames` | Логическое значение | `false` | Показывает в INDEX имена файлов вместо названий документов |
| `lunascapeDocEditor.tree.showDocumentIcons` | Логическое значение | `false` | Показывает в INDEX значки документов |
| `lunascapeDocEditor.tree.showFolderIcons` | Логическое значение | `false` | Показывает в INDEX значки папок |
| `lunascapeDocEditor.tree.showItemCounts` | Логическое значение | `false` | Показывает в INDEX число элементов, вложенных непосредственно в папку |
| `lunascapeDocEditor.tree.showGuides` | Логическое значение | `true` | Показывает в INDEX направляющие линии уровней вложенности |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Межстрочный интервал в INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Логическое значение | `true` | Закрывает INDEX один раз, если документ всего один |

## Редактирование

| Настройка | Значения | По умолчанию | Действие |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Режим редактирования, пока вы его не переключили. Приоритет имеет режим, использованный последним |
| `lunascapeDocEditor.editor.showEditButton` | Логическое значение | `true` | Показывает [Редактировать] в правом нижнем углу документа |

## Схемы

| Настройка | Значения | По умолчанию | Действие |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Среда отрисовки TikZ. `bundled` — входящая в комплект одобренная среда (в текущей версии дистрибутива не поставляется), `workspace` — `node-tikzjax` 1.0.5 в корне надежной рабочей области (только для разработки и оценки), `disabled` — отрисовка не выполняется |

## Устаревшие настройки

| Настройка | Что использовать вместо нее |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` в `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` в `lunascape-docs.json` |

Персональные настройки не могут переопределить языки проекта.

## Связанные темы

- [Изменение параметров отображения](../02-reading/display-settings.md)
- [Настройка проекта](../04-document-tools/project-configuration.md)
