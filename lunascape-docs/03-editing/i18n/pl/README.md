# Edytowanie dokumentu

Dokumenty można edytować bezpośrednio w przeglądarce dokumentów. Ekran edycji ma widok wizualny, w którym edytujesz to, co widzisz, oraz widok źródła Markdown; jeden przycisk przełącza między nimi.

## Rozpoczynanie edycji

Naciśnij jeden z poniższych elementów. Wszystkie otwierają ten sam ekran edycji.

- [Edytuj] w prawym dolnym rogu treści
- [⋯] (Więcej operacji) w prawym górnym rogu treści → [Edytuj]
- Menu pozycji w panelu INDEX → [Edytuj]

## Edytowanie

1. Edytuj treść bezpośrednio.
   Na pasku narzędzi u góry ekranu edycji dostępne są: format akapitu (treść, nagłówki 1–4, cytat, kod), [Pogrubienie], [Kursywa], [Lista punktowana], [Lista numerowana], [Link], [Wstaw tabelę], [Rozmiar obrazu], [Cofnij] i [Ponów].
2. Aby edytować źródło Markdown bezpośrednio, naciśnij [Markdown].
   Naciśnij ponownie, aby wrócić do widoku wizualnego. Ostatnio używany widok jest zapamiętywany i przywracany przy następnym naciśnięciu przycisku [Edytuj].
3. Naciśnij [Zapisz].
   Zmiany zostaną zapisane w pliku Markdown, a przeglądarka wróci do trybu czytania. Aby zrezygnować, naciśnij [Anuluj].

> **Uwaga**
>
> - Zapis powoduje wyłącznie zapisanie pliku. Przygotowanie zmian ani zatwierdzenie w Git nie odbywa się automatycznie.
> - Wzory matematyczne oraz diagramy, takie jak Mermaid, TikZ czy Vega-Lite, są w widoku wizualnym pokazywane jako gotowy rysunek. Aby zmienić ich treść, przełącz się na [Markdown].
> - Dokumenty zawierające składnię charakterystyczną dla MDX (komponenty, `import` i podobne) edytuje się wyłącznie w widoku Markdown, aby zachować tę składnię.
> - Front matter (ustawienia ujęte na początku pliku w znaczniki `---`) zostaje zachowany również przy edycji w widoku wizualnym.

> **Wskazówka**
>
> - Naciśnięcie [Otwórz w VS Code] otwiera plik w zwykłym edytorze tekstu. Zapis w edytorze tekstu automatycznie odświeża widok w przeglądarce dokumentów.
> - Aby ukryć przycisk [Edytuj], wyłącz opcję [Przycisk edycji] w [Ustawienia widoku]. Aby ukryć go w całym projekcie, ustaw `editor.showEditButton` na `false` w pliku `lunascape-docs.json`.
> - Domyślny widok otwierany jako pierwszy (wizualny lub Markdown) można zmienić ustawieniem `lunascapeDocEditor.editor.defaultMode` albo `editor.defaultMode` w pliku `lunascape-docs.json`.

## Powiązane tematy

- [Tworzenie i porządkowanie dokumentów oraz folderów](organize.md)
- [Dostosowywanie rozmiaru obrazów](images.md)
- [Pisanie wzorów matematycznych](math.md)
- [Tworzenie diagramów i wykresów](diagrams.md)
