# Sprawdzanie dokumentów

docs-lint sprawdza strukturę nagłówków, niedziałające odnośniki, brakujące wymagane dokumenty i rozdziały, niespójną terminologię, zgodność identyfikatorów wymagań i inne elementy. Sprawdzanie zawsze obejmuje cały katalog główny dokumentacji.

## Uruchamianie sprawdzania

1. Naciśnij [Narzędzia dokumentów] na pasku narzędzi i otwórz kartę [Sprawdzanie].
2. Naciśnij [Sprawdź katalog główny dokumentacji].
   Możesz też użyć polecenia „Lunascape Docs: Sprawdź katalog główny dokumentacji" w palecie poleceń.
3. Przejrzyj listę wyników.

## Odczytywanie wyników

- Przełączniki [Ten dokument] / [Wszystkie] nad listą zmieniają zakres wyświetlania. Zakres samego sprawdzania zawsze obejmuje cały katalog główny dokumentacji.
- Uwagi mają cztery poziomy: błąd, ostrzeżenie, informacja i podpowiedź. Element [Narzędzia dokumentów] na pasku narzędzi pokazuje liczbę błędów i ostrzeżeń.
- Naciśnij uwagę, aby otworzyć odpowiednie miejsce w źródle Markdown w edytorze VS Code.
- Uwagi dotyczące całego katalogu głównego dokumentacji (na przykład brak dokumentu testów) pojawiają się jako pozycje „cały katalog główny dokumentacji" i nie mają położenia.
- Te same uwagi pojawiają się także w panelu „Problemy" w VS Code.

## Sprawdzane elementy

Naciśnij [Przejrzyj i zmień reguły], aby zobaczyć listę aktywnych sprawdzeń wraz z ich przeznaczeniem. Najważniejsze z nich to:

| Element | Znaczenie |
|---|---|
| Struktura nagłówków | Czy jest dokładnie jeden nagłówek H1 i czy poziomy nagłówków nie są pomijane |
| Odnośniki wewnętrzne | Czy dokumenty docelowe istnieją i nie wychodzą poza katalog główny dokumentacji |
| Język bloków kodu | Czy bloki kodu mają podaną nazwę języka |
| Wymagane foldery i dokumenty | Czy istnieją foldery i dokumenty wymagane przez profil Standard Pack |
| Wymagane rozdziały dokumentu | Czy każdy typ dokumentu ma wymagane rozdziały |
| Spójność terminologii | Wykrywanie wyrażeń, których należy unikać, i podpowiadanie zalecanych terminów |
| Nazewnictwo i duplikaty identyfikatorów wymagań | Czy identyfikatory wymagań są zgodne z regułą nazewnictwa i nie są zdefiniowane dwukrotnie |
| Zgodność odwołań do identyfikatorów wymagań | Czy identyfikatory wymagań przywoływane w projekcie, testach i tabelach stanu istnieją |
| Powiązanie wymagań z testami | Czy identyfikatory wymagań są przywoływane w dokumentach testów |

To, które elementy są aktywne, zależy od pakietu Standard Pack i profilu wybranych w pliku `lunascape-docs.json` oraz od pliku `docs-lint.config.json`.

> **Uwaga**
>
> - Zmiana dokumentu lub ustawienia oznacza poprzedni wynik jako „wymaga ponownego sprawdzenia". Nic nie jest zaliczane automatycznie; naciśnij ponownie [Sprawdź katalog główny dokumentacji].
> - Niezapisane zmiany nie są uwzględniane w sprawdzaniu. Najpierw zapisz.
> - Sprawdzanie działa lokalnie i deterministycznie. Wyniki oceny przez AI ani tłumaczenia nigdy nie mieszają się z wynikami sprawdzania.

## Powiązane tematy

- [Zmiana reguł sprawdzania](rules.md)
- [Konfiguracja projektu](project-configuration.md)
- [Sprawdzanie, tworzenie lub tłumaczenie nie działa](../07-troubleshooting/tools.md)
