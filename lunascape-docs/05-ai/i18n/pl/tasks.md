# Dostępne zadania

Wybierz w zakładce [AI] w polu [Zadanie]. Każde zadanie zmienia przekazywane instrukcje oraz sprawdzanie wykonywane po jego zakończeniu.

| Zadanie | Treść | Wymagania | Typ API |
|---|---|---|---|
| Przetłumacz tę stronę | Tłumaczy wyświetlany dokument na wybrany język | Otwarty dokument, język docelowy | ○ |
| Przetłumacz wszystkie brakujące | Tłumaczy po kolei dokumenty wybranego języka oznaczone jako brak tłumaczenia oraz nieaktualne | Język docelowy | tylko typ sesyjny |
| Skoryguj tę stronę | Sprawdza i poprawia terminologię, styl oraz układ rozdziałów wymagany przez standard dokumentów | Otwarty dokument | ○ |
| Utwórz nowy dokument | Tworzy nowy dokument zgodnie ze standardem dokumentów i szablonami | Temat (opcjonalnie) | tylko typ sesyjny |

## Co zawierają instrukcje

| Nr | Treść |
|---|---|
| 1 | Położenie katalogu głównego dokumentacji wraz z poleceniem, aby nie zmieniać niczego poza nim |
| 2 | Język domyślny (dokument źródłowy) oraz miejsce, w którym znajdują się tłumaczenia (folder `i18n/<język>/` obok dokumentu) |
| 3 | Że `navigation.order` należy wyłącznie do dokumentu źródłowego, a tłumaczenie może nadpisać jedynie `navigation.title` |
| 4 | Że nie wolno zmieniać identyfikatorów wymagań, odnośników, kodu, Mermaid, TeX ani struktury front matter |
| 5 | Standard dokumentów i słownik terminów (`terminology` w pliku `docs-lint.config.json`) |
| 6 | Aby po zakończeniu uruchomić sprawdzanie dokumentów, zgłosić zmienione pliki i nie wykonywać żadnych operacji Git |

> **Wskazówka**
>
> Dokumenty dla zadania „Przetłumacz wszystkie brakujące" pochodzą z rejestru, po maksymalnie 200 dokumentów na jedno uruchomienie. Jeśli jest ich więcej, uruchom zadanie ponownie.

## Powiązane tematy

- [Przekazywanie pracy do AI](README.md)
- [Rejestr i zapisy](ledger.md)
