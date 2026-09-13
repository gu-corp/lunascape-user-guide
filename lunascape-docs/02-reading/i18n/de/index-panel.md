# INDEX verwenden

Der INDEX auf der linken Seite ist die Baumansicht der Ordner und Dokumente in der Dokumentwurzel.

## Filtern

1. Geben Sie oberhalb des INDEX ein Wort in [Dokumente filtern] ein.
2. Es werden nur die Einträge angezeigt, deren Dokumentname übereinstimmt. Löschen Sie die Eingabe, um wieder alles anzuzeigen.

> **Hinweis**
>
> Während des Filterns ist das Umsortieren per Drag-and-drop nicht möglich.

## Ordner auf- und zuklappen

- Drücken Sie den Pfeil links neben einem Ordnernamen oder den Namen eines Ordners ohne Titelseite, um ihn auf- oder zuzuklappen.
- Bei einem Ordner mit Titelseite (einer `README.md` oder `index.md` mit Inhalt) öffnet ein Druck auf den Namen diese Titelseite. Um nur auf- oder zuzuklappen, verwenden Sie [Ordner öffnen] / [Ordner schließen] im Eintragsmenü.
- Der Auf- und Zuklappzustand wird pro Benutzer gespeichert und nicht in von Git verwaltete Dateien geschrieben.

## README und die Titelseite eines Ordners

`README.md` ist die Datei, die den Inhalt eines Ordners beschreibt.

- Bei einem Ordner mit README wird beim Drücken des Ordnernamens diese README angezeigt.
- Bei einem Ordner ohne README wird das oberste Dokument darin angezeigt.
- Die Überschrift (H1) der README wird zum Namen dieses Ordners im INDEX.

Eine README ist nicht erforderlich. Um sie später hinzuzufügen, wählen Sie im Eintragsmenü des Ordners [README erstellen] (erscheint nur bei Ordnern ohne README).

## INDEX ein- oder ausblenden

- Mit dem linken Symbol der Spaltenanzeige in der Symbolleiste blenden Sie den INDEX ein oder aus. Das rechte Symbol blendet „Auf dieser Seite“ ein oder aus.
- Auf schmalen Bildschirmen beginnt der INDEX geschlossen. Drücken Sie [INDEX öffnen] (drei Linien) links neben [Zurück], dann öffnet sich der INDEX über dem Text. Er schließt sich über das [×] im INDEX, einen Klick auf den Hintergrund, `Esc` oder beim Wechsel des Dokuments. Dieses vorübergehende Öffnen und Schließen ändert die Einstellung für breite Bildschirme nicht.
- In einer Dokumentwurzel, in der nur ein Dokument angezeigt wird, schließt sich der INDEX nur beim ersten Mal automatisch. Über das Symbol der Spaltenanzeige öffnen Sie ihn wieder. Dieses Verhalten lässt sich unter [Anzeigeeinstellungen] mit [Ausblenden, wenn nur ein Dokument vorhanden ist] abschalten.

## Das Eintragsmenü verwenden

Mit dem [⋯], das erscheint, wenn Sie mit der Maus auf einen Eintrag im INDEX zeigen, oder mit einem Rechtsklick auf den Eintrag öffnen Sie dessen Menü. Die Einträge sind in dieser Reihenfolge angeordnet.

| Gruppe | Einträge |
|---|---|
| Häufige Aktionen | [Ordner öffnen] / [Ordner schließen], [INDEX öffnen] (Titelseite des Ordners öffnen), [Bearbeiten], [Titel ändern], [In VS Code öffnen], [Pfad kopieren] |
| Erstellen und Ordnen | [README erstellen] (nur bei Ordnern ohne README), [Neues Dokument], [Neuer Ordner], [Duplizieren], [Dateinamen ändern] / [Ordnernamen ändern], [Nach oben verschieben], [Nach unten verschieben] |
| Löschen | [In den Papierkorb verschieben] |

- Um direkt unterhalb der Dokumentwurzel etwas anzulegen, drücken Sie das [⋯] am rechten Rand der INDEX-Überschrift oder klicken Sie mit der rechten Maustaste auf eine leere Stelle im INDEX und wählen dann [Neues Dokument] oder [Neuer Ordner]. Im selben Menü stehen [Dokumentnamen ändern] und, wenn die Dokumentwurzel keine README hat, [README erstellen]. Auch ein Rechtsklick auf den in der Symbolleiste angezeigten Dokumentnamen öffnet dasselbe Menü.
- Im Menü bewegen Sie sich mit `↑` `↓`, mit `Home` `End` springen Sie an den Anfang und ans Ende. Schließen Sie mit `Esc`, kehrt der Fokus an die Stelle zurück, an der das Menü geöffnet wurde.

> **Hinweis**
>
> Die Einträge zum Erstellen, Ordnen und Löschen erscheinen nur, wenn dem Arbeitsbereich in VS Code vertraut wird. Während ein Dokument bearbeitet wird oder eine andere INDEX-Aktion verarbeitet wird, stehen sie ebenfalls nicht zur Verfügung.

## Die Darstellung ändern

Unter [Anzeigeeinstellungen] können Sie die Anzeige der Dateinamen, die Symbole für Dokumente und Ordner, die Anzahl der Einträge in Ordnern, die Hilfslinien der Ebenen und die Anzeigedichte ändern. Näheres finden Sie unter [Anzeigeeinstellungen ändern](display-settings.md).

## Verwandte Themen

- [Dokumente und Ordner erstellen und ordnen](../03-editing/organize.md)
- [Die Reihenfolge der Dokumente ändern](../03-editing/reorder.md)
