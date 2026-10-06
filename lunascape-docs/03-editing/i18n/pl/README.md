# Edytowanie dokumentu

Dokumenty można edytować bezpośrednio w przeglądarce. Ekran edycji ma widok wizualny, w którym edytujesz to, co widzisz, oraz widok źródła Markdown; jeden przycisk przełącza między nimi.

## Rozpoczynanie edycji

Naciśnij jeden z poniższych elementów. Wszystkie otwierają ten sam ekran edycji.

- [Edytuj] w prawym dolnym rogu treści
- [⋯] (Więcej operacji) w prawym górnym rogu treści → [Edytuj]
- Menu pozycji w INDEX → [Edytuj]

## Edytowanie

1. Edytuj treść bezpośrednio.
   Na pasku narzędzi u góry ekranu edycji dostępne są format akapitu (treść, nagłówki 1–4, cytat, kod), [Pogrubienie], [Kursywa], [Lista punktowana], [Lista numerowana], [Link], [Wstaw tabelę], [Rozmiar obrazu], [Cofnij] i [Ponów].
2. Aby edytować źródło Markdown bezpośrednio, naciśnij [Markdown].
   Naciśnij ponownie, aby wrócić do widoku wizualnego. Ostatnio użyty widok jest zapamiętywany i przywracany przy następnym naciśnięciu [Edytuj].
3. Naciśnij [Zapisz] (możesz też zapisać za pomocą Ctrl+S/⌘S).
   Zawartość zostaje zapisana do pliku Markdown i następuje powrót do widoku odczytu. Aby przerwać edycję i przywrócić ostatnio zapisaną zawartość, naciśnij [Odrzuć zmiany].

## Zawsze zaczynaj od ekranu edycji (tryb edycji)

Naciśnij [Tryb edycji] na pasku narzędzi, aby go włączyć: od tej chwili każdy dokument będzie otwierany od razu na ekranie edycji. Używaj tego, gdy piszesz w sposób ciągły, jak w notatniku.

- Gdy tryb jest włączony, naciśnięcie [Zapisz] nie zamyka ekranu edycji. [Odrzuć zmiany] przywraca ostatnio zapisaną zawartość, a ekran edycji pozostaje otwarty.
- Naciśnij ponownie, aby go wyłączyć i wrócić do widoku odczytu. Włączenie/wyłączenie jest zapamiętywane dla każdego użytkownika osobno.
- Nie jest wyświetlany w katalogu głównym dokumentacji, do którego nie można zapisywać (na przykład w źródle GitHub tylko do odczytu).

## Niezapisane zmiany

Niezapisane zmiany są automatycznie zachowywane na tym urządzeniu. Przejście do innego dokumentu ani zamknięcie karty lub okna ich nie usuwa.

- [Niezapisane] na ekranie edycji oznacza, że treść różni się od ostatnio zapisanej.
- Przy następnym otwarciu tego samego dokumentu praca zostaje wznowiona od zachowanych zmian i pojawia się o tym informacja. Jeśli oryginalny dokument został w międzyczasie zaktualizowany, również o tym informuje. Za pomocą [Odrzuć zmiany] można przywrócić najnowszą zawartość.
- Zachowane zmiany znikają po naciśnięciu [Zapisz] lub [Odrzuć zmiany]. Nie zostały one zapisane, więc nie pojawiają się w Git ani wśród wersji roboczych.

> **Uwaga**
>
> - Zapisywanie tylko zapisuje plik. Przygotowanie do zatwierdzenia (staging) ani zatwierdzanie w Git nigdy nie odbywają się automatycznie.
> - Wzory matematyczne oraz diagramy takie jak Mermaid, TikZ czy Vega-Lite są w widoku wizualnym pokazywane jako wynik renderowania. Aby zmienić ich zawartość, przełącz na [Markdown].
> - Dokumenty zawierające składnię specyficzną dla MDX (komponenty, `import` itp.) są edytowane wyłącznie w widoku Markdown, aby zachować tę składnię.
> - Front matter (ustawienia otoczone znakami `---` na początku) jest zachowywany nawet podczas edycji w widoku wizualnym.

> **Wskazówka**
>
> - Naciśnięcie [Otwórz w VS Code] otwiera plik w zwykłym edytorze tekstu. Zapisanie w edytorze tekstu automatycznie aktualizuje również widok w przeglądarce.
> - Aby ukryć przycisk [Edytuj], wyłącz [Przycisk edycji] w [Ustawienia widoku]. Aby ukryć go w całym projekcie, ustaw `editor.showEditButton` na `false` w `lunascape-docs.json`.
> - Domyślny widok początkowy (wizualny/Markdown) można zmienić za pomocą ustawienia `lunascapeDocEditor.editor.defaultMode` lub `editor.defaultMode` w `lunascape-docs.json`.

## Zobacz też

- [Tworzenie i porządkowanie dokumentów oraz folderów](organize.md)
- [Dostosowywanie rozmiaru obrazów](images.md)
- [Pisanie wzorów matematycznych](math.md)
- [Tworzenie diagramów i wykresów](diagrams.md)
