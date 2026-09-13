# Dokumentwurzeln und Dateikonventionen

Dies sind die Regeln, nach denen Lunascape Docs Dokumente findet und den INDEX zusammenstellt. Das Dateisystem selbst ist das Original, daher sind kein Verzeichnis und keine Build-Konfiguration nötig.

## Dokumentwurzel

- Der nächstgelegene Ordner `docs` oder der Ordner, der `lunascape-docs.json` enthält, wird zur Dokumentwurzel.
- Mit einer `lunascape-docs.json` muss der Ordner nicht `docs` heißen.
- Wenn Sie eine Markdown-Datei außerhalb jeder Dokumentwurzel öffnen, wird deren Ordner als vorübergehende Dokumentwurzel angezeigt.

## Im INDEX angezeigte Dateien

- Angezeigt werden Dateien mit `.md`, `.markdown` und `.mdx`. Neue Dateien erscheinen immer, auch ohne Front Matter oder Navigationsangaben.
- Ordner, die mit `.` beginnen, `node_modules` sowie die unter `ignoredDirectories` angegebenen Ordner (Standard: `99-archive`) werden nicht angezeigt.
- Alles unterhalb von `i18n/` gilt als Übersetzung und wird im INDEX nicht gesondert aufgeführt.

## Titelseiten von Ordnern

- Eine `README.md` mit Inhalt (oder `index.md`, wenn keine README vorhanden ist) ist die Titelseite ihres Ordners. Wenn Sie im INDEX auf den Ordnernamen drücken, wird sie geöffnet.
- Eine `README.md`, die nur aus Front Matter ohne Inhalt besteht, gilt als „reiner Konfigurationsdeskriptor“ und wird nicht als Seite angezeigt. Verwenden Sie sie, wenn ein Ordner nur einen Titel oder eine Reihenfolge braucht.
- Wenn sowohl `README.md` als auch `index.md` vorhanden sind, hat `README.md` Vorrang.

## Standardsprache und Übersetzungen

- Dokumente in der Standardsprache (Originaldokumente) bleiben an ihrem Platz.
- Eine Übersetzung kommt unter demselben Dateinamen in den Ordner `i18n/<Sprache>/` neben dem Originaldokument. Die Ordnerstruktur unterhalb von `i18n/` nachzubauen, wird nicht erkannt.
- Nur an dieser einen Stelle wird eine Übersetzung aufgelöst. Dieselbe Datei an einem anderen Ort ist eine verwaiste Datei, die zu keinem Dokument als Übersetzung gehört.

```text
docs/
  lunascape-docs.json
  README.md                  ← landing page of the root (start page)
  i18n/en/README.md          ← its English translation
  01-product/
    README.md                ← landing page of the folder
    requirements.md
    i18n/en/README.md        ← the English translations of the two above
    i18n/en/requirements.md
  99-archive/                ← excluded from the INDEX by default
```

## Über `_meta.json`

Die `_meta.json` von Nextra wird nicht für die Navigation verwendet. Vorhandene Dateien werden weder geändert noch gelöscht. Künftig wird sie ausschließlich von einer ausdrücklichen Import-/Exportfunktion behandelt.

## Verwandte Themen

- [Navigationsangaben festlegen](navigation-metadata.md)
- [Projekteinstellungen](project-configuration.md)
- [Dokumentwurzel wechseln](../02-reading/roots.md)
