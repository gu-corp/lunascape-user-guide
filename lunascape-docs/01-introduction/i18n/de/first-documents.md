# Erste Dokumente erstellen

In einem Projekt, das noch keinen Dokumentordner hat, können Sie über die Befehlspalette einen ersten Satz von Dokumenten erstellen.

1. Öffnen Sie den Projektordner in VS Code und stufen Sie den Arbeitsbereich als vertrauenswürdig ein.
2. Führen Sie in der Befehlspalette (`⇧⌘P` / `Ctrl+Shift+P`) den Befehl „Lunascape Docs: Dokumentation aus Vorlage erstellen“ aus.
   Wenn der Arbeitsbereich mehrere Ordner enthält, wählen Sie den Arbeitsbereich aus, in dem erstellt werden soll.
3. Wählen Sie den zu erstellenden Aufbau.
   - [Einseitiges Dokument]: nur eine `README.md`. Geeignet für eine kurze Spezifikation, Notizen oder ein einzelnes Erläuterungsdokument.
   - [Dokumentationssatz]: eine Startseite sowie die Einstiegsseiten für `specification/` (Spezifikation), `manual/` (Handbuch) und `help/` (Hilfe).
4. Geben Sie den Titel der Dokumentation ein. Er wird für die README und die Überschriften der einzelnen Dokumente verwendet.
5. Geben Sie den zu erstellenden Dokumentordner ein. Der Pfad ist relativ zum Arbeitsbereich, Standard ist `docs`.
6. Prüfen Sie die Liste der zu erstellenden Dateien und drücken Sie [Erstellen].
   Nach Abschluss der Erstellung wird die neue `README.md` im Viewer geöffnet.

> **Hinweis**
>
> - Vorhandene Dateien werden nicht überschrieben. Wenn auch nur eine der zu erstellenden Dateien bereits vorhanden ist, wird nichts erstellt und der Vorgang abgebrochen.
> - In einem nicht vertrauenswürdigen Arbeitsbereich ist das Erstellen nicht möglich.

> **Tipp**
>
> - Wenn bereits ein Dokumentordner vorhanden ist, entfällt dieser Schritt. Fahren Sie mit [Grundlegende Bedienung](../02-reading/README.md) fort.
> - Wenn die Dokumentation wächst, können Sie über die Registerkarte [Erstellen] der Dokumentwerkzeuge eine Vorlage wählen und Dokumente einzeln hinzufügen.

## Verwandte Themen

- [Ein Dokument aus einer Vorlage erstellen](../04-document-tools/templates.md)
- [Dokumentwurzeln und Dateikonventionen](../04-document-tools/structure.md)
