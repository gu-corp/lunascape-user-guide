# Czym jest Lunascape Docs

Lunascape Docs to narzędzie, które traktuje dokumenty Markdown umieszczone w repozytorium Git wprost jako „witrynę ze specyfikacjami”. Nie jest potrzebna wcześniejsza kompilacja, serwer dokumentów ani osobna baza danych.

## Co można zrobić

| Cel | Główne funkcje |
|---|---|
| Czytanie | INDEX (spis treści), odsyłacze w tekście, ścieżka nawigacji, wstecz i dalej, spis treści strony, wyszukiwanie zawężające |
| Wyświetlanie | Tabele, bloki kodu, automatyczne dopasowanie obrazów, wzory matematyczne KaTeX, diagramy Mermaid, Vega-Lite, Markmap, WaveDrom i Svgbob, zwinięte tabele zarządzania dokumentem |
| Pisanie | Przełączanie między edycją wizualną a edycją źródła Markdown, tworzenie, powielanie, zmiana nazwy i kolejności z poziomu INDEX |
| Sprawdzanie | Sprawdzanie dokumentów przez docs-lint, kontrola wymaganych dokumentów, rozdziałów i terminów według Standard Pack, tworzenie z szablonu |
| Tłumaczenie | Generowanie propozycji tłumaczenia dla pojedynczej strony lub zbiorczo. Zapis po sprawdzeniu <!-- ai-only --> |
| Użycie przez AI | Narzędzie do specyfikacji tylko do odczytu, z którego może korzystać agent w VS Code <!-- ai-only --> |

## Dostępne środowiska

| Środowisko | Zastosowanie |
|---|---|
| Rozszerzenie VS Code | Przeglądanie, edycja, sprawdzanie i tłumaczenie repozytorium na własnym komputerze. To główny temat tej pomocy |
| Wersja dla przeglądarki internetowej | Przeglądanie dokumentów w GitHub (publicznych i prywatnych), wersje robocze na urządzeniu, przeglądanie folderu lokalnego |
| Rozszerzenie Chromium | Otwiera wersję dla przeglądarki internetowej w karcie przeglądarki |
| Przeglądarka Lunascape | Planowane wbudowanie tego samego modelu dokumentów |

## Podstawowe założenia

- **Markdown jest dokumentem źródłowym.** Dokumenty pozostają plikami Markdown zarządzanymi przez Git. Lunascape Docs nie przechowuje ich w przekształconej postaci.
- **Zapisu dokonuje użytkownik.** Zmiany są zapisywane do pliku dopiero po naciśnięciu [Zapisz]. Przygotowanie do zatwierdzenia ani zatwierdzanie w Git nie odbywa się automatycznie.
- **Dokumenty są przetwarzane na urządzeniu.** Do przeglądania i edycji dokumenty nie są wysyłane na zewnątrz. Tylko przy tłumaczeniu adresat i treść są wcześniej pokazywane, a wysyłka następuje po zatwierdzeniu.
- **Tłumaczenia znajdują się w `i18n/<język>/`.** Dokumenty w języku domyślnym pozostają na swoim miejscu, a tłumaczenia trafiają pod tą samą ścieżką względną do `i18n/en/` i podobnych folderów.
- **AI tylko proponuje.** Propozycje tłumaczenia są zapisywane po sprawdzeniu różnic. Dokumenty nie są zmieniane bez wiedzy użytkownika. <!-- ai-only -->

## Zobacz też

- [Nazwy i funkcje elementów ekranu](screen.md)
- [Instalowanie rozszerzenia](install.md)
- [Podstawowa obsługa](../02-reading/README.md)
