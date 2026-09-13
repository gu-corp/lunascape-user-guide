# Dokumente und Ordner erstellen und organisieren

Über das Eintragsmenü im INDEX können Sie Dokumente und Ordner erstellen, duplizieren, umbenennen und löschen. Die Eingabe erfolgt in einem kleinen Dialog innerhalb des Viewers, ohne das Lesen zu unterbrechen.

> **Hinweis**
>
> Diese Aktionen stehen nur zur Verfügung, wenn dem Arbeitsbereich in VS Code vertraut wird. Sie lassen sich nicht ausführen, während ein Dokument bearbeitet wird, während ein anderer Vorgang läuft oder wenn das Ziel ungespeicherte Änderungen enthält.

## Ein Dokument oder einen Ordner erstellen

1. Öffnen Sie das Eintragsmenü ([⋯] oder Rechtsklick) des Zielordners.
   Um direkt unterhalb der Dokumentwurzel zu erstellen, verwenden Sie [⋯] am rechten Rand der INDEX-Überschrift oder klicken Sie mit der rechten Maustaste auf eine freie Stelle im INDEX.
2. Wählen Sie [Neues Dokument] oder [Neuer Ordner].
3. Geben Sie einen Namen ein und drücken Sie [Erstellen].
   Ein Dokumentname benötigt eine Markdown-Erweiterung (`.md`, `.markdown`, `.mdx` und so weiter).

Neue Dokumente werden als Dokumente in der Standardsprache (Originaldokumente) erstellt.

## Ein Dokument duplizieren

1. Öffnen Sie das Eintragsmenü des Dokuments und wählen Sie [Duplizieren].
2. Geben Sie einen neuen Namen ein und drücken Sie [Erstellen].

Dupliziert wird nur das Originaldokument; seine Übersetzungen werden nicht dupliziert.

## Den Titel ändern

Ändert die Überschrift (H1) des Dokuments. Der Dateiname bleibt unverändert.

1. Öffnen Sie das Eintragsmenü eines Dokuments oder Ordners und wählen Sie [Titel ändern].
2. Geben Sie den neuen Titel in einer Zeile ein und drücken Sie [Ändern].

Bei einem Ordner wird die Überschrift seiner `README.md` geändert. Wird gerade eine Übersetzung angezeigt, ändert sich der Titel des Dokuments in dieser Sprache.

## Den Dokumentnamen ändern

Ändert den in der Symbolleiste angezeigten Dokumentnamen (den Namen der Dokumentwurzel).

1. Klicken Sie mit der rechten Maustaste auf den Dokumentnamen in der Symbolleiste. Das [⋯] am rechten Rand der INDEX-Überschrift öffnet dasselbe Menü.
2. Wählen Sie [Dokumentnamen ändern] und geben Sie einen neuen Namen ein.

Solange nichts eingestellt ist, wird der Ordnername unverändert angezeigt.

Ein von Ihnen festgelegter Name wird an **der Stelle** geschrieben, **die den Dokumentnamen derzeit liefert**, damit eine sichtbare Überschrift niemals ignoriert wird.

| Aktueller Zustand | Wird geschrieben nach |
|---|---|
| `lunascape-docs.json` enthält einen Namen | `lunascape-docs.json` wird aktualisiert |
| Kein Name, aber die Dokumentwurzel hat eine README | Die Überschrift (H1) der README wird geändert |
| Keines von beidem | `lunascape-docs.json` wird erstellt und der Name dort gespeichert |

Die Meldung nach der Änderung gibt an, wohin geschrieben wurde.

> **Tipp**
>
> Der Dokumentname wird in dieser Reihenfolge bestimmt: der Name in `lunascape-docs.json`, dann die Überschrift der README der Dokumentwurzel, dann der Ordnername.

## Einen Datei- oder Ordnernamen ändern

1. Öffnen Sie das Eintragsmenü und wählen Sie [Dateinamen ändern] oder [Ordnernamen ändern].
2. Geben Sie den neuen Namen ein und drücken Sie [Ändern].

Die zugehörigen Übersetzungen (derselbe Pfad unter `i18n/<Sprache>/`) werden mit umbenannt.

## Löschen

1. Öffnen Sie das Eintragsmenü und wählen Sie [In den Papierkorb verschieben].
2. Prüfen Sie die Bestätigungsmeldung und bestätigen Sie das Verschieben.

Das Ziel wird in den Papierkorb des Betriebssystems verschoben und kann bei Bedarf wiederhergestellt werden. Übersetzungen werden nicht gelöscht und bleiben erhalten.

## Namen, die nicht verwendet werden können

- Namen, die mit `.` beginnen (sie würden im INDEX nicht erscheinen)
- `i18n` (für Übersetzungsdateien reserviert)
- Unter Windows reservierte Namen (`CON`, `PRN` und so weiter)
- Namen, die auf einen Punkt oder ein Leerzeichen enden
- Namen mit Steuerzeichen oder mit Zeichen, die in Dateinamen nicht zulässig sind
- Namen, die im selben Ordner bereits vorhanden sind (einschließlich Namen, die sich nur in der Groß- und Kleinschreibung unterscheiden)

> **Hinweis**
>
> Die Startseite (normalerweise die `README.md` im Stammverzeichnis) kann weder umbenannt noch verschoben werden. Ändern Sie zuerst `startPage` in `lunascape-docs.json`.

## Verwandte Themen

- [Die Reihenfolge der Dokumente ändern](reorder.md)
- [Den INDEX verwenden](../02-reading/index-panel.md)
