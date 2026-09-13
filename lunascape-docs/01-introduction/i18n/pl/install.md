# Instalowanie rozszerzenia

Rozszerzenie do VS Code „Lunascape Docs Pro” jest rozpowszechniane jako plik VSIX. Jest bezpłatne; „Pro” oznacza wersję, która przekazuje pracę AI i sama się aktualizuje.

## Wymagania

- VS Code 1.90 lub nowszy
- Funkcje zapisujące pliki — tworzenie dokumentów, porządkowanie INDEX, zapisywanie ustawień sprawdzania, tłumaczenie — działają tylko w obszarze roboczym oznaczonym w VS Code jako zaufany.

## Instalacja

1. Pobierz plik VSIX. Ten odnośnik zawsze wskazuje bieżącą wersję.

   [Pobierz lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Otwórz widok rozszerzeń (`⇧⌘X` / `Ctrl+Shift+X`).
3. Z menu `…` w prawym górnym rogu wybierz [Zainstaluj z pliku VSIX…] i wskaż pobrany plik.

### Z wiersza poleceń

Jedna linijka, jeśli wolisz nie opuszczać terminala. Pobiera i instaluje.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Uwaga**
> Jeśli polecenie `code` nie zostanie znalezione, uruchom [Polecenie powłoki: zainstaluj polecenie „code” w ścieżce PATH] z palety poleceń (`⇧⌘P` / `Ctrl+Shift+P`).

## Aktualizacja

Gdy zostanie opublikowana nowsza wersja, rozszerzenie pobiera ją i instaluje. VS Code proponuje ponowne załadowanie okna i wtedy zaczynasz z niej korzystać. Twoje ustawienia i dokumenty pozostają bez zmian.

Sprawdzanie odbywa się raz dziennie. Aby sprawdzić od razu, uruchom [Lunascape Docs: Sprawdź dostępność nowszej wersji] z palety poleceń (`⇧⌘P` / `Ctrl+Shift+P`).

Ustawienie `lunascapeDocEditor.update.check` zmienia to, co się dzieje.

| Ustawienie | Co się dzieje |
|---|---|
| Instaluj nowszą wersję po jej opublikowaniu | Domyślne |
| Powiadom mnie i pozwól decydować za każdym razem | Pojawia się powiadomienie i nic się nie zmienia, dopóki nie naciśniesz [Aktualizuj] |
| Nigdy nie sprawdzaj | Nic się nie dzieje |

### Gdy nie można zaktualizować

Komunikat „Nie udało się pobrać aktualizacji: No Servers” oznacza, że zainstalowana wersja to 0.22.18 lub wcześniejsza. Jej mechanizm aktualizacji zawodzi w ostatnim kroku za każdym razem, więc nie potrafi sam przejść do nowszej wersji. Zainstaluj ją raz ręcznie, jak powyżej; od tej pory będzie się aktualizować samodzielnie.

## Sprawdzanie wersji

Otwórz „Lunascape Docs Pro” w widoku rozszerzeń, aby zobaczyć zainstalowaną wersję. Będzie potrzebna przy zgłaszaniu problemu.

## Powiązane tematy

- [Tworzenie pierwszych dokumentów](first-documents.md)
- [Zgłaszanie problemu](../07-troubleshooting/report.md)
