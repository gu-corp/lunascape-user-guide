# Przełączanie katalogów głównych dokumentacji

Katalog główny dokumentacji to najwyższy folder jednego zestawu dokumentów. INDEX, filtrowanie, sprawdzanie i tłumaczenie działają w obrębie jednego katalogu głównego dokumentacji.

## Jak wyszukiwany jest katalog główny dokumentacji

Lunascape Docs przechodzi w górę od otwartego pliku Markdown przez foldery nadrzędne i za katalog główny dokumentacji przyjmuje najbliższy folder spełniający jeden z poniższych warunków.

- Folder zawierający plik `lunascape-docs.json` (nazwa folderu jest dowolna)
- Folder o nazwie `docs` (kolejne nazwy można dodać w ustawieniu `lunascapeDocEditor.rootDirectoryNames`)

Po uruchomieniu polecenia „Lunascape Docs: Otwórz przeglądarkę specyfikacji” otwierany jest katalog główny dokumentacji z ustawienia `lunascapeDocEditor.root` (domyślnie `docs`).

## Przełączanie na inny katalog główny dokumentacji

Gdy obszar roboczy zawiera kilka katalogów głównych dokumentacji, nazwa katalogu przy lewej krawędzi paska narzędzi staje się listą rozwijaną.

1. Naciśnij nazwę katalogu głównego dokumentacji przy lewej krawędzi paska narzędzi.
2. Wybierz katalog główny dokumentacji z listy.
   Zostanie wyświetlona jego strona początkowa, a INDEX przełączy się.

> **Wskazówka**
>
> Nazwy na liście ustalane są w następującej kolejności. Nie zmieniają się po przełączeniu języka interfejsu.
>
> 1. `title` w pliku `lunascape-docs.json`
> 2. `navigation.title` z pliku `README.md` w katalogu głównym, a w razie jego braku nagłówek H1 tego pliku
> 3. `navigation.title` z pliku `index.md` w katalogu głównym, a w razie jego braku nagłówek H1 tego pliku
> 4. Nazwa folderu (w przypadku standardowego folderu `docs` — nazwa jego folderu nadrzędnego)

## Otwieranie pliku Markdown spoza katalogu głównego dokumentacji

Po otwarciu pliku Markdown, który nie należy do żadnego katalogu głównego dokumentacji, folder tego pliku jest wyświetlany jako tymczasowy katalog główny dokumentacji. W panelu INDEX wyświetlane są pliki Markdown z tego folderu i z folderów poniżej.

- Naciśnij [Folder wyżej] na pasku narzędzi, aby rozszerzyć zakres wyświetlania do folderu nadrzędnego w obszarze roboczym.
- W tym widoku nie są dostępne ustawienia języka projektu ani tłumaczenie zbiorcze. Aby ich używać, umieść w folderze plik `lunascape-docs.json` i uczyń go katalogiem głównym dokumentacji.

## Zawsze otwieranie ustalonego katalogu głównego dokumentacji

Ustaw `lunascapeDocEditor.rootMode` na `fixed`, aby niezależnie od otwieranego pliku Markdown zawsze otwierany był katalog główny dokumentacji z ustawienia `lunascapeDocEditor.root`.

## Tematy pokrewne

- [Katalogi główne dokumentacji i konwencje plików](../04-document-tools/structure.md)
- [Konfiguracja projektu](../04-document-tools/project-configuration.md)
- [Lista ustawień VS Code](../08-reference/settings.md)
