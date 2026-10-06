# Czym jest Lunascape Docs

Lunascape Docs to narzędzie, które pozwala traktować dokumenty Markdown umieszczone w repozytorium Git bezpośrednio jako „witrynę specyfikacji”. Nie są potrzebne wstępne budowanie, serwer dokumentów ani osobna baza danych.

## Co można zrobić

| Cel | Główne funkcje |
|---|---|
| Czytanie | INDEX (spis treści), linki w treści, ścieżka nawigacji, Wstecz i Dalej, spis treści strony, wyszukiwanie z filtrowaniem |
| Wyświetlanie | Tabele, bloki kodu, automatyczne dopasowanie obrazów, wzory matematyczne KaTeX, diagramy Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, zwinięte tabele kontroli dokumentu |
| Pisanie | Przełączanie między edycją wizualną a edycją źródła Markdown, tworzenie, duplikowanie, zmiana nazwy i zmiana kolejności z poziomu INDEX |
| Sprawdzanie | Sprawdzanie dokumentów za pomocą docs-lint, weryfikacja wymaganych dokumentów, rozdziałów i terminów na podstawie Standard Pack, tworzenie dokumentów z szablonów |
| Tłumaczenie | Generowanie propozycji tłumaczenia dla jednej strony lub zbiorczo. Zapis dopiero po sprawdzeniu <!-- ai-only --> |
| Korzystanie z poziomu AI | Narzędzie specyfikacji tylko do odczytu, z którego mogą korzystać agenci VS Code <!-- ai-only --> |

## Dostępne środowiska

| Środowisko | Zastosowanie |
|---|---|
| Rozszerzenie VS Code | Przeglądanie, edycja, sprawdzanie i tłumaczenie repozytorium na komputerze. Ta pomoc dotyczy głównie tego środowiska |
| Wersja przeglądarkowa | Przeglądanie dokumentów w serwisie GitHub (publicznych i prywatnych), wersje robocze na urządzeniu, przeglądanie folderu lokalnego |
| Rozszerzenie Chromium | Otwiera wersję przeglądarkową w karcie przeglądarki |

## Podstawowe zasady

- **Dokumentem źródłowym jest Markdown.** Dokumenty pozostają plikami Markdown zarządzanymi przez Git. Lunascape Docs nie przechowuje ich po konwersji do innego formatu.
- **Zapis wykonuje użytkownik.** Zmiany są zapisywane w pliku tylko po naciśnięciu [Zapisz]. Dodawanie zmian do indeksu Git ani tworzenie commitów nie odbywa się automatycznie.
- **Dokumenty są przetwarzane na urządzeniu.** Podczas przeglądania ani edycji dokumenty nie są wysyłane na zewnątrz. Tylko przy tłumaczeniu najpierw wyświetlane jest miejsce docelowe i wysyłana treść, a wysyłka następuje dopiero po zatwierdzeniu.
- **Tłumaczenia znajdują się w `i18n/<locale>/`.** Dokumenty w języku domyślnym pozostają na swoim miejscu, a wersje przetłumaczone są umieszczane pod tą samą ścieżką względną w folderach takich jak `i18n/en/`.
- **AI tylko proponuje.** Propozycje tłumaczenia są zapisywane dopiero po sprawdzeniu różnic. Dokumenty nigdy nie są zmieniane bez wiedzy użytkownika. <!-- ai-only -->

## Zobacz także

- [Nazwy i funkcje elementów ekranu](screen.md)
- [Instalowanie rozszerzenia](install.md)
- [Podstawowa obsługa](../02-reading/README.md)
