# Bearbeiten, Speichern oder Umsortieren nicht möglich

## Die Schaltfläche [Bearbeiten] fehlt

- [Bearbeiten-Schaltfläche] ist unter [Anzeigeeinstellungen] ausgeschaltet. Schalten Sie sie ein, oder verwenden Sie [⋯] → [Bearbeiten] oben rechts im Dokument bzw. das Eintragsmenü im INDEX → [Bearbeiten].
- Dasselbe gilt, wenn `editor.showEditButton` in `lunascape-docs.json` auf `false` steht.
- Während die Hilfe angezeigt wird, ist das Bearbeiten nicht möglich. Schließen Sie die Hilfe.

## Umschalten auf die visuelle Ansicht nicht möglich

„Dieses Dokument enthält MDX-Syntax und kann nicht im normalen Bearbeitungsfenster geöffnet werden“: Dokumente mit MDX-eigener Syntax (Komponenten, `import` und Ähnliches) werden nur in der Markdown-Ansicht bearbeitet, damit diese Syntax erhalten bleibt.

## Formeln oder Diagramme lassen sich nicht direkt bearbeiten

Die visuelle Ansicht zeigt das gezeichnete Ergebnis. Drücken Sie im Bearbeitungsfenster auf [Markdown] und bearbeiten Sie den Quelltext.

## Umsortieren oder Ziehen nicht möglich

- Während einer Filterung, während der Bearbeitung eines Dokuments und während eine andere INDEX-Aktion ausgeführt wird, ist das Umsortieren nicht möglich.
- In einem nicht vertrauenswürdigen Arbeitsbereich stehen die Aktionen zum Erstellen, Organisieren und Löschen nicht zur Verfügung. Stufen Sie den Arbeitsbereich in VS Code als vertrauenswürdig ein.
- „Der INDEX wurde aktualisiert. Bitte ziehen Sie erneut.“: Soeben wurde eine andere Änderung übernommen. Führen Sie die Aktion erneut aus.
- Die Startseite (`README.md` in der Wurzel) kann nicht verschoben werden.

## Es wird „Es sind ungespeicherte Änderungen vorhanden“ angezeigt

Die betreffende Datei wird gerade im Editor von VS Code bearbeitet. Speichern oder verwerfen Sie die Änderungen zuerst, und versuchen Sie es dann erneut.

## Umbenennen nicht möglich

Die folgenden Namen sind nicht zulässig.

- Namen, die mit `.` beginnen, `i18n` sowie unter Windows reservierte Namen (`CON` und Ähnliche)
- Namen, die auf einen Punkt oder ein Leerzeichen enden, sowie Namen mit Steuerzeichen oder mit Zeichen, die in Dateinamen nicht zulässig sind
- Namen, die im selben Ordner bereits vorhanden sind (einschließlich Namen, die sich nur in der Groß- und Kleinschreibung unterscheiden)
- Dokumentnamen ohne Markdown-Dateierweiterung

## Gespeicherte Änderungen erscheinen nicht in Git oder werden nicht committet

Lunascape Docs schreibt nur in die Datei. Es führt in Git weder das Staging noch einen Commit aus. Prüfen Sie die Quellcodeverwaltungsansicht in VS Code und committen Sie bei Bedarf.

## Verwandte Themen

- [Ein Dokument bearbeiten](../03-editing/README.md)
- [Dokumente und Ordner erstellen und organisieren](../03-editing/organize.md)
- [Die Reihenfolge der Dokumente ändern](../03-editing/reorder.md)
