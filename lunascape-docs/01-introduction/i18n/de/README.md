# Was Lunascape Docs ist

Lunascape Docs behandelt die Markdown-Dokumente in einem Git-Repository unverändert als „Spezifikationswebsite". Ein vorheriger Build, ein Dokumentserver oder eine eigene Datenbank sind nicht nötig.

## Was Sie tun können

| Zweck | Wichtigste Funktionen |
|---|---|
| Lesen | INDEX (Inhaltsverzeichnis), Links im Text, Navigationspfad, Zurück/Vorwärts, Inhalt der Seite, Filtersuche |
| Ansehen | Tabellen, Codeblöcke, automatisch eingepasste Bilder, KaTeX-Formeln, Diagramme mit Mermaid, Vega-Lite, Markmap, WaveDrom und Svgbob, eingeklappte Dokumentverwaltungstabellen |
| Schreiben | Umschalten zwischen visueller Bearbeitung und Markdown-Quelltext; Erstellen, Duplizieren, Umbenennen und Umsortieren über den INDEX |
| Prüfen | Dokumentprüfung mit docs-lint, Abgleich der vorgeschriebenen Dokumente, Kapitel und Begriffe nach Standard Pack, Erstellen aus Vorlagen |
| Übersetzen | Übersetzungsvorschläge für eine einzelne Seite oder für mehrere auf einmal. Vor dem Speichern prüfen <!-- ai-only --> |
| Aus KI nutzen | Ein schreibgeschütztes Spezifikationswerkzeug, das Agenten in VS Code abfragen können <!-- ai-only --> |

## Verfügbare Umgebungen

| Umgebung | Verwendung |
|---|---|
| VS Code-Erweiterung | Lesen, Bearbeiten, Prüfen und Übersetzen des Repositorys auf Ihrem Gerät. Im Mittelpunkt dieser Hilfe |
| Webbrowser-Version | Lesen von Dokumenten auf GitHub (öffentlich und nicht öffentlich), Entwürfe auf dem Gerät, Ansehen eines lokalen Ordners |
| Chromium-Erweiterung | Öffnet die Webbrowser-Version in einem Browser-Tab |
| Lunascape-Browser | Wird dasselbe Dokumentmodell einbetten |

## Grundgedanken

- **Markdown ist das Original.** Die Dokumente bleiben die von Git verwalteten Markdown-Dateien. Lunascape Docs wandelt sie nicht in ein anderes Format um und bewahrt keine Kopie auf.
- **Das Speichern nehmen Sie vor.** Bearbeitungen werden nur dann in die Datei geschrieben, wenn Sie [Speichern] drücken. Git-Staging und Commits geschehen nicht automatisch.
- **Dokumente werden auf Ihrem Gerät verarbeitet.** Zum Lesen oder Bearbeiten wird kein Dokument nach außen gesendet. Nur bei der Übersetzung werden Ziel und Inhalt vorab angezeigt und erst nach Ihrer Zustimmung gesendet.
- **Übersetzungen liegen unter `i18n/<Sprache>/`.** Dokumente in der Standardsprache bleiben an ihrem Platz, Übersetzungen liegen unter demselben relativen Pfad in `i18n/en/` und so weiter.
- **Die KI macht nur Vorschläge.** Übersetzungsvorschläge werden gespeichert, nachdem Sie die Unterschiede geprüft haben. Dokumente werden nie stillschweigend umgeschrieben. <!-- ai-only -->

## Verwandte Themen

- [Die Teile des Bildschirms und ihre Aufgaben](screen.md)
- [Die Erweiterung installieren](install.md)
- [Grundlegende Bedienung](../02-reading/README.md)
