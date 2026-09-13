# Nutzung durch KI-Agenten

Die Erweiterung registriert das schreibgeschützte Language Model Tool `lunascape_getDocsSpecification` bei VS Code. Wird ein kompatibler VS-Code-Agent zu Funktionen, Einstellungen oder Dokumentkonventionen von Lunascape Docs befragt, kann er über dieses Werkzeug den Inhalt dieser Hilfe (die allgemeine Spezifikation) abrufen.

## Verwendung

Stellen Sie Ihre Frage im VS-Code-Chat mit `#lunascapeDocs`, oder fragen Sie einfach nach den Einstellungen oder dem Dokumentaufbau von Lunascape Docs.

```text
#lunascapeDocs How do I enable English translations in lunascape-docs.json?
```

## Argumente des Werkzeugs

| Argument | Inhalt |
|---|---|
| `topic` | Der abzurufende Abschnitt: `all`, `usage` (Grundlegende Bedienung), `structure` (Dokumentwurzeln und Dateikonventionen), `editing` (Ein Dokument bearbeiten), `configuration` (Projekteinstellungen), `security` (Sicherheit und Speichergrenzen) oder `ai` (Nutzung durch KI-Agenten) |
| `locale` | Die Sprache der Hilfe (ein Sprachtag der mitgelieferten Hilfe, etwa `ja` oder `en`). Wird es weggelassen, gilt die Anzeigesprache von VS Code, andernfalls wird die japanische Hilfe zurückgegeben |

> **Hinweis**
>
> - Das Werkzeug sendet keine Dokumentinhalte nach außen.
> - Das Werkzeug gibt keine Arbeitsbereichsnamen oder lokalen Pfade zurück.
> - Das Werkzeug verändert keine Dateien.
> - Es lässt sich auch ohne `AGENTS.md` von kompatiblen VS-Code-Agenten nutzen. An andere KI-Clients, die die Werkzeug-API der Erweiterung nicht verwenden, wird es nicht automatisch weitergegeben.

## Verwandte Themen

- [Hilfe anzeigen](../02-reading/help.md)
- [Sicherheit und Speichergrenzen](security.md)
