# Tworzenie dokumentu z szablonu

Na karcie [Utwórz] w Narzędziach dokumentów można wybrać szablon, wyświetlić podgląd treści, a następnie utworzyć nowy dokument.

1. Na pasku narzędzi naciśnij [Narzędzia dokumentów] i otwórz kartę [Utwórz].
2. Naciśnij [Utwórz z szablonu] i wybierz szablon.
3. Wypełnij pola (tytuł, opis i tak dalej). Pola obowiązkowe są oznaczone słowem „Wymagane”.
4. Wpisz miejsce zapisu jako ścieżkę względem katalogu głównego dokumentacji (na przykład `03-design/api.md`).
5. Naciśnij [Podgląd] i sprawdź wygenerowany Markdown.
6. Naciśnij [Utwórz z tą treścią].
   Dokument zostanie utworzony i wyświetlony w przeglądarce dokumentów. Następnie zostanie wykonane sprawdzanie całego katalogu głównego dokumentacji.

## Dostępne szablony

| Szablon | Treść |
|---|---|
| Dokument jednostronicowy | Krótka specyfikacja, notatka lub samodzielny dokument objaśniający w jednym pliku |
| Specyfikacja, podręcznik, pomoc | Jeden plik z ogólnym podziałem na rozdziały, przydatny w specyfikacji, podręczniku lub pomocy |
| Szablony Standard Pack | Gdy w pliku `lunascape-docs.json` wybrano Standard Pack, dochodzą rodzaje dokumentów dostępne w tym profilu (dokument wymagań, dokument projektowy i tak dalej) |

> **Uwaga**
>
> - Tworzenie wymaga zaufanego obszaru roboczego.
> - Istniejące pliki nie są nadpisywane. Jeżeli w miejscu zapisu znajduje się dokument o tej samej nazwie, utworzenie nie powiedzie się.
> - Miejsce zapisu wymaga rozszerzenia `.md` lub `.mdx`. Nie można tworzyć dokumentów w katalogu `i18n` (tam znajdują się tłumaczenia).
> - Po zmianie danych naciśnij ponownie [Podgląd], a dopiero potem utwórz dokument.

> **Wskazówka**
>
> W projekcie, który nie ma jeszcze folderu dokumentów, pierwszy zestaw można utworzyć poleceniem „Lunascape Docs: Utwórz dokumentację z szablonu” w palecie poleceń. Zobacz [Tworzenie pierwszych dokumentów](../01-introduction/first-documents.md).

## Zobacz też

- [Korzystanie z Narzędzi dokumentów](README.md)
- [Zmiana reguł sprawdzania](rules.md)
