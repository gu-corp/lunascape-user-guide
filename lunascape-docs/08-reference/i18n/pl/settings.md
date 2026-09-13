# Ustawienia VS Code

Po wyszukaniu „Lunascape Docs” w ustawieniach VS Code (`⌘,` / `Ctrl+,`) można zmienić poniższe pozycje. Wszystkie są ustawieniami osobistymi i nie są zapisywane w dokumentach projektu.

## Katalog główny dokumentacji

| Ustawienie | Wartości | Domyślnie | Działanie |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` wybiera katalog główny dokumentacji położony najbliżej otwartego pliku Markdown, a gdy plik do żadnego nie należy, tymczasowo otwiera folder nadrzędny. `fixed` zawsze otwiera katalog główny wskazany w `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Tablica ciągów znaków | `["docs"]` | Nazwy folderów wykrywanych jako katalogi główne dokumentacji w trybie `auto`. Folder z plikiem `lunascape-docs.json` jest wykrywany niezależnie od nazwy. Gdy plik `lunascape-docs.json` w katalogu głównym repozytorium zawiera `defaultFolder` lub `roots`, mają one pierwszeństwo |
| `lunascapeDocEditor.root` | Ścieżka | `docs` | Katalog główny dokumentacji względem obszaru roboczego, używany w trybie `fixed` oraz przy otwieraniu poleceniem |
| `lunascapeDocEditor.startPage` | Ścieżka | `README.md` | Strona początkowa względem katalogu głównego dokumentacji |
| `lunascapeDocEditor.title` | Ciąg znaków | `Lunascape Docs` | Zastępuje tytuł karty dokumentu. Nie wpływa na nazwę wybranego katalogu głównego dokumentacji |
| `lunascapeDocEditor.ignoredDirectories` | Tablica ciągów znaków | `["99-archive"]` | Nazwy folderów wykluczonych z INDEX |

## Wyświetlanie

| Ustawienie | Wartości | Domyślnie | Działanie |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` daje białe tło, `auto` podąża za kolorystyką VS Code |
| `lunascapeDocEditor.locale` | Znacznik języka | Brak | Osobisty język dokumentu, używany z pierwszeństwem, gdy jest dostępny. Nie zmienia języka dokumentu źródłowego projektu |
| `lunascapeDocEditor.documentMetadata.compact` | Wartość logiczna | `true` | Zwija tabelę zarządzania dokumentem znajdującą się po nagłówku H1 do wiersza „Informacje o dokumencie” |
| `lunascapeDocEditor.tree.showFileNames` | Wartość logiczna | `false` | Pokazuje w INDEX nazwy plików zamiast nazw dokumentów |
| `lunascapeDocEditor.tree.showDocumentIcons` | Wartość logiczna | `false` | Pokazuje w INDEX ikony dokumentów |
| `lunascapeDocEditor.tree.showFolderIcons` | Wartość logiczna | `false` | Pokazuje w INDEX ikony folderów |
| `lunascapeDocEditor.tree.showItemCounts` | Wartość logiczna | `false` | Pokazuje w INDEX liczbę elementów bezpośrednio w folderze |
| `lunascapeDocEditor.tree.showGuides` | Wartość logiczna | `true` | Pokazuje w INDEX linie prowadzące hierarchii |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Odstęp między wierszami w INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Wartość logiczna | `true` | Gdy dokument jest tylko jeden, zamyka INDEX przy pierwszym otwarciu |

## Edytowanie

| Ustawienie | Wartości | Domyślnie | Działanie |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Widok edycji używany, dopóki go nie przełączysz. Pierwszeństwo ma widok użyty ostatnio |
| `lunascapeDocEditor.editor.showEditButton` | Wartość logiczna | `true` | Pokazuje [Edytuj] w prawym dolnym rogu treści |

## Diagramy

| Ustawienie | Wartości | Domyślnie | Działanie |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Środowisko uruchomieniowe rysujące TikZ. `bundled` to dołączone, zatwierdzone środowisko (nie jest dołączone do bieżącej wersji dystrybucyjnej), `workspace` to `node-tikzjax` 1.0.5 w katalogu głównym zaufanego obszaru roboczego (wyłącznie do prac rozwojowych i oceny), `disabled` nie rysuje niczego |

## Ustawienia niezalecane

| Ustawienie | Czego użyć zamiast |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` w `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` w `lunascape-docs.json` |

Ustawieniami osobistymi nie można zastąpić języków projektu.

## Powiązane tematy

- [Zmiana ustawień widoku](../02-reading/display-settings.md)
- [Konfiguracja projektu](../04-document-tools/project-configuration.md)
