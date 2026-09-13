# Tworzenie i porządkowanie dokumentów oraz folderów

Z menu elementu w panelu INDEX można tworzyć, duplikować, zmieniać nazwy i usuwać dokumenty oraz foldery. Dane wpisuje się w małym oknie dialogowym wewnątrz przeglądarki dokumentów, bez przerywania czytania.

> **Uwaga**
>
> Te operacje są dostępne tylko wtedy, gdy obszar roboczy jest zaufany w VS Code. Nie można ich wykonać podczas edycji dokumentu, w trakcie innej operacji ani wtedy, gdy element docelowy ma niezapisane zmiany.

## Tworzenie dokumentu lub folderu

1. Otwórz menu elementu ([⋯] lub kliknięcie prawym przyciskiem myszy) folderu docelowego.
   Aby utworzyć element bezpośrednio w katalogu głównym dokumentacji, użyj [⋯] po prawej stronie nagłówka INDEX albo kliknij prawym przyciskiem myszy puste miejsce w panelu INDEX.
2. Wybierz [Nowy dokument] lub [Nowy folder].
3. Wpisz nazwę i naciśnij [Utwórz].
   Nazwa dokumentu musi mieć rozszerzenie Markdown (`.md`, `.markdown`, `.mdx` itp.).

Nowe dokumenty są tworzone jako dokumenty w języku domyślnym (dokumenty źródłowe).

## Duplikowanie dokumentu

1. Otwórz menu elementu dokumentu i wybierz [Duplikuj].
2. Wpisz nową nazwę i naciśnij [Utwórz].

Duplikowany jest tylko dokument źródłowy. Tłumaczenia nie są duplikowane.

## Zmiana tytułu

Zmienia nagłówek dokumentu (H1). Nazwa pliku pozostaje bez zmian.

1. Otwórz menu elementu dokumentu lub folderu i wybierz [Zmień tytuł].
2. Wpisz nowy tytuł w jednym wierszu i naciśnij [Zmień].

W przypadku folderu zmieniany jest nagłówek pliku `README.md` w tym folderze. Jeśli wyświetlane jest tłumaczenie, zmieniany jest tytuł dokumentu w tym języku.

## Zmiana nazwy dokumentacji

Zmienia nazwę dokumentacji widoczną na pasku narzędzi (nazwę katalogu głównego dokumentacji).

1. Kliknij prawym przyciskiem myszy nazwę dokumentacji na pasku narzędzi. To samo menu otwiera [⋯] po prawej stronie nagłówka INDEX.
2. Wybierz [Zmień nazwę dokumentu] i wpisz nową nazwę.

Gdy nic nie jest ustawione, wyświetlana jest nazwa folderu.

Ustawiona nazwa jest zapisywana w **tym miejscu, które aktualnie dostarcza nazwę dokumentacji**, dzięki czemu widoczny nagłówek nigdy nie zostaje zignorowany.

| Stan bieżący | Miejsce zapisu |
|---|---|
| `lunascape-docs.json` zawiera nazwę | Aktualizowany jest plik `lunascape-docs.json` |
| Nazwy nie ma, ale katalog główny dokumentacji zawiera plik README | Zmieniany jest nagłówek (H1) pliku README |
| Żadne z powyższych | Tworzony jest plik `lunascape-docs.json` i tam zapisywana jest nazwa |

Komunikat wyświetlany po zmianie informuje, gdzie zapisano nazwę.

> **Wskazówka**
>
> Nazwa dokumentacji jest ustalana w następującej kolejności: nazwa w pliku `lunascape-docs.json`, następnie nagłówek pliku README w katalogu głównym dokumentacji, a na końcu nazwa folderu.

## Zmiana nazwy pliku lub folderu

1. Otwórz menu elementu i wybierz [Zmień nazwę pliku] lub [Zmień nazwę folderu].
2. Wpisz nową nazwę i naciśnij [Zmień].

Odpowiadające tłumaczenia (ta sama ścieżka w katalogu `i18n/<język>/`) otrzymują nową nazwę razem z oryginałem.

## Usuwanie

1. Otwórz menu elementu i wybierz [Przenieś do kosza].
2. Sprawdź treść komunikatu potwierdzenia i zatwierdź przeniesienie.

Element jest przenoszony do kosza systemu operacyjnego, więc w razie potrzeby można go przywrócić. Tłumaczenia nie są usuwane i pozostają na miejscu.

## Nazwy, których nie można używać

- Nazwy zaczynające się od `.` (nie byłyby widoczne w panelu INDEX)
- `i18n` (zarezerwowana dla plików tłumaczeń)
- Nazwy zarezerwowane w systemie Windows (`CON`, `PRN` itp.)
- Nazwy kończące się kropką lub spacją
- Nazwy zawierające znaki sterujące lub znaki niedozwolone w nazwach plików
- Nazwy już istniejące w tym samym folderze (w tym nazwy różniące się tylko wielkością liter)

> **Uwaga**
>
> Nie można zmienić nazwy ani przenieść strony startowej (zwykle jest to plik `README.md` w katalogu głównym). Najpierw zmień wartość `startPage` w pliku `lunascape-docs.json`.

## Powiązane tematy

- [Zmiana kolejności dokumentów](reorder.md)
- [Korzystanie z panelu INDEX](../02-reading/index-panel.md)
