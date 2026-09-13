# Was die Web-Version kann

Die Web-Browser-Version von Lunascape Docs ist unter <https://docs.lunascape.org/> veröffentlicht. Ohne Installation lesen Sie Dokumente auf GitHub wie eine Website.

## Funktionen

| Funktion | Inhalt |
|---|---|
| Öffentliche Repositorys lesen | Öffnet die Dokumente eines öffentlichen GitHub-Repositorys ohne Anmeldung |
| Nicht öffentliche Repositorys lesen | Nach der Anmeldung bei GitHub öffnen Sie die Repositorys, für die Sie Leserechte haben |
| Lokale Ordner lesen | Über [Dokumente öffnen] und [Dokumente aus einem lokalen Ordner öffnen] öffnen Sie einen Ordner auf Ihrem Gerät (nur in unterstützten Browsern) |
| Lesefunktionen | INDEX, Links, Verlauf, Filtern, Inhaltsverzeichnis der Seite, Sprachumschaltung, Themenumschaltung. Wie in der VS Code-Version |
| Diagramme und Formeln | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, KaTeX-Formeln |
| Entwürfe | Sie bearbeiten ein Dokument, und die Änderungen bleiben als Entwurf auf Ihrem Gerät. In das Repository wird nichts geschrieben |
| Direktlinks auf Seiten | Eine URL kann Repository und Seite angeben, sodass eine bestimmte Seite direkt geöffnet wird |

## Unterschiede zur VS Code-Version

- Dokumentprüfung, Erstellung aus Vorlagen, Erzeugung von Übersetzungsvorschlägen und Ordnen über den INDEX gibt es in der Web-Version nicht.
- TikZ-Diagramme werden nicht gezeichnet.
- Bearbeitungen werden nicht in das Repository geschrieben, sondern zu Entwürfen auf Ihrem Gerät. Die „Veröffentlichungsanfrage“, die Entwürfe als Pull Request sendet, ist zwar umgesetzt, im öffentlichen Viewer aber nicht aktiviert. Um Änderungen in das Repository zu übernehmen, bearbeiten Sie die Dokumente in der VS Code-Version oder in einem lokalen Klon.

## Verwandte Themen

- [Ein Repository auf GitHub öffnen](open-repository.md)
- [Ein nicht öffentliches Repository lesen](private-repository.md)
- [Entwürfe speichern](drafts.md)
