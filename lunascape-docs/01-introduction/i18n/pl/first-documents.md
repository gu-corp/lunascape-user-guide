# Tworzenie pierwszych dokumentów

W projekcie, który nie ma jeszcze folderu dokumentacji, początkowy zestaw dokumentów można utworzyć z palety poleceń.

1. Otwórz folder projektu w VS Code i oznacz obszar roboczy jako zaufany.
2. W palecie poleceń (`⇧⌘P` / `Ctrl+Shift+P`) uruchom polecenie „Lunascape Docs: Utwórz dokumentację z szablonu”.
   Jeśli obszar roboczy zawiera kilka folderów, wybierz ten, w którym mają powstać dokumenty.
3. Wybierz strukturę do utworzenia.
   - [Dokument jednostronicowy]: tylko plik `README.md`. Nadaje się do krótkiej specyfikacji, notatek lub pojedynczego dokumentu objaśniającego.
   - [Zestaw dokumentacji]: strona główna oraz strony wejściowe dla `specification/` (specyfikacja), `manual/` (podręcznik) i `help/` (pomoc).
4. Wpisz tytuł dokumentacji. Jest on używany w pliku README i w nagłówkach poszczególnych dokumentów.
5. Wpisz folder dokumentacji, który ma zostać utworzony. Ścieżka jest względna wobec obszaru roboczego, domyślnie `docs`.
6. Sprawdź listę plików do utworzenia i naciśnij [Utwórz].
   Po zakończeniu nowy plik `README.md` otworzy się w przeglądarce dokumentów.

> **Uwaga**
>
> - Istniejące pliki nie są nadpisywane. Jeśli choć jeden z plików do utworzenia już istnieje, nic nie zostanie utworzone, a operacja zostanie przerwana.
> - W obszarze roboczym, który nie jest zaufany, tworzenie nie jest możliwe.

> **Wskazówka**
>
> - Jeśli masz już folder dokumentacji, pomiń te kroki i przejdź do [Podstawowych operacji](../02-reading/README.md).
> - Gdy dokumentacja się rozrośnie, możesz dodawać dokumenty pojedynczo na karcie [Utwórz] w Narzędziach dokumentów, wybierając szablon.

## Zobacz także

- [Tworzenie dokumentu z szablonu](../04-document-tools/templates.md)
- [Katalogi główne dokumentacji i konwencje plików](../04-document-tools/structure.md)
