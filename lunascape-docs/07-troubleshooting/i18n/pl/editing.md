# Nie można edytować, zapisywać ani zmieniać kolejności

## Brak przycisku [Edytuj]

- Opcja [Przycisk edycji] w [Ustawienia widoku] jest wyłączona. Włącz ją albo użyj [⋯] → [Edytuj] w prawym górnym rogu treści lub menu pozycji w INDEX → [Edytuj].
- To samo dotyczy sytuacji, gdy `editor.showEditButton` w pliku `lunascape-docs.json` ma wartość `false`.
- Podczas wyświetlania pomocy edycja jest niedostępna. Zamknij pomoc.

## Nie można przełączyć się na widok wizualny

„Ten dokument zawiera składnię MDX, dlatego nie można przełączyć się na zwykły ekran edycji”: dokumenty ze składnią właściwą dla MDX (komponenty, `import` i podobne) edytuje się wyłącznie w widoku Markdown, aby zachować tę składnię.

## Nie można bezpośrednio edytować wzorów matematycznych ani diagramów

Widok wizualny pokazuje wynik renderowania. Na ekranie edycji naciśnij [Markdown] i edytuj źródło.

## Nie można zmienić kolejności ani przeciągać

- Zmiana kolejności jest niedostępna podczas filtrowania, podczas edycji dokumentu oraz w trakcie innej operacji w INDEX.
- Gdy obszar roboczy nie jest zaufany, operacje tworzenia, porządkowania i usuwania są niedostępne. Oznacz obszar roboczy jako zaufany w VS Code.
- „INDEX został zaktualizowany. Przeciągnij ponownie”: właśnie została zastosowana inna zmiana. Wykonaj operację ponownie.
- Strony początkowej (plik `README.md` w katalogu głównym) nie można przenieść.

## Pojawia się komunikat „Istnieją niezapisane zmiany”

Wskazany plik jest edytowany w edytorze VS Code. Najpierw zapisz lub odrzuć zmiany, a potem spróbuj ponownie.

## Nie można zmienić nazwy

Nie można użyć następujących nazw.

- Nazwy zaczynające się od `.`, nazwa `i18n` oraz nazwy zastrzeżone w systemie Windows (np. `CON`)
- Nazwy kończące się kropką lub spacją oraz nazwy zawierające znaki sterujące lub znaki niedozwolone w nazwach plików
- Nazwy, które już istnieją w tym samym folderze (w tym nazwy różniące się wyłącznie wielkością liter)
- Nazwy dokumentów bez rozszerzenia Markdown

## Zapisano zmiany, ale nie widać ich w Git lub nie zostały zatwierdzone

Lunascape Docs tylko zapisuje plik. Nie dodaje zmian do przechowalni ani nie tworzy commitów w Git. Sprawdź widok kontroli źródła w VS Code i w razie potrzeby utwórz commit.

## Powiązane tematy

- [Edytowanie dokumentu](../03-editing/README.md)
- [Tworzenie i porządkowanie dokumentów oraz folderów](../03-editing/organize.md)
- [Zmiana kolejności dokumentów](../03-editing/reorder.md)
