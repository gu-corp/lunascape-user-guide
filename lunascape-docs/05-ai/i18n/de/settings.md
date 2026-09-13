# KI-Einstellungen

Wählen Sie die KI und das Modell, an die Sie Ihre Arbeit übergeben. Dieser Bildschirm verwendet eigene Auswahlmenüs, nicht die Schnellauswahl von VS Code.

1. Drücken Sie [Dokumentwerkzeuge] → Registerkarte [KI] → [KI-Einstellungen …].
2. Wählen Sie unter [Anbieter] einen Anbieter.
   Anbieter, die in dieser Umgebung nicht verfügbar sind, werden nicht auswählbar und mit Begründung angezeigt.
3. Wählen Sie unter [Modell] ein Modell. Die Auswahl ändert sich je nach Anbieter.
4. Schließen Sie den Bildschirm. Die Auswahl wird pro Benutzer gespeichert und beim nächsten Mal wieder verwendet.

## Anbieter

| Anbieter | Form | Erkennung |
|---|---|---|
| Claude Code | Sitzung | Vorhandensein des Befehls `claude` |
| Codex | Sitzung | Vorhandensein des Befehls `codex` |
| Sprachmodelle von VS Code | API | Modelle, die bei der VS Code Language Model API registriert sind |
| Anthropic API | API | Registrierung eines API-Schlüssels |
| OpenAI-kompatible API | API | Registrierung von API-Schlüssel und Endpunkt |

Ein **Sitzungs**-Anbieter liest und schreibt Dateien selbst und führt auch die Dokumentprüfung selbst aus. Die Ergebnisse werden direkt in den Arbeitsbaum geschrieben und im Git-Diff geprüft.

Ein **API**-Anbieter gibt das Markdown eines Dokuments zurück; die Erweiterung zeigt die Unterschiede an und speichert dann.

## Einen API-Schlüssel registrieren

Die Anthropic API und OpenAI-kompatible APIs lassen sich verwenden, sobald ein API-Schlüssel registriert ist.

1. Wählen Sie unter [Anbieter] den Anbieter aus, für den Sie den Schlüssel registrieren. Das Eingabefeld für den API-Schlüssel erscheint.
2. Geben Sie den [API-Schlüssel] ein. Bei einer OpenAI-kompatiblen API geben Sie zusätzlich den [Endpunkt] ein (Beispiel: `https://api.openai.com/v1`).
3. Drücken Sie [Speichern]. Es wird „Schlüssel registriert“ angezeigt.

> **Hinweis**
>
> - Der Schlüssel wird im SecretStorage von VS Code gespeichert und nicht erneut angezeigt. Er wird auch nicht in `settings.json` oder in ein Dokument geschrieben. Mit [Schlüssel löschen] können Sie ihn entfernen.
> - Die Modellliste wird mit dem registrierten Schlüssel von den jeweiligen Diensten abgerufen. Solange der Abruf nicht möglich ist, wird eine bekannte Liste angezeigt.
> - Mit einem API-Anbieter lassen sich nur „Diese Seite übersetzen“ und „Diese Seite korrekturlesen“ ausführen. Das Durchlaufen mehrerer Dokumente und das Erstellen von Dokumenten führen Sie mit einem Sitzungs-Anbieter aus.

> **Tipp**
>
> Wenn kein Anbieter gefunden wird, installieren Sie Claude Code oder Codex oder registrieren Sie einen API-Schlüssel. Öffnen Sie [KI-Einstellungen …] erneut, dann wird der Anbieter erkannt.

## Verwandte Themen

- [Arbeit an eine KI übergeben](README.md)
- [Übersicht der VS Code-Einstellungen](../08-reference/settings.md)
