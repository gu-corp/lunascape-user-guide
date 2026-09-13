# Diagramme, Formeln oder Bilder werden nicht angezeigt

## Ein TikZ-Diagramm wird als eingeklappter Quelltext angezeigt

- Die ausgelieferte Erweiterung enthält keine Zeichen-Engine für TikZ. Diese Anzeige ist normal.
- Für Entwicklung und Erprobung installieren Sie `node-tikzjax` 1.0.5 direkt in der Wurzel eines vertrauenswürdigen Arbeitsbereichs und setzen die Einstellung `lunascapeDocEditor.tikz.runtime` auf `workspace`. Dann wird gezeichnet.
- In der Webversion im Browser wird TikZ nicht gezeichnet.

## Formeln werden als reiner Text angezeigt

- Prüfen Sie die Trennzeichen: `$...$` oder `\(...\)` für Formeln im Text, `$$...$$` oder `\[...\]` für abgesetzte Formeln.
- Ein `$` innerhalb von Inline-Code oder einem Codeblock wird nie zu einer Formel.
- Geldbeträge wie `$5 and $10` werden nicht als Formel behandelt.
- Sehr große Formeln oder Formeln mit vielen Makroerweiterungen werden nicht gezeichnet, wenn sie die Grenzwerte (`maxSize: 50`, `maxExpand: 1000`) überschreiten. Teilen Sie sie auf.

## Ein Diagramm meldet „Kann nicht gezeichnet werden“

- Die Fehlermeldung von Mermaid, Vega-Lite, WaveDrom und anderen benennt das Syntaxproblem. Prüfen Sie den Quelltext im Bearbeitungsfenster mit [Markdown].
- Vega-Lite: Betten Sie die Daten in `data.values` oder `datasets` ein. Daten über externe URLs und Bildmarkierungen sind nicht möglich.
- WaveDrom: Schreiben Sie striktes JSON. Die JavaScript-Schreibweise (Schlüssel ohne Anführungszeichen und Ähnliches) ist nicht möglich.
- Penrose: Verwenden Sie nur `@preset set-theory` am Anfang und die zugelassenen Anweisungen (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „Das erzeugte SVG enthält unsichere Verweise“ / „Das erzeugte SVG überschreitet den Grenzwert“: Diagramme mit Verweisen auf externe Ressourcen und zu große Diagramme werden nicht angezeigt. Verringern Sie den Inhalt oder entfernen Sie die Verweise.

## Ein Bild wird nicht angezeigt

- Geben Sie den Bildpfad relativ zum Dokument an. Bilder außerhalb der Dokumentwurzel werden nicht angezeigt.
- Bei `<img>` geben Sie für `width` nur eine Zahl an (`width="360"`).

## Auf der exportierten Website fehlen die Diagramme

Die Zeichenbibliotheken für TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob und Penrose werden bei der Anzeige geladen. Legen Sie den Ordner `vendor/` zusammen mit der exportierten Website ab.

## Verwandte Themen

- [Formeln schreiben](../03-editing/math.md)
- [Diagramme und Grafiken schreiben](../03-editing/diagrams.md)
- [Bildgröße anpassen](../03-editing/images.md)
