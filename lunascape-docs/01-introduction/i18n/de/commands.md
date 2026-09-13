# Befehlsübersicht

Geben Sie in der Befehlspalette (`⇧⌘P` / `Ctrl+Shift+P`) „Lunascape Docs“ ein, um die folgenden Befehle auszuführen.

| Befehl | Funktion |
|---|---|
| Lunascape Docs: Spezifikationsanzeige öffnen | Öffnet die nächstgelegene Dokumentwurzel in der Anzeige. Lesen, Bearbeiten, Prüfen und Übersetzen erfolgen in dieser Ansicht |
| Lunascape Docs: In Spezifikationsanzeige öffnen | Zeigt die im Editor geöffnete Markdown-Datei in der Anzeige an |
| Lunascape Docs: Dokument aus Vorlage erstellen | Erstellt in einem Projekt ohne Dokumentordner einen ersten Satz von Dokumenten |
| Lunascape Docs: Dokumentwurzel prüfen | Prüft die gesamte Dokumentwurzel mit docs-lint und zeigt die Ergebnisse in den Dokumentwerkzeugen und im Bereich „Probleme“ an |
| Lunascape Docs: Hilfe öffnen | Öffnet diesen Hilfeleitfaden |

## Bedienung über den Explorer

Klicken Sie im Explorer mit der rechten Maustaste auf eine Datei `.md`, `.markdown` oder `.mdx` und wählen Sie [Lunascape Docs: In Spezifikationsanzeige öffnen].

> **Hinweis**
>
> Damit Markdown-Dateien auch beim normalen Öffnen in Lunascape Docs angezeigt werden, fügen Sie den Einstellungen des Arbeitsbereichs eine Editorzuordnung hinzu.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## Einführung

Über die Einführung „Erste Schritte mit Lunascape Docs“ im Menü [Hilfe] → „Willkommen“ von VS Code können Sie die ersten Schritte der Reihe nach ausprobieren.

## Verwandte Themen

- [Grundlegende Bedienung](../02-reading/README.md)
- [Tastaturbedienung](../08-reference/keyboard.md)
