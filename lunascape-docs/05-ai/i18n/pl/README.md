# Przekazywanie pracy do AI

Lunascape Docs nie wywołuje modelu językowego. Przygotowuje **kontekst, narzędzia i sprawdzanie**, a tłumaczenie, korektę i tworzenie tekstu pozostawia AI, z którego korzystasz.

## Zasada działania

| Co zapewnia produkt | Zawartość |
|---|---|
| Kontekst | Konwencje dokumentacji (miejsce tłumaczeń, front matter, standard dokumentu, glosariusz) oraz położenie dokumentu docelowego |
| Narzędzia pracy | Rejestr braków tłumaczeń i nieaktualnych tłumaczeń, odczyt i zapis dokumentów, tworzenie z szablonów |
| Sprawdzanie po pracy | Weryfikacja przez docs-lint, różnice w pokryciu i aktualności |

Polecenie nie zawiera treści dokumentu: AI samo odczytuje pliki, samo je zapisuje i samo je weryfikuje.

## Przekazanie pracy

1. Naciśnij [Narzędzia dokumentów] na pasku narzędzi i otwórz kartę [AI].
2. W polu [Zadanie] wybierz pracę, którą chcesz przekazać.
3. Wypełnij wymagane pola (język docelowy, temat).
4. Naciśnij [Przekaż to zadanie].
   Otworzy się terminal VS Code, a wybrane AI odbierze polecenie i rozpocznie pracę.

> **Wskazówka**
>
> Sesji Claude Code towarzyszą narzędzia pracy (serwer MCP `lunascape-docs`). Sesja może samodzielnie pobrać listę braków tłumaczeń i tłumaczeń nieaktualnych, uruchomić docs-lint oraz zapisać aktualność po tłumaczeniu.

## Sprawdzanie wyniku

| Rodzaj dostawcy | Gdzie trafia wynik |
|---|---|
| Sesyjny (Claude Code, Codex) | Zapisuje bezpośrednio w drzewie roboczym. **Sprawdź w różnicach Git** |
| API (modele językowe VS Code, Anthropic, zgodne z OpenAI) | Zwraca propozycję dla jednego dokumentu naraz. Sprawdź ją przyciskiem [Otwórz różnice] i zapisz przyciskiem [Zapisz] |

### Sprawdzanie propozycji dostawcy API

Po uruchomieniu z dostawcą API propozycja trafia na kartę [AI].

1. Naciśnij [Otwórz różnice] i porównaj propozycję z bieżącą treścią.
2. Jeśli wszystko się zgadza, naciśnij [Zapisz]. W przypadku tłumaczenia zapisywana jest też jego aktualność. Aby zrezygnować, naciśnij [Odrzuć].
   Aby przerwać generowanie w trakcie, naciśnij [Przerwij].

> **Uwaga**
>
> - Lunascape Docs nigdy nie dodaje zmian do przechowalni Git ani ich nie zatwierdza. Zawsze sprawdzaj zmiany w różnicach.
> - W obszarze roboczym, który nie jest zaufany, oraz podczas tymczasowego przeglądania folderu spoza katalogu głównego dokumentacji nie można przekazać pracy.

## Zobacz też

- [Dostępne zadania](tasks.md)
- [Ustawienia AI](settings.md)
- [Rejestr i zapisy](ledger.md)
