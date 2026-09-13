# Rejestr i zapisy

Rejestr u góry karty [AI] pokazuje stan tłumaczenia dla każdego obsługiwanego języka. Jest przydatny także bez AI: mówi, czego brakuje.

| Etykieta | Znaczenie |
|---|---|
| Brak tłumaczenia | Liczba dokumentów, które nie mają jeszcze tłumaczenia |
| Nieaktualne | Liczba dokumentów, których tłumaczenie istnieje, ale dokument źródłowy jest nowszy niż zapis |
| Przetłumaczone | Liczba tłumaczeń nadążających za dokumentem źródłowym |

Rejestr jest obliczany przez przejście katalogu głównego dokumentacji. Nie bierze w tym udziału ani AI, ani model językowy.

## Aktualizacja zapisów tłumaczenia

Aby ustalić stan „nieaktualne”, potrzebny jest zapis dokumentu źródłowego i tłumaczenia z chwili tłumaczenia. AI działające w trybie sesji zapisuje pliki bezpośrednio, więc zapis nie powstaje automatycznie.

1. Gdy tłumaczenie jest gotowe i sprawdzisz jego treść, naciśnij [Aktualizuj zapisy tłumaczenia].
2. Tłumaczenia bez zapisu zostaną zapisane jako odpowiadające bieżącemu dokumentowi źródłowemu.

Sesje Claude Code i zapis przez dostawcę API tworzą zapisy automatycznie (sesja otrzymuje polecenie użycia narzędzia MCP `record_translation_freshness`). Ten przycisk jest potrzebny wtedy, gdy tłumaczysz w Codex lub w czacie VS Code.

Od tej pory zmiana dokumentu źródłowego oznacza jego tłumaczenie jako nieaktualne.

> **Uwaga**
>
> - Tłumaczenia, które mają już zapis, nie są nadpisywane. Dzięki temu istniejący stan „nieaktualne” nie zostaje skasowany.
> - Zapisy są przechowywane w pliku `.lunascape-docs/translation-freshness.json`. Zawierają tylko ścieżki względne, języki, skróty treści i datę z godziną — nigdy treści dokumentu.

## Tematy pokrewne

- [Zadania do przekazania](tasks.md)
- [Czytanie w innym języku](../02-reading/languages.md)
