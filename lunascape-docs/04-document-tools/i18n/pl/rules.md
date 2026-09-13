# Zmiana reguł sprawdzania

Możesz zmienić poziom powiadomienia każdego sprawdzenia (błąd, ostrzeżenie, informacja) albo wyłączyć dane sprawdzenie. Zmiany są zapisywane w pliku `docs-lint.config.json` w katalogu głównym dokumentacji i udostępniane zespołowi.

## Zmiana poziomu powiadomienia

1. Naciśnij [Narzędzia dokumentów] na pasku narzędzi i otwórz kartę [Sprawdzanie].
2. Naciśnij [Przejrzyj i zmień reguły].
   Lista sprawdzeń rozwinie się w tej samej karcie. Przy każdym sprawdzeniu widoczny jest jego cel oraz źródło bieżącego ustawienia (Project, Profile, Pack lub Default).
3. Wybierz poziom powiadomienia dla sprawdzenia, które chcesz zmienić.
4. Naciśnij [Zapisz i sprawdź ponownie].
   Ustawienie zostanie zapisane, a cały katalog główny dokumentacji zostanie sprawdzony ponownie z nową konfiguracją.

| Opcja | Znaczenie |
|---|---|
| [Ustawienie standardowe (…)] | Usuwa nadpisanie i przywraca ustawienie standardowe, wyznaczane kolejno przez profil, Standard Pack i wartość domyślną |
| [Nie używaj] | To sprawdzenie nie jest wykonywane |
| [Informacja] / [Ostrzeżenie] / [Błąd] | Zgłasza na tym poziomie powiadomienia |

> **Uwaga**
>
> - Zapisywanie wymaga zaufanego obszaru roboczego.
> - Zapisywany jest wyłącznie poziom powiadomienia każdego sprawdzenia. Opcje poszczególnych sprawdzeń pozostają bez zmian. Samego Standard Pack ani profilu nie zmienia się na tym ekranie.
> - Jeśli plik `docs-lint.config.json` został zmieniony zewnętrznie tuż przed zapisem, zapis zostaje przerwany. Załaduj najnowszy stan i spróbuj ponownie.
> - Jeśli plik `docs-lint.config.json` nie istnieje, zostanie utworzony przy zapisie.

## Bezpośrednia edycja plików konfiguracyjnych

- Naciśnięcie [Otwórz ustawienia szczegółowe] otwiera plik `docs-lint.config.json` w VS Code.
- Rozwiń [Źródło reguł i ustawienia dokumentów] i naciśnij [Edytuj ustawienia dokumentów], aby otworzyć plik `lunascape-docs.json` w VS Code. Standard Pack i profil wybiera się właśnie tam.

W obu plikach działa uzupełnianie i opisy pochodzące ze schematów JSON Schema dołączonych do rozszerzenia.

## Standard Pack i profile

Standard Pack to standard dokumentacji, który zbiera wymagane rodzaje dokumentów, układ rozdziałów, terminologię i szablony. Wybiera się go za pomocą `documentStandards` w pliku `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Dołączony pakiet `builtin:gu-corp-software` zawiera profile `base`, `web-application`, `api-service`, `regulated-financial-product` i `smart-contract`.

## Powiązane tematy

- [Sprawdzanie dokumentów](check.md)
- [Ustawienia projektu](project-configuration.md)
