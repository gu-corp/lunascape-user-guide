# Das Register und seine Datensätze

Das Register oben im Tab [AI] zeigt den Übersetzungsstand je unterstützter Sprache. Es ist auch ohne KI nützlich: Es zeigt, was fehlt.

| Anzeige | Bedeutung |
|---|---|
| Nicht übersetzt | Anzahl der Dokumente, zu denen es noch keine Übersetzung gibt |
| Veraltet | Anzahl der Dokumente, zu denen es eine Übersetzung gibt, deren Originaldokument aber neuer ist als der Datensatz |
| Übersetzt | Anzahl der Übersetzungen, die dem Originaldokument folgen |

Das Register wird durch Durchlaufen der Dokumentwurzel berechnet. Weder eine KI noch ein Sprachmodell ist daran beteiligt.

## Die Übersetzungsdatensätze aktualisieren

Um „Veraltet“ feststellen zu können, braucht es einen Datensatz des Originaldokuments und der Übersetzung zum Zeitpunkt der Übersetzung. Session-basierte KI schreibt Dateien direkt, daher entsteht der Datensatz nicht von selbst.

1. Wenn die Übersetzung fertig ist und Sie den Inhalt geprüft haben, drücken Sie [Übersetzungsdatensätze aktualisieren].
2. Übersetzungen ohne Datensatz werden als zum aktuellen Originaldokument gehörend aufgezeichnet.

Sitzungen von Claude Code und das Speichern über API-Anbieter legen den Datensatz automatisch an (eine Sitzung wird angewiesen, das MCP-Werkzeug `record_translation_freshness` zu verwenden). Die Schaltfläche brauchen Sie, wenn Sie mit Codex oder im Chat von VS Code übersetzt haben.

Von da an wird die Übersetzung als „Veraltet“ angezeigt, sobald Sie das Originaldokument ändern.

> **Hinweis**
>
> - Übersetzungen, zu denen bereits ein Datensatz vorliegt, werden nicht überschrieben. So geht ein bestehender Zustand „Veraltet“ nicht verloren.
> - Die Datensätze werden in `.lunascape-docs/translation-freshness.json` gespeichert. Gespeichert werden nur relative Pfade, Sprachen, Hashwerte des Inhalts und ein Zeitstempel – niemals der Text selbst.

## Verwandte Themen

- [Übergebbare Arbeiten](tasks.md)
- [In einer anderen Sprache lesen](../02-reading/languages.md)
