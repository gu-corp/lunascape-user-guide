# Diagramy, wzory matematyczne lub obrazy nie są wyświetlane

## Rysunek TikZ wyświetla się jako zwinięte źródło

- Dystrybuowane rozszerzenie nie zawiera silnika renderowania TikZ. Jest to prawidłowe wyświetlanie.
- Do celów programistycznych i ewaluacyjnych zainstaluj `node-tikzjax` 1.0.5 bezpośrednio w katalogu głównym zaufanego obszaru roboczego i ustaw `lunascapeDocEditor.tikz.runtime` na `workspace`.
- Przeglądarkowa wersja Web nie renderuje TikZ.

## Wzory matematyczne wyświetlają się jako zwykły tekst

- Sprawdź znaczniki ograniczające. W tekście jest to `$...$` lub `\(...\)`, a dla wzorów w osobnym wierszu `$$...$$` lub `\[...\]`.
- Znak `$` wewnątrz kodu w tekście lub bloku kodu nie tworzy wzoru.
- Zapis przypominający kwotę, na przykład `$5 and $10`, nie jest traktowany jako wzór.
- Bardzo duże wzory lub wzory z rozbudowanym rozwijaniem makr nie są renderowane po przekroczeniu limitów (`maxSize: 50`, `maxExpand: 1000`). Podziel je na części.

## Diagram zgłasza, że nie można go narysować

- Komunikat o błędzie z Mermaid, Vega-Lite, WaveDrom i innych wskazuje problem ze składnią. Sprawdź źródło w ekranie edycji za pomocą [Markdown].
- Vega-Lite: dane osadź w `data.values` lub `datasets`. Nie można używać danych z zewnętrznych adresów URL ani znaczników obrazów.
- WaveDrom: zapisuj w ścisłym formacie JSON. Format JavaScript (na przykład klucze bez cudzysłowów) nie jest obsługiwany.
- Penrose: używaj wyłącznie `@preset set-theory` na początku oraz dozwolonych instrukcji (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „Wygenerowany plik SVG zawiera niebezpieczne odwołania”, „Wygenerowany plik SVG przekracza limit”: diagramy zawierające odwołania do zasobów zewnętrznych oraz diagramy zbyt duże nie są wyświetlane. Ogranicz zawartość lub usuń odwołania.

## Obraz nie jest wyświetlany

- Ścieżkę obrazu podaje się względem dokumentu. Obrazy znajdujące się poza katalogiem głównym dokumentacji nie są wyświetlane.
- Atrybut `width` w `<img>` przyjmuje wyłącznie liczbę (`width="360"`).

## Diagramy nie są wyświetlane na wyeksportowanej witrynie

Biblioteki renderujące dla TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob i Penrose są wczytywane w momencie wyświetlania. Umieść folder `vendor/` razem z wyeksportowaną witryną.

## Tematy pokrewne

- [Pisanie wzorów matematycznych](../03-editing/math.md)
- [Rysowanie diagramów i wykresów](../03-editing/diagrams.md)
- [Dostosowywanie rozmiaru obrazów](../03-editing/images.md)
