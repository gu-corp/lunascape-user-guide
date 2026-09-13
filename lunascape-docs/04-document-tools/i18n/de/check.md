# Dokumente prüfen

Mit docs-lint lassen sich Überschriftenaufbau, defekte Links, fehlende Pflichtdokumente und -abschnitte, uneinheitliche Terminologie, die Stimmigkeit von Anforderungs-IDs und weiteres prüfen. Eine Prüfung erfasst immer die gesamte Dokumentwurzel.

## Eine Prüfung ausführen

1. Drücken Sie in der Symbolleiste [Dokumentwerkzeuge] und öffnen Sie die Registerkarte [Prüfung].
2. Drücken Sie [Dokumentwurzel prüfen].
   Sie können die Prüfung auch über „Lunascape Docs: Dokumentwurzel prüfen“ in der Befehlspalette ausführen.
3. Sehen Sie die Liste der Meldungen durch.

## Die Ergebnisse lesen

- Mit [Dieses Dokument] / [Alle] über der Liste schalten Sie den angezeigten Bereich um. Der Umfang der Prüfung selbst bleibt immer die gesamte Dokumentwurzel.
- Meldungen haben vier Stufen: „Fehler“, „Warnung“, „Information“ und „Vorschlag“. In der Symbolleiste zeigt [Dokumentwerkzeuge] die Anzahl der Fehler und Warnungen an.
- Wenn Sie eine Meldung drücken, wird die zugehörige Stelle in der Markdown-Quelle im Editor von VS Code geöffnet.
- Meldungen, die die gesamte Dokumentwurzel betreffen (etwa ein fehlendes Testdokument), erscheinen als Eintrag „Gesamte Dokumentwurzel“ und haben keine Position.
- Dieselben Meldungen erscheinen auch im Bereich „Probleme“ von VS Code.

## Was geprüft wird

Wenn Sie [Regeln prüfen und ändern] drücken, erscheint die Liste der aktiven Prüfungen mit ihrem jeweiligen Zweck. Die wichtigsten Punkte sind:

| Punkt | Inhalt |
|---|---|
| Überschriftenaufbau | Es gibt genau eine H1, und die Überschriftenebenen überspringen keine Stufe |
| Interne Links | Die verlinkten Dokumente sind vorhanden und führen nicht aus der Dokumentwurzel hinaus |
| Sprache der Codeblöcke | In den Codeblöcken ist ein Sprachname angegeben |
| Erforderliche Ordner und Dokumente | Die vom Profil des Standard Pack geforderten Ordner und Dokumente sind vollständig vorhanden |
| Erforderliche Abschnitte im Dokument | Je Dokumentart sind die erforderlichen Abschnitte vorhanden |
| Einheitliche Terminologie | Zu vermeidende Ausdrücke werden erkannt und die empfohlenen Begriffe vorgeschlagen |
| Benennung und Dopplung von Anforderungs-IDs | Die Anforderungs-IDs folgen der Benennungsregel und sind nicht doppelt definiert |
| Stimmigkeit der Verweise auf Anforderungs-IDs | Die aus Entwurf, Tests und Statustabellen referenzierten Anforderungs-IDs sind vorhanden |
| Zuordnung von Anforderungen und Tests | Die Anforderungs-IDs werden aus Testdokumenten referenziert |

Welche Punkte aktiv sind, ergibt sich aus dem in `lunascape-docs.json` gewählten Standard Pack samt Profil sowie aus `docs-lint.config.json`.

> **Hinweis**
>
> - Wenn Sie ein Dokument oder eine Einstellung ändern, wird das vorherige Ergebnis auf „Erneute Prüfung erforderlich“ gesetzt. Nichts gilt automatisch als bestanden. Drücken Sie erneut [Dokumentwurzel prüfen].
> - Nicht gespeicherte Änderungen fließen nicht in die Prüfung ein. Speichern Sie zuerst.
> - Die Prüfung läuft lokal auf dem Gerät und deterministisch ab. Ergebnisse von KI-Bewertungen oder Übersetzungen mischen sich nicht in die Prüfergebnisse.

## Verwandte Themen

- [Prüfregeln ändern](rules.md)
- [Projekteinstellungen](project-configuration.md)
- [Prüfung, Erstellung oder Übersetzung schlägt fehl](../07-troubleshooting/tools.md)
