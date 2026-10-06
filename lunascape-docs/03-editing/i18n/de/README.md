# Ein Dokument bearbeiten

Dokumente lassen sich direkt in der Ansicht bearbeiten. Der Editor bietet eine visuelle Ansicht, in der Sie bearbeiten, was Sie sehen, und eine Markdown-Quellansicht; eine einzige Schaltfläche schaltet zwischen ihnen um.

## Bearbeitung beginnen

Drücken Sie eine der folgenden Möglichkeiten. Alle öffnen denselben Editor.

- [Bearbeiten] unten rechts im Dokument
- [⋯] (Weitere Aktionen) oben rechts im Dokument → [Bearbeiten]
- Das Eintragsmenü im INDEX → [Bearbeiten]

## Bearbeiten

1. Bearbeiten Sie den Text direkt.
   Die Symbolleiste am oberen Rand des Editors bietet das Absatzformat (Fließtext, Überschriften 1–4, Zitat, Code), [Fett], [Kursiv], [Aufzählung], [Nummerierte Liste], [Link], [Tabelle einfügen], [Bildgröße], [Rückgängig] und [Wiederherstellen].
2. Um die Markdown-Quelle direkt zu bearbeiten, drücken Sie [Markdown].
   Drücken Sie erneut, um zur visuellen Ansicht zurückzukehren. Die zuletzt verwendete Ansicht wird gespeichert und wiederhergestellt, wenn Sie das nächste Mal [Bearbeiten] drücken.
3. Drücken Sie [Speichern] (auch mit Ctrl+S / ⌘S möglich).
   Die Markdown-Datei wird geschrieben und die Ansicht kehrt zum Lesemodus zurück. Um die Bearbeitung abzubrechen und zum zuletzt gespeicherten Stand zurückzukehren, drücken Sie [Bearbeitungen verwerfen].

## Immer im Editor beginnen (Bearbeitungsmodus)

Drücken Sie [Bearbeitungsmodus] in der Symbolleiste, um ihn einzuschalten: Von da an öffnet sich jedes Dokument im Editor, so wie ein Notizblock. Verwenden Sie ihn, wenn Sie schreiben statt lesen.

- Solange er eingeschaltet ist, schließt [Speichern] den Editor nicht. [Bearbeitungen verwerfen] kehrt zum zuletzt gespeicherten Stand zurück und lässt den Editor geöffnet.
- Drücken Sie erneut, um ihn auszuschalten und zum Lesemodus zurückzukehren. Die Ein-/Aus-Einstellung wird pro Benutzer gespeichert.
- Bei einer Dokumentwurzel, in die nicht geschrieben werden kann (etwa eine schreibgeschützte GitHub-Quelle), wird er nicht angezeigt.

## Nicht gespeicherte Bearbeitungen

Bearbeitungen, die Sie nicht gespeichert haben, werden automatisch auf diesem Gerät aufbewahrt. Sie gehen nicht verloren, wenn Sie zu einem anderen Dokument wechseln oder den Tab oder das Fenster schließen.

- [Nicht gespeichert] im Editor bedeutet, dass sich der Text vom zuletzt gespeicherten Stand unterscheidet.
- Wenn Sie dasselbe Dokument das nächste Mal öffnen, wird von den aufbewahrten Bearbeitungen aus fortgesetzt, und es wird darauf hingewiesen. Falls sich das Dokument selbst seither geändert hat, wird auch das angezeigt; mit [Bearbeitungen verwerfen] kehren Sie zur neuesten Fassung zurück.
- Die aufbewahrten Bearbeitungen verschwinden mit [Speichern] oder [Bearbeitungen verwerfen]. Es wurde nichts gespeichert, daher erscheinen sie weder in Git noch unter den Entwürfen.

> **Hinweis**
>
> - Das Speichern schreibt nur die Datei. Das Stagen und Committen in Git geschieht nie automatisch.
> - Formeln und Diagramme wie Mermaid, TikZ und Vega-Lite werden in der visuellen Ansicht gerendert dargestellt. Wechseln Sie zu [Markdown], um ihren Inhalt zu ändern.
> - Dokumente mit MDX-spezifischer Syntax (Komponenten, `import` und dergleichen) werden nur in der Markdown-Ansicht bearbeitet, um diese Syntax zu erhalten.
> - Front Matter (der Block zwischen den `---`-Zeilen am Anfang) bleibt erhalten, wenn Sie in der visuellen Ansicht bearbeiten.

> **Tipp**
>
> - [In VS Code öffnen] öffnet die Datei im normalen Texteditor. Wenn Sie dort speichern, wird die Ansicht automatisch aktualisiert.
> - Um die [Bearbeiten]-Schaltfläche auszublenden, schalten Sie [Bearbeiten-Schaltfläche] in den [Anzeigeeinstellungen] aus. Um sie für das gesamte Projekt auszublenden, setzen Sie in `lunascape-docs.json` `editor.showEditButton` auf `false`.
> - Die anfänglich geöffnete Ansicht (visuell oder Markdown) legen Sie standardmäßig über die Einstellung `lunascapeDocEditor.editor.defaultMode` oder über `editor.defaultMode` in `lunascape-docs.json` fest.

## Verwandte Themen

- [Dokumente und Ordner erstellen und ordnen](organize.md)
- [Bildgrößen anpassen](images.md)
- [Formeln schreiben](math.md)
- [Diagramme und Grafiken erstellen](diagrams.md)
