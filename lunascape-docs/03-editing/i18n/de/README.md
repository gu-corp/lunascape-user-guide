# Ein Dokument bearbeiten

Dokumente lassen sich direkt im Viewer bearbeiten. Der Bearbeitungsbereich bietet eine visuelle Ansicht, in der Sie bearbeiten, was Sie sehen, und eine Markdown-Quelltextansicht; eine Schaltfläche wechselt zwischen beiden.

## Die Bearbeitung beginnen

Drücken Sie eine der folgenden Schaltflächen. Alle öffnen denselben Bearbeitungsbereich.

- [Bearbeiten] unten rechts im Dokument
- [⋯] (Weitere Aktionen) oben rechts im Dokument → [Bearbeiten]
- Das Elementmenü im INDEX → [Bearbeiten]

## Bearbeiten

1. Bearbeiten Sie den Text direkt.
   In der Symbolleiste oben im Bearbeitungsbereich stehen das Absatzformat (Fließtext, Überschrift 1–4, Zitat, Code), [Fett], [Kursiv], [Aufzählung], [Nummerierte Liste], [Link], [Tabelle einfügen], [Bildgröße], [Rückgängig] und [Wiederherstellen] zur Verfügung.
2. Wenn Sie den Markdown-Quelltext direkt bearbeiten möchten, drücken Sie [Markdown].
   Drücken Sie erneut darauf, um zur visuellen Ansicht zurückzukehren. Die zuletzt verwendete Ansicht wird gespeichert und beim nächsten Drücken von [Bearbeiten] wiederhergestellt.
3. Drücken Sie [Speichern].
   Die Markdown-Datei wird geschrieben, und die Leseansicht kehrt zurück. Zum Abbrechen drücken Sie [Abbrechen].

> **Hinweis**
>
> - Beim Speichern wird nur die Datei geschrieben. Das Stagen und Committen in Git erfolgt nicht automatisch.
> - Formeln sowie Diagramme wie Mermaid, TikZ und Vega-Lite werden in der visuellen Ansicht gerendert dargestellt. Um ihren Inhalt zu ändern, wechseln Sie zu [Markdown].
> - Dokumente mit MDX-spezifischer Syntax (Komponenten, `import` und Ähnliches) werden nur in der Markdown-Ansicht bearbeitet, damit diese Syntax erhalten bleibt.
> - Das Front Matter (der Block zwischen den `---`-Zeilen am Anfang) bleibt erhalten, wenn Sie in der visuellen Ansicht bearbeiten.

> **Tipp**
>
> - Mit [In VS Code öffnen] öffnen Sie die Datei im normalen Texteditor. Speichern Sie dort, wird die Anzeige im Viewer automatisch aktualisiert.
> - Wenn die Schaltfläche [Bearbeiten] nicht angezeigt werden soll, schalten Sie unter [Anzeigeeinstellungen] die Option [Bearbeiten-Schaltfläche] aus. Um sie im gesamten Projekt auszublenden, setzen Sie in `lunascape-docs.json` den Wert `editor.showEditButton` auf `false`.
> - Die Standardansicht beim Öffnen (visuell oder Markdown) ändern Sie mit der Einstellung `lunascapeDocEditor.editor.defaultMode` oder mit `editor.defaultMode` in `lunascape-docs.json`.

## Verwandte Themen

- [Dokumente und Ordner erstellen und ordnen](organize.md)
- [Die Größe von Bildern anpassen](images.md)
- [Formeln schreiben](math.md)
- [Diagramme und Grafiken erstellen](diagrams.md)
