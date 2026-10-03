# Was ist Lunascape Docs?

Lunascape Docs ist ein Werkzeug, mit dem Sie die Markdown-Dokumente in einem Git-Repository unverändert als „Spezifikations-Website“ nutzen können. Ein vorheriger Build-Schritt, ein Dokumentationsserver oder eine eigene Datenbank ist nicht erforderlich.

## Was Sie tun können

| Zweck | Wichtigste Funktionen |
|---|---|
| Lesen | INDEX (Inhaltsverzeichnis), Links im Text, Navigationspfad, Zurück/Vorwärts, Gliederung der Seite, Filtersuche |
| Anzeigen | Tabellen, Codeblöcke, automatisch eingepasste Bilder, KaTeX-Formeln, Mermaid-, Vega-Lite-, Markmap-, WaveDrom- und Svgbob-Diagramme, eingeklappte Anzeige von Dokumentverwaltungstabellen |
| Schreiben | Wechsel zwischen visueller Bearbeitung und Bearbeitung der Markdown-Quelle; Erstellen, Duplizieren, Umbenennen und Ändern der Reihenfolge über den INDEX |
| Prüfen | Prüfung der Dokumente mit docs-lint, Kontrolle der erforderlichen Dokumente, Kapitel und Begriffe nach dem Standard Pack, Erstellen aus Vorlagen |
| Übersetzen | Erzeugen von Übersetzungsvorschlägen seitenweise oder gesammelt. Gespeichert wird erst nach Ihrer Durchsicht <!-- ai-only --> |
| Mit KI nutzen | Schreibgeschütztes Spezifikationswerkzeug, auf das Agenten in VS Code zugreifen können <!-- ai-only --> |

## Verfügbare Umgebungen

| Umgebung | Verwendung |
|---|---|
| Erweiterung für VS Code | Lesen, Bearbeiten, Prüfen und Übersetzen eines Repositorys auf Ihrem Rechner. Darauf liegt der Schwerpunkt dieser Hilfe |
| Webversion | Lesen von Dokumenten auf GitHub (öffentlich und privat), Entwürfe auf Ihrem Gerät, Lesen lokaler Ordner |
| Chromium-Erweiterung | Öffnet die Webversion in einem Browsertab |

## Grundprinzipien

- **Markdown ist das Original.** Die Dokumente bleiben die Markdown-Dateien, die mit Git verwaltet werden. Lunascape Docs speichert sie nicht in einem anderen Format.
- **Sie speichern selbst.** Bearbeitungen werden nur dann in die Datei geschrieben, wenn Sie auf [Speichern] klicken. Staging und Commit in Git erfolgen nicht automatisch.
- **Dokumente werden auf Ihrem Gerät verarbeitet.** Zum Lesen oder Bearbeiten werden keine Dokumente nach außen gesendet. Nur bei der Übersetzung werden Ziel und Inhalt vorab angezeigt und erst nach Ihrer Zustimmung gesendet.
- **Übersetzungen liegen unter `i18n/<Sprache>/`.** Dokumente in der Standardsprache bleiben an ihrem Ort; Übersetzungen liegen unter demselben relativen Pfad in `i18n/en/` usw.
- **Die KI macht nur Vorschläge.** Übersetzungsvorschläge werden erst gespeichert, nachdem Sie die Änderungen durchgesehen haben. Dokumente werden nie ohne Ihr Wissen geändert. <!-- ai-only -->

## Verwandte Themen

- [Bildschirmbereiche und ihre Funktionen](screen.md)
- [Erweiterung installieren](install.md)
- [Grundlegende Bedienung](../02-reading/README.md)
