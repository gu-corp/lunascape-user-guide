# Konfiguracja projektu

Plik `lunascape-docs.json` bezpośrednio w katalogu głównym dokumentacji zawiera współdzieloną przez zespół konfigurację tego katalogu. Jest zarządzany w Git.

## Tworzenie i edytowanie pliku konfiguracji

- Na pasku narzędzi naciśnij [Narzędzia dokumentów] → kartę [Sprawdzanie] → [Źródło reguł i ustawienia dokumentów] → [Edytuj ustawienia dokumentów], aby otworzyć plik w VS Code. Jeśli plik nie istnieje, w tym momencie tworzony jest plik początkowy.
- Nazwa pliku `lunascape-docs.json` jest automatycznie powiązana z dołączonym schematem JSON Schema, który udostępnia uzupełnianie oraz opis każdego pola. Wpis `$schema` nie jest potrzebny.

## Przykład konfiguracji

```json
{
  "id": "product-docs",
  "title": "Dokumentacja produktu",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Opis pól

| Pole | Znaczenie | Domyślnie |
|---|---|---|
| `id` | Klucz, pod którym zapisywane są ustawienia widoku dla poszczególnych użytkowników. Nadaj mu stałą wartość, aby zachować ustawienia po przeniesieniu folderu | Ścieżka folderu |
| `title` | Nazwa wyświetlana na lewym końcu paska narzędzi oraz na liście katalogów głównych dokumentacji. Nie zmienia się przy zmianie języka interfejsu | Nagłówek README/index katalogu głównego, a w razie jego braku nazwa folderu |
| `indexTitle` | Nagłówek INDEX | `INDEX` |
| `startPage` | Dokument otwierany jako pierwszy (ścieżka względem katalogu głównego dokumentacji) | `README.md` |
| `appearance` | Kolorystyka: `light` (zawsze jasna) lub `auto` (zgodna z motywem VS Code) | `light` |
| `defaultLocale` | Język domyślny (język dokumentów źródłowych) jako tag języka BCP 47, na przykład `ja`, `en` lub `zh-Hant`. Jest to język wyjściowy tłumaczeń | Nieustawione (wywnioskowane z treści tylko do wyświetlania) |
| `fallbackLocale` | Język pokazywany najpierw czytelnikom, których język środowiska nie pasuje do żadnego z obsługiwanych języków. Wskaż język zawarty w `locales` | Nieustawione (używany jest `defaultLocale`) |
| `locales` | Lista obsługiwanych języków, wraz z `defaultLocale`. Pojawiają się w menu języków i są językami docelowymi tłumaczenia | Tylko `defaultLocale` |
| `ignoredDirectories` | Nazwy folderów wykluczonych z INDEX, wyszukiwania i sprawdzania. Podanie tej wartości zastępuje wartość domyślną | `["99-archive"]` |
| `tree` | Wartości domyślne sposobu wyświetlania INDEX. Użytkownicy mogą je nadpisać w ustawieniach widoku | Jak w przykładzie powyżej |
| `editor.defaultMode` | Widok edycji używany, dopóki użytkownik go nie przełączy: `visual` lub `source` | `visual` |
| `editor.showEditButton` | Czy w prawym dolnym rogu dokumentu wyświetlany jest [Edytuj] | `true` |
| `documentStandards.pack` | Standard Pack używany do sprawdzania dokumentów i szablonów: `builtin:<nazwa>` lub ścieżka względem katalogu głównego dokumentacji | Brak |
| `documentStandards.profile` | Nazwa profilu zdefiniowana przez Pack | Brak |
| `translation.enabled` | Włącza tworzenie propozycji tłumaczeń i tłumaczenie zbiorcze | `true` |
| `translation.contextFiles` | Pliki Markdown dokumentu źródłowego (ścieżki względem katalogu głównego dokumentacji) przekazywane podczas tłumaczenia jako materiał odniesienia dla terminologii i stylu | `[]` |
| `translation.maxContextCharacters` | Górny limit łącznej liczby znaków dokumentów odniesienia (maksymalnie 1048576) | `49152` |
| `description` | Jednowierszowy opis zestawu dokumentów, wyświetlany na kartach na stronie głównej repozytorium. Podobnie jak `title`, można go zapisać jako ciąg znaków lub obiekt z podziałem na języki | Brak |

## Wskazanie, gdzie w repozytorium znajdują się dokumenty

Plik `lunascape-docs.json` umieszczony bezpośrednio w repozytorium może zawierać nie ustawienia tego folderu, lecz **mapę repozytorium**. Wpisanie któregokolwiek z poniższych trzech pól tworzy mapę, a sam folder nie staje się wtedy katalogiem głównym dokumentacji.

| Pole | Do czego służy | Domyślnie |
|---|---|---|
| `defaultFolder` | Który folder zawiera dokumenty (ścieżka względem tego folderu). Wskazany folder nie potrzebuje własnej konfiguracji | Brak (używany jest `docs`) |
| `roots` | Lista zestawów dokumentów, gdy jest ich kilka (ścieżki względem tego folderu, w kolejności wyświetlania). W tym przypadku ten folder staje się stroną główną | Brak |
| `excludes` | Foldery wykluczone z wykrywania katalogów głównych dokumentacji (ścieżki względem tego folderu). Dodawane do domyślnych wykluczeń, takich jak `node_modules` | `[]` |
| `home.cards` | Czy strona główna wyświetla karty zestawów dokumentów pod swoim README. Ustaw na `false`, jeśli sam wpisujesz odnośniki w README | `true` |

Katalog główny dokumentacji jest ustalany w następującej kolejności. Używany jest pierwszy znaleziony, licząc od góry.

1. Gdy folder został wskazany w ustawieniu lub w poleceniu — ten folder
2. Cel wskazany przez `defaultFolder` lub `roots` w pliku `lunascape-docs.json` w katalogu bezpośrednim
3. Folder zawierający plik `lunascape-docs.json` (jeśli pod wspólnym rodzicem są dwa lub więcej, ten rodzic staje się stroną główną)
4. Folder `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Sam katalog bezpośredni repozytorium

> **Wskazówka**
>
> Jeśli nic nie wpiszesz, zadziała punkt 4, więc zwykłe repozytorium z jednym folderem `docs/` działa tak jak dotychczas. Wpisz `defaultFolder` tylko wtedy, gdy folder nazywa się inaczej, na przykład `manual`.

### Przykład mapy

```json
{
  "title": "Lunascape — pomoc",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Priorytet ustawień

Pola dotyczące wyświetlania mają priorytet w następującej kolejności.

1. Ustawienia widoku użytkownika (panel [Ustawienia widoku])
2. Ustawienia VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Wartości domyślne produktu

Wyjątkiem są wyłącznie języki (`defaultLocale`, `fallbackLocale`, `locales`) — tu rozstrzygający jest `lunascape-docs.json`. Osobiste ustawienia VS Code nie mogą nadpisać języków projektu.

> **Uwaga**
>
> Standard Pack można również określić jako `standard` w pliku `docs-lint.config.json`. Gdy występuje w obu miejscach, pierwszeństwo ma `docs-lint.config.json`.

## Powiązane tematy

- [Zmiana reguł sprawdzania](rules.md)
- [Zmiana ustawień widoku](../02-reading/display-settings.md)
- [Lista ustawień VS Code](../08-reference/settings.md)
