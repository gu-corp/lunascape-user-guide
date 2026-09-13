# Arbeit an eine KI übergeben

Lunascape Docs ruft kein Sprachmodell auf. Es stellt **Kontext, Werkzeuge und Prüfungen** bereit und überlässt das Übersetzen, Korrekturlesen und Verfassen der KI, die Sie verwenden.

## Der Gedanke dahinter

| Was das Produkt bereitstellt | Inhalt |
|---|---|
| Kontext | Die Konventionen der Dokumente (wo Übersetzungen liegen, Front Matter, der Dokumentstandard, das Glossar) und die Position des Zieldokuments |
| Arbeitswerkzeuge | Das Verzeichnis nicht übersetzter und veralteter Dokumente, Lesen und Schreiben von Dokumenten, Erstellen aus Vorlagen |
| Prüfung im Nachgang | Die Prüfung durch docs-lint sowie die Unterschiede bei Abdeckung und Aktualität |

Die Anweisung enthält keinen Dokumenttext: Die KI liest die Dateien selbst, schreibt selbst und prüft selbst.

## Arbeit übergeben

1. Drücken Sie in der Symbolleiste auf [Dokumentwerkzeuge] und öffnen Sie die Registerkarte [AI].
2. Wählen Sie unter [Aufgabe] die Arbeit aus, die Sie übergeben möchten.
3. Füllen Sie die erforderlichen Angaben aus (Zielsprache, Thema).
4. Drücken Sie auf [Diese Arbeit übergeben].
   Ein Terminal von VS Code öffnet sich, und die gewählte KI nimmt die Anweisung entgegen und beginnt mit der Arbeit.

> **Hinweis**
>
> Eine Sitzung von Claude Code bringt die Arbeitswerkzeuge mit (den MCP-Server `lunascape-docs`). Die Sitzung kann die Liste der nicht übersetzten und veralteten Dokumente selbst abrufen, docs-lint ausführen und die Aktualität nach der Übersetzung selbst eintragen.

## Das Ergebnis prüfen

| Form des Anbieters | Wo das Ergebnis landet |
|---|---|
| Sitzungsbasiert (Claude Code, Codex) | Schreibt direkt in den Arbeitsbaum. **Prüfen Sie es im Git-Unterschied** |
| API-basiert (Sprachmodelle von VS Code, Anthropic, OpenAI-kompatibel) | Liefert Vorschläge für jeweils ein Dokument. Prüfen Sie sie mit [Unterschied öffnen] und schreiben Sie sie mit [Speichern] |

### Einen Vorschlag eines API-Anbieters prüfen

Bei der Ausführung über einen API-Anbieter erscheint der Vorschlag auf der Registerkarte [AI].

1. Drücken Sie auf [Unterschied öffnen] und vergleichen Sie ihn mit dem aktuellen Inhalt.
2. Wenn er passt, drücken Sie auf [Speichern]. Bei einer Übersetzung wird auch die Aktualität eingetragen. Zum Verwerfen drücken Sie auf [Verwerfen].
   Um eine laufende Generierung zu beenden, drücken Sie auf [Abbrechen].

> **Achtung**
>
> - Lunascape Docs führt in Git weder das Vormerken noch das Committen durch. Prüfen Sie Änderungen stets im Unterschied.
> - In einem Arbeitsbereich, dem Sie nicht vertrauen, sowie bei der vorübergehenden Anzeige eines Ordners außerhalb der Dokumentwurzel lässt sich keine Arbeit übergeben.

## Verwandte Themen

- [Verfügbare Arbeiten](tasks.md)
- [AI-Einstellungen](settings.md)
- [Verzeichnis und Einträge](ledger.md)
