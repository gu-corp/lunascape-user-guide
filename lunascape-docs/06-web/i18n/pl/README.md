# Co potrafi wersja przeglądarkowa

Przeglądarkowa wersja Lunascape Docs jest dostępna pod adresem <https://docs.lunascape.org/>. Bez instalowania czegokolwiek można czytać dokumenty z GitHub tak jak zwykłą witrynę.

## Możliwości

| Funkcja | Opis |
|---|---|
| Przeglądanie repozytoriów publicznych | Otwiera dokumenty z publicznego repozytorium GitHub bez logowania |
| Przeglądanie repozytoriów prywatnych | Po zalogowaniu się w GitHub otwiera repozytoria, do których masz prawo odczytu |
| Przeglądanie folderów lokalnych | Polecenie [Otwórz dokumenty], a następnie [Otwórz dokumenty z folderu lokalnego], otwiera folder na Twoim urządzeniu (tylko w obsługiwanych przeglądarkach) |
| Funkcje czytania | INDEX, odsyłacze, historia, filtrowanie, spis treści strony, przełączanie języka i przełączanie motywu. Tak samo jak w wersji VS Code |
| Diagramy i wzory matematyczne | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, wzory KaTeX |
| Wersje robocze | Dokumenty można edytować, a zmiany są przechowywane jako wersje robocze na urządzeniu. Nic nie jest zapisywane w repozytorium |
| Bezpośrednie odsyłacze do stron | Adres URL może wskazywać repozytorium i stronę, dzięki czemu konkretną stronę można otworzyć bezpośrednio |

## Różnice względem wersji VS Code

- Sprawdzanie dokumentów, tworzenie z szablonu, generowanie propozycji tłumaczenia oraz porządkowanie z poziomu INDEX nie są dostępne w wersji przeglądarkowej.
- Diagramy TikZ nie są rysowane.
- Zmiany nie są zapisywane w repozytorium, lecz stają się wersjami roboczymi na urządzeniu. „Prośba o publikację”, która wysyła wersje robocze jako pull request, została zaimplementowana, ale nie jest włączona w publicznej przeglądarce. Aby wprowadzić zmiany do repozytorium, edytuj je w wersji VS Code lub w lokalnym klonie.

## Powiązane tematy

- [Otwieranie repozytorium GitHub](open-repository.md)
- [Przeglądanie repozytorium prywatnego](private-repository.md)
- [Zapisywanie wersji roboczych](drafts.md)
