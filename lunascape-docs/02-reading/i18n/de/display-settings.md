# Anzeigeeinstellungen ändern

Über [Anzeigeeinstellungen] (Zahnrad) in der Symbolleiste kann jede Person ändern, wie der INDEX aussieht und ob die Bearbeiten-Schaltfläche angezeigt wird.

1. Drücken Sie in der Symbolleiste auf [Anzeigeeinstellungen].
2. Schalten Sie die gewünschten Einträge um. Die Änderungen werden sofort wirksam.
3. Drücken Sie erneut auf [Anzeigeeinstellungen] oder klicken Sie außerhalb des Bereichs, um ihn zu schließen.

## Einstellbare Einträge

| Bereich | Eintrag | Funktion |
|---|---|---|
| Dokumentsprache | (aktueller Zustand) | Zeigt die Standardsprache des Projekts und die aktuell angezeigte Sprache an. Über [Projektsprachen festlegen…] öffnen Sie die Spracheinstellungen des Projekts |
| Inhalt | [Dateinamen] | Zeigt Dateinamen anstelle der Dokumenttitel an |
| | [Dokumentsymbole] | Zeigt bei jedem Dokument ein Symbol an |
| | [Ordnersymbole] | Zeigt bei jedem Ordner ein Symbol an |
| | [Anzahl der Einträge] | Zeigt die Anzahl der Dokumente in einem Ordner an |
| | [Einrückungslinien] | Zeigt Linien an, die die Gliederungsebenen kennzeichnen |
| | [Ausblenden, wenn nur ein Dokument vorhanden ist] | Schließt den INDEX in einer Dokumentwurzel mit nur einem Dokument einmalig beim ersten Öffnen |
| | [Dokumentinformationen einklappen] | Klappt die Verwaltungstabelle am Anfang eines Dokuments zur Zeile „Dokumentinformationen“ ein. Ausgeschaltet wird die Tabelle unverändert angezeigt |
| | [Dichte] | Wählt den Zeilenabstand des INDEX zwischen [Standard] und [Kompakt] |
| | [Bearbeiten-Schaltfläche] | Zeigt [Bearbeiten] unten rechts im Dokument an |
| Aktionen | [Auf Projektstandard zurücksetzen] | Löscht alle eigenen Änderungen und stellt die Einstellungen des Projekts wieder her |
| | [Erweiterungseinstellungen öffnen] | Öffnet die Einstellungen von Lunascape Docs im Einstellungsfenster von VS Code |

> **Hinweis**
>
> - Die Anzeigeeinstellungen werden pro Person und pro Dokumentwurzel gespeichert und nicht in Dateien geschrieben, die mit Git verwaltet werden.
> - Die Einstellungen gelten in der Reihenfolge „eigene Anzeigeeinstellungen → VS Code-Einstellungen → `lunascape-docs.json` → Produktstandard“. Teamweite Standardwerte legen Sie in `lunascape-docs.json` unter `tree` und `editor` fest.

## Farbgebung umschalten

Wenn Sie in der Symbolleiste auf die Designumschaltung (Sonne/Mond) drücken, wechseln Sie zwischen weißem Hintergrund und der Farbgebung von VS Code. Welche Farbgebung beim Öffnen verwendet wird, legt die Einstellung `lunascapeDocEditor.appearance` (`light` oder `auto`) fest.

## Verwandte Themen

- [INDEX verwenden](index-panel.md)
- [Projekteinstellungen](../04-document-tools/project-configuration.md)
- [Übersicht der VS Code-Einstellungen](../08-reference/settings.md)
