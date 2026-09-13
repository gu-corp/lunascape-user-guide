# Podstawowe operacje

Podstawowe czynności od otwarcia dokumentów do przejścia na stronę, którą chcesz przeczytać.

## Otwieranie dokumentów

1. Otwórz repozytorium w VS Code.
2. W palecie poleceń (`⇧⌘P` / `Ctrl+Shift+P`) uruchom polecenie „Lunascape Docs: Otwórz przeglądarkę specyfikacji”.
   Zostanie znaleziony najbliższy katalog główny dokumentacji (domyślnie folder `docs`) i wyświetlona jego strona początkowa.

> **Wskazówka**
>
> - Kliknij plik Markdown prawym przyciskiem myszy w Eksploratorze i wybierz [Lunascape Docs: Otwórz w przeglądarce specyfikacji], aby zacząć od tego pliku.
> - Po otwarciu pliku Markdown, który nie należy do żadnego katalogu głównego dokumentacji, jego folder jest wyświetlany jako tymczasowy katalog główny dokumentacji.

## Przechodzenie między stronami

| Czynność | Sposób |
|---|---|
| Otwarcie ze spisu treści | Naciśnij nazwę dokumentu w panelu INDEX po lewej stronie |
| Przejście po łączu | Naciśnij łącze w treści. Otworzy się w tym samym widoku |
| Poruszanie się po historii | [Wstecz] i [Dalej] na pasku narzędzi albo `Alt`+`←` / `Alt`+`→` |
| Powrót na stronę początkową | [Strona główna specyfikacji] na pasku narzędzi |
| Przejście o poziom wyżej | [Nadrzędny INDEX] na pasku narzędzi albo element ścieżki nawigacji |
| Poruszanie się w obrębie strony | Naciśnij nagłówek w panelu „Na tej stronie” po prawej stronie |

## Wyszukiwanie dokumentu

Wpisz słowo w polu [Filtruj dokumenty] nad panelem INDEX, aby wyświetlić tylko dokumenty o pasujących nazwach. Wyczyść pole, aby wrócić do pełnej listy.

## Aktualizowanie treści

Po zapisaniu pliku Markdown w edytorze VS Code widok jest aktualizowany automatycznie. Jeśli pliki zostały zmienione narzędziem zewnętrznym, naciśnij [Załaduj ponownie] na pasku narzędzi.

> **Uwaga**
>
> - Łącza zewnętrzne w treści (`https://` i podobne) otwierają się w domyślnej przeglądarce. Łącza do plików spoza katalogu głównego dokumentacji nie są otwierane.
> - Przeglądane dokumenty są przetwarzane na Twoim urządzeniu. Nic nie jest wysyłane na zewnątrz w celu ich odczytania.

## Powiązane tematy

- [Korzystanie z panelu INDEX](index-panel.md)
- [Przełączanie katalogu głównego dokumentacji](roots.md)
- [Edytowanie dokumentu](../03-editing/README.md)
