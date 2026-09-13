# VS Code-Einstellungen

Suchen Sie in den VS Code-Einstellungen (`⌘,` / `Ctrl+,`) nach „Lunascape Docs", um die folgenden Punkte zu ändern. Alle sind persönliche Einstellungen und werden nie in den Dokumenten des Projekts gespeichert.

## Dokumentwurzel

| Einstellung | Werte | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` wählt automatisch die Dokumentwurzel, die der geöffneten Markdown-Datei am nächsten liegt, und öffnet vorübergehend den übergeordneten Ordner, wenn die Datei zu keiner gehört. `fixed` öffnet immer die Dokumentwurzel aus `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Zeichenkettenliste | `["docs"]` | Ordnernamen, die im Modus `auto` als Dokumentwurzel gefunden werden. Ein Ordner mit `lunascape-docs.json` wird unabhängig von seinem Namen gefunden. Sind in der `lunascape-docs.json` direkt im Repository `defaultFolder` oder `roots` angegeben, haben diese Vorrang |
| `lunascapeDocEditor.root` | Pfad | `docs` | Die Dokumentwurzel relativ zum Arbeitsbereich für den Modus `fixed` und beim Öffnen über den Befehl |
| `lunascapeDocEditor.startPage` | Pfad | `README.md` | Die Startseite relativ zur Dokumentwurzel |
| `lunascapeDocEditor.title` | Zeichenkette | `Lunascape Docs` | Überschreibt den Titel des Dokumenttabs. Der Name in der Auswahl der Dokumentwurzel bleibt unverändert |
| `lunascapeDocEditor.ignoredDirectories` | Zeichenkettenliste | `["99-archive"]` | Ordnernamen, die aus dem INDEX ausgeschlossen werden |

## Anzeige

| Einstellung | Werte | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` verwendet einen weißen Hintergrund, `auto` folgt dem Farbschema von VS Code |
| `lunascapeDocEditor.locale` | Sprachkennung | Keine | Ihre bevorzugte Dokumentsprache, sofern verfügbar. Die Sprache des Originaldokuments im Projekt wird nicht geändert |
| `lunascapeDocEditor.documentMetadata.compact` | Wahrheitswert | `true` | Klappt die Dokumentverwaltungstabelle direkt unter der H1 in die Zeile „Dokumentinformationen" ein |
| `lunascapeDocEditor.tree.showFileNames` | Wahrheitswert | `false` | Zeigt im INDEX Dateinamen statt Dokumentnamen an |
| `lunascapeDocEditor.tree.showDocumentIcons` | Wahrheitswert | `false` | Zeigt im INDEX Dokumentsymbole an |
| `lunascapeDocEditor.tree.showFolderIcons` | Wahrheitswert | `false` | Zeigt im INDEX Ordnersymbole an |
| `lunascapeDocEditor.tree.showItemCounts` | Wahrheitswert | `false` | Zeigt im INDEX die Anzahl der Einträge direkt unter jedem Ordner an |
| `lunascapeDocEditor.tree.showGuides` | Wahrheitswert | `true` | Zeigt im INDEX Hilfslinien für die Ebenen an |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Zeilenabstand des INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Wahrheitswert | `true` | Schließt den INDEX einmalig, wenn nur ein Dokument vorhanden ist |

## Bearbeiten

| Einstellung | Werte | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Die Bearbeitungsansicht, solange Sie nicht gewechselt haben. Die zuletzt verwendete Ansicht hat Vorrang |
| `lunascapeDocEditor.editor.showEditButton` | Wahrheitswert | `true` | Zeigt [Bearbeiten] unten rechts im Dokument an |

## Diagramme

| Einstellung | Werte | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Die Laufzeitumgebung für die TikZ-Darstellung. `bundled` verwendet die mitgelieferte geprüfte Laufzeitumgebung (in der aktuellen Auslieferung nicht enthalten), `workspace` verwendet `node-tikzjax` 1.0.5 direkt in einem vertrauenswürdigen Arbeitsbereich (nur für Entwicklung und Erprobung), `disabled` stellt nichts dar |

## Veraltete Einstellungen

| Einstellung | Stattdessen verwenden |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` in `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` in `lunascape-docs.json` |

Die Sprachen des Projekts lassen sich mit persönlichen Einstellungen nicht überschreiben.

## Verwandte Themen

- [Anzeigeeinstellungen ändern](../02-reading/display-settings.md)
- [Projektkonfiguration](../04-document-tools/project-configuration.md)
