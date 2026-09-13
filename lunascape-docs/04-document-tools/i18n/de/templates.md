# Ein Dokument aus einer Vorlage erstellen

Im Reiter [Erstellen] der Dokumentwerkzeuge wählen Sie eine Vorlage, sehen den Inhalt in der Vorschau und erstellen dann ein neues Dokument.

1. Drücken Sie [Dokumentwerkzeuge] in der Symbolleiste und öffnen Sie den Reiter [Erstellen].
2. Drücken Sie [Aus Vorlage erstellen] und wählen Sie eine Vorlage.
3. Füllen Sie die Eingabefelder aus (Titel, Zusammenfassung und so weiter). Pflichtfelder sind mit „Erforderlich“ gekennzeichnet.
4. Geben Sie den Speicherort als Pfad relativ zur Dokumentwurzel ein (zum Beispiel `03-design/api.md`).
5. Drücken Sie [Vorschau] und prüfen Sie das erzeugte Markdown.
6. Drücken Sie [Mit diesem Inhalt erstellen].
   Das Dokument wird erstellt und im Betrachter angezeigt. Anschließend wird die gesamte Dokumentwurzel geprüft.

## Verfügbare Vorlagen

| Vorlage | Inhalt |
|---|---|
| Einseitiges Dokument | Eine kurze Spezifikation, Notizen oder ein eigenständiger Erklärungstext in einer Datei |
| Spezifikation, Handbuch, Hilfe | Eine Datei mit einer allgemeinen Kapitelgliederung, die sich für Spezifikationen, Handbücher und Hilfen eignet |
| Vorlagen des Standard Pack | Wenn in `lunascape-docs.json` ein Standard Pack ausgewählt ist, kommen die Dokumentarten hinzu, die dieses Profil zulässt (Anforderungsdokument, Entwurfsdokument und so weiter) |

> **Hinweis**
>
> - Zum Erstellen ist ein vertrauenswürdiger Arbeitsbereich erforderlich.
> - Vorhandene Dateien werden nicht überschrieben. Wenn am Speicherort bereits ein Dokument mit demselben Namen liegt, ist das Erstellen nicht möglich.
> - Der Speicherort braucht die Erweiterung `.md` oder `.mdx`. Unterhalb von `i18n` (dort liegen die Übersetzungen) kann nichts erstellt werden.
> - Drücken Sie nach einer Änderung der Eingaben erneut [Vorschau], bevor Sie erstellen.

> **Tipp**
>
> In einem Projekt ohne Dokumentordner erstellen Sie den ersten Satz mit „Lunascape Docs: Dokumentation aus Vorlage erstellen“ in der Befehlspalette. Siehe [Die ersten Dokumente erstellen](../01-introduction/first-documents.md).

## Verwandte Themen

- [Die Dokumentwerkzeuge verwenden](README.md)
- [Prüfregeln ändern](rules.md)
