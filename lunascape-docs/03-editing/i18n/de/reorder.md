# Reihenfolge der Dokumente ändern

Die im INDEX angezeigte Reihenfolge lässt sich per Drag-and-drop oder über die Tastatur ändern. Die geänderte Reihenfolge wird im Front Matter des Dokuments als `navigation.order` gespeichert.

## Per Drag-and-drop umsortieren

1. Ziehen Sie im INDEX ein Dokument oder einen Ordner.
2. Lassen Sie es vor oder hinter einem Element derselben Ebene oder auf einem Ordner los.
   Innerhalb derselben Ebene ändert sich die Reihenfolge. Beim Ablegen auf einem anderen Ordner wird das Element in diesen Ordner verschoben.

## Mit Tastatur oder Menü umsortieren

- Setzen Sie den Fokus auf einen Eintrag im INDEX und drücken Sie `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Wählen Sie im Menü des Eintrags [Nach oben verschieben] / [Nach unten verschieben].

## Was gespeichert wird

- Beim Umsortieren innerhalb derselben Ebene wird `navigation.order` im Front Matter des Originaldokuments aktualisiert. Bei einem Ordner wird der Wert in dessen `README.md` geschrieben. Hat der Ordner keine `README.md`, wird eine `README.md` nur mit Front Matter angelegt.
- Beim Verschieben in einen anderen Ordner werden das Originaldokument und die zugehörigen Übersetzungen gemeinsam verschoben. Vor dem Verschieben erscheint eine Rückfrage zu den Auswirkungen auf relative Links.
- Git-Staging und Commits werden nicht ausgeführt.

> **Hinweis**
>
> - Während einer Filterung, während der Bearbeitung eines Dokuments und in einem nicht vertrauenswürdigen Arbeitsbereich ist das Umsortieren nicht möglich.
> - Die Meldung „Der INDEX wurde aktualisiert“ bedeutet, dass gerade eine andere Änderung übernommen wurde. Führen Sie den Vorgang erneut aus.
> - Die Startseite lässt sich nicht in einen anderen Ordner verschieben.

> **Tipp**
>
> Wenn Sie `navigation.order` in Hunderterschritten vergeben, etwa 100, 200, 300, können Sie später leicht Dokumente dazwischen einfügen. Näheres finden Sie unter [Navigationsinformationen festlegen](../04-document-tools/navigation-metadata.md).

## Verwandte Themen

- [Dokumente und Ordner erstellen und ordnen](organize.md)
- [Navigationsinformationen festlegen](../04-document-tools/navigation-metadata.md)
