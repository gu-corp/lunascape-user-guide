# Sprawdzanie, tworzenie lub tłumaczenie nie działa

## Sprawdzanie

### Pojawia się komunikat „Nie można użyć docs-lint"

- Rozszerzenie nie zawiera środowiska uruchomieniowego docs-lint albo konfiguracja jest nieprawidłowa. Zainstaluj rozszerzenie ponownie.
- „Aby bezpiecznie wczytać lokalny pakiet i ustawienia, zaufaj temu obszarowi roboczemu w VS Code": korzystanie z lokalnego Standard Pack wymaga zaufanego obszaru roboczego.

### Wynik pozostaje w stanie „wymagana ponowna weryfikacja"

Zmiana dokumentu lub ustawienia unieważnia poprzedni wynik. Naciśnij ponownie [Sprawdź katalog główny dokumentacji]. Niezapisane zmiany nie są uwzględniane.

### Naciśnięcie uwagi niczego nie otwiera

Pozycje dotyczące „całego katalogu głównego dokumentacji" nie są powiązane z konkretnym dokumentem, więc nie mają położenia. Sprawdź dokumenty wskazane w treści uwagi.

### Nie można zapisać reguł

- Wymagany jest zaufany obszar roboczy.
- „Ustawienia lint zostały zmienione przez inną operację": plik `docs-lint.config.json` został zmieniony z zewnątrz. Wczytaj najnowszy stan i spróbuj ponownie.
- Nie można edytować dowiązań symbolicznych ani plików ustawień znajdujących się poza katalogiem głównym dokumentacji.

## Tworzenie z szablonu

- „Podgląd szablonu wygasł" / „Dane wejściowe zostały zmienione": naciśnij ponownie [Podgląd], a następnie utwórz dokument.
- „Dokument w miejscu zapisu już istnieje": istniejące pliki nie są nadpisywane. Wskaż inne miejsce zapisu.
- Miejsce zapisu wymaga ścieżki względem katalogu głównego dokumentacji oraz rozszerzenia `.md` lub `.mdx`. Nie można tworzyć plików w katalogu `i18n`.
- „Aby tworzyć dokumenty, zaufaj obszarowi roboczemu": zaufaj obszarowi roboczemu w VS Code.

<!-- ai-only:start -->
## Tłumaczenie

### Nie można nacisnąć przycisków tłumaczenia

- „Tłumaczenie AI nie jest włączone dla tego katalogu głównego dokumentacji": ustaw `translation.enabled` na `true` w pliku `lunascape-docs.json`.
- „Nie ustawiono języka domyślnego projektu": zapisz język domyślny zgodnie z opisem w [Zmiana ustawień widoku](../02-reading/display-settings.md).
- „Dodaj język docelowy do obsługiwanych języków": dodaj język docelowy do `locales`.
- „Nie znaleziono dokumentu źródłowego do przetłumaczenia": otwarta jest strona tłumaczenia. Przełącz się na stronę w języku domyślnym.
- Przy tymczasowym otwarciu folderu tłumaczenie zbiorcze jest niedostępne. Umieść w tym folderze plik `lunascape-docs.json`, aby stał się katalogiem głównym dokumentacji.

### Propozycja tłumaczenia jest odrzucana lub wymaga ponownego utworzenia

- „Dokument źródłowy został zmieniony. Utwórz propozycję tłumaczenia ponownie": po utworzeniu propozycji zmienił się dokument źródłowy lub docelowy. Przetłumacz jeszcze raz.
- Odpowiedź modelu językowego, w której brakuje chronionych identyfikatorów lub kodu, nie jest przyjmowana. Treść odpowiedzi można sprawdzić w panelu wyjściowym „Lunascape Docs Tłumaczenie".
- „Tłumaczenie zbiorcze obejmuje maksymalnie 1000 dokumentów naraz": podziel zakres według folderów lub przez jawny wybór.
<!-- ai-only:end -->

## Powiązane tematy

- [Sprawdzanie dokumentów](../04-document-tools/check.md)
- [Tworzenie dokumentu z szablonu](../04-document-tools/templates.md)
- [Przekazywanie pracy do AI](../05-ai/README.md)
