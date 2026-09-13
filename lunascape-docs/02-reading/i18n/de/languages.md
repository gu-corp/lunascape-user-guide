# In einer anderen Sprache lesen

Wenn ein Dokument Übersetzungen hat, können Sie die Sprache über das Sprachmenü (Globus) in der Symbolleiste wechseln.

## Die Sprache wechseln

1. Drücken Sie in der Symbolleiste auf das Sprachmenü.
   Angezeigt werden die Sprache der aktuellen Seite und deren Grundlage (Pfad der Übersetzung, automatische Erkennung oder Standardsprache des Projekts).
2. Wählen Sie die Sprache, in der Sie lesen möchten.
   Die Übersetzung desselben Dokuments wird geöffnet. Die gewählte Sprache wird gespeichert; das nächste Dokument, das Sie öffnen, wird in dieser Sprache angezeigt, sofern eine Übersetzung vorhanden ist.

In der Sprachliste ist angegeben, ob für dieses Dokument eine Übersetzung vorliegt.

| Anzeige | Bedeutung |
|---|---|
| Übersetzt | Eine Übersetzung ist vorhanden und kann geöffnet werden |
| Nicht übersetzt | Die Sprache wird vom Projekt unterstützt, für dieses Dokument gibt es aber noch keine Übersetzung |
| Veraltet | Eine Übersetzung ist vorhanden, das Originaldokument wurde aber nach der Übersetzung geändert |

> **Hinweis**
>
> - Beim Wählen einer Sprache wird lediglich eine vorhandene Übersetzung geöffnet. Es wird weder eine Übersetzung erzeugt noch eine Datei angelegt. Um eine Übersetzung zu erstellen, verwenden Sie im selben Menü [Übersetzungen erstellen und verwalten…].
> - Wenn die Sprache der aktuellen Seite von der Standardsprache des Projekts abzuweichen scheint, wird eine Warnung angezeigt. Die Einstellungen werden dabei nicht verändert.

## Die zuerst angezeigte Sprache

Beim Öffnen eines Dokuments wird die anfängliche Anzeigesprache in dieser Reihenfolge bestimmt.

1. Die Sprache, die Sie in dieser Dokumentwurzel zuvor selbst gewählt haben. Ihre Wahl wird gespeichert (auch die Wahl der Standardsprache wird als Auswahl gespeichert).
2. Die Anzeigesprache von VS Code (in der Webbrowser-Version die Spracheinstellung des Browsers). Eine passende unterstützte Sprache wird automatisch ausgewählt. Eine Sprache mit Regionsangabe (etwa `en-US`) passt auch zur Basissprache (`en`).
3. Die Ausweichsprache des Projekts (`fallbackLocale` in `lunascape-docs.json`).
4. Die Standardsprache des Projekts.

> **Tipp**
>
> - Bei automatischer Auswahl wird die aktuelle Sprache im Sprachmenü mit „Automatisch ausgewählt“ gekennzeichnet. Zeigen Sie mit dem Mauszeiger auf die Kennzeichnung, um den Grund zu sehen.
> - `fallbackLocale` ist die Sprache, die Leserinnen und Lesern angezeigt wird, deren Umgebungssprache zu keiner der unterstützten Sprachen passt. Setzen Sie in einem Projekt mit japanischem Originaldokument und englischer Übersetzung den Wert `"en"`, so wird etwa in einer spanischsprachigen Umgebung die englische Fassung geöffnet. Ohne Angabe wird die Standardsprache verwendet.

## Wo Übersetzungen liegen

Dokumente in der Standardsprache bleiben an ihrem Platz; Übersetzungen liegen **im selben Ordner unter `i18n/<Sprache>/`**, unter demselben Dateinamen.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Hinweis**
>
> - Wird die Ordnerstruktur unter `i18n/` nachgebildet (`i18n/en/guide/setup.md`), wird sie nicht erkannt. Der Ordner `i18n/` liegt immer im selben Ordner wie das Dokument.
> - Übersetzungen werden ausschließlich an dieser einen Stelle aufgelöst. Legen Sie die Übersetzung desselben Dokuments zusätzlich im `i18n/` eines übergeordneten Ordners ab, entsteht kein Vorrangkonflikt: Die Kopie im übergeordneten Ordner wird zu einer verwaisten Datei, die weder im Sprachmenü noch im Verzeichnis erscheint (und nicht automatisch gelöscht wird). Legen Sie dieselbe Übersetzung nicht an zwei Stellen ab.

## Beim Lesen in der Webbrowser-Version

Auch in der Webbrowser-Version können Sie auf dieselbe Weise wechseln, sofern eine Übersetzung vorhanden ist. Möchten Sie in einer Sprache lesen, für die es keine Übersetzung gibt, können Sie die Seitenübersetzung des Browsers verwenden. Code, Formeln und Diagramme sind von der Übersetzung ausgenommen.

## Verwandte Themen

- [Arbeit an eine KI übergeben](../05-ai/README.md)
- [Übergebbare Aufgaben](../05-ai/tasks.md)
- [Anzeigeeinstellungen ändern](../02-reading/display-settings.md)
