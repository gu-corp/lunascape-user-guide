# Grundlegende Bedienung

Die grundlegenden Schritte vom Öffnen der Dokumente bis zu der Seite, die Sie lesen möchten.

## Dokumente öffnen

1. Öffnen Sie das Repository in VS Code.
2. Führen Sie in der Befehlspalette (`⇧⌘P` / `Ctrl+Shift+P`) den Befehl „Lunascape Docs: Spezifikations-Viewer öffnen" aus.
   Die nächstgelegene Dokumentwurzel (standardmäßig der Ordner `docs`) wird gefunden, und ihre Startseite wird angezeigt.

> **Hinweis**
>
> - Klicken Sie im Explorer mit der rechten Maustaste auf eine Markdown-Datei und wählen Sie [Lunascape Docs: Im Spezifikations-Viewer öffnen], um mit dieser Datei zu beginnen.
> - Wenn Sie eine Markdown-Datei öffnen, die zu keiner Dokumentwurzel gehört, wird deren Ordner als vorübergehende Dokumentwurzel angezeigt.

## Zwischen Seiten wechseln

| Aktion | Vorgehen |
|---|---|
| Aus dem Inhaltsverzeichnis öffnen | Im INDEX links auf einen Dokumentnamen klicken |
| Einem Link folgen | Im Text auf einen Link klicken. Er wird in derselben Ansicht geöffnet |
| Im Verlauf navigieren | [Zurück] und [Vor] in der Symbolleiste oder `Alt`+`←` / `Alt`+`→` |
| Zur Startseite zurückkehren | [Startseite der Spezifikation] in der Symbolleiste |
| Eine Ebene nach oben | [Übergeordneter INDEX] in der Symbolleiste oder ein Eintrag im Navigationspfad |
| Innerhalb der Seite navigieren | Rechts unter „Auf dieser Seite" auf eine Überschrift klicken |

## Ein Dokument finden

Geben Sie oberhalb des INDEX in [Dokumente filtern] ein Wort ein, damit nur die Dokumente angezeigt werden, deren Name dazu passt. Löschen Sie die Eingabe, um wieder alle anzuzeigen.

## Inhalte aktualisieren

Wenn Sie eine Markdown-Datei im Editor von VS Code speichern, wird die Anzeige automatisch aktualisiert. Nach Änderungen mit einem externen Werkzeug klicken Sie in der Symbolleiste auf [Neu laden].

> **Achtung**
>
> - Externe Links im Text (`https://` und Ähnliches) werden im Standardbrowser geöffnet. Links auf Dateien außerhalb der Dokumentwurzel werden nicht geöffnet.
> - Die angezeigten Dokumente werden auf Ihrem Gerät verarbeitet. Zum Lesen wird kein Dokument nach außen übertragen.

## Verwandte Themen

- [INDEX verwenden](index-panel.md)
- [Dokumentwurzel wechseln](roots.md)
- [Ein Dokument bearbeiten](../03-editing/README.md)
