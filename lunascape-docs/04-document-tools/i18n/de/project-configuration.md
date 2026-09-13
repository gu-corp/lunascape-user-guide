# Projektkonfiguration

Die Datei `lunascape-docs.json` direkt unter der Dokumentwurzel enthält die im Team geteilte Konfiguration dieser Dokumentwurzel. Sie wird mit Git verwaltet.

## Die Konfigurationsdatei erstellen oder bearbeiten

- Drücken Sie in der Symbolleiste [Dokumentwerkzeuge] → Registerkarte [Prüfung] → [Woher die Regeln stammen und die Projekteinstellungen] → [Projekteinstellungen bearbeiten], um die Datei in VS Code zu öffnen. Wenn die Datei nicht vorhanden ist, wird in diesem Moment eine Anfangsdatei erstellt.
- Dem Dateinamen `lunascape-docs.json` wird automatisch das mitgelieferte JSON Schema zugeordnet, das eine Eingabevervollständigung und eine Beschreibung für jedes Feld bereitstellt. Ein `$schema`-Eintrag ist nicht erforderlich.

## Konfigurationsbeispiel

```json
{
  "id": "product-docs",
  "title": "Produktdokumentation",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Beschreibung der Felder

| Feld | Bedeutung | Standard |
|---|---|---|
| `id` | Der Schlüssel, unter dem die benutzerspezifischen Anzeigeeinstellungen gespeichert werden. Vergeben Sie eine feste ID, wenn die Einstellungen beim Verschieben des Ordners erhalten bleiben sollen | Der Ordnerpfad |
| `title` | Der Name, der ganz links in der Symbolleiste und in der Liste der Dokumentwurzeln angezeigt wird. Er ändert sich nicht mit der Anzeigesprache | Die Überschrift des README/index der Wurzel, sonst der Ordnername |
| `indexTitle` | Die Überschrift des INDEX | `INDEX` |
| `startPage` | Das zuerst geöffnete Dokument (relativ zur Dokumentwurzel) | `README.md` |
| `appearance` | Das Farbschema: `light` (immer hell) oder `auto` (folgt dem Design von VS Code) | `light` |
| `defaultLocale` | Die Standardsprache (die Sprache der Originaldokumente). Wird als BCP-47-Sprach-Tag angegeben (`ja`, `en`, `zh-Hant` usw.). Sie ist die Übersetzungsquelle | Nicht gesetzt (aus dem Text abgeleitet und angezeigt) |
| `fallbackLocale` | Die Sprache, die Lesern zuerst gezeigt wird, deren Umgebungssprache mit keiner der unterstützten Sprachen übereinstimmt. Geben Sie eine in `locales` enthaltene Sprache an | Nicht gesetzt (`defaultLocale` wird verwendet) |
| `locales` | Die Liste der unterstützten Sprachen. Schließt `defaultLocale` ein. Sie werden zu Einträgen im Sprachmenü und zu Übersetzungszielen | Nur `defaultLocale` |
| `ignoredDirectories` | Ordnernamen, die vom INDEX, von der Suche und von Prüfungen ausgeschlossen werden. Eine Angabe ersetzt den Standard | `["99-archive"]` |
| `tree` | Die Standardwerte für die Anzeige des INDEX. Benutzer können sie in den Anzeigeeinstellungen überschreiben | Wie im obigen Beispiel |
| `editor.defaultMode` | Die Bearbeitungsansicht, solange ein Benutzer noch nicht gewechselt hat: `visual` oder `source` | `visual` |
| `editor.showEditButton` | Ob [Bearbeiten] unten rechts im Dokument angezeigt wird | `true` |
| `documentStandards.pack` | Das Standard Pack, das für Dokumentprüfungen und Vorlagen verwendet wird: `builtin:<Name>` oder ein Pfad relativ zur Dokumentwurzel | Keins |
| `documentStandards.profile` | Ein vom Pack definierter Profilname | Keiner |
| `translation.enabled` | Aktiviert die Erstellung von Übersetzungsvorschlägen und die Massenübersetzung | `true` |
| `translation.contextFiles` | Das Original-Markdown (relativ zur Dokumentwurzel), das bei der Übersetzung als Referenz für Terminologie und Stil übergeben wird | `[]` |
| `translation.maxContextCharacters` | Die Obergrenze für die Gesamtzeichenzahl der Referenzdokumente (maximal 1048576) | `49152` |
| `description` | Eine einzeilige Beschreibung des Dokumentsatzes. Wird auf der Karte der Repository-Startseite angezeigt. Wie bei `title` kann sie als Zeichenkette oder als Objekt je Sprache geschrieben werden | Keine |

## Mitteilen, wo im Repository die Dokumente liegen

In eine `lunascape-docs.json` direkt unter dem Repository können Sie nicht die Einstellungen dieses Ordners, sondern eine **Karte des Repository** schreiben. Sobald Sie eines der folgenden drei Felder angeben, wird die Datei zu einer Karte, und der Ordner selbst wird dann keine Dokumentwurzel.

| Feld | Bedeutung | Standard |
|---|---|---|
| `defaultFolder` | In welchem Ordner die Dokumente liegen (Pfad relativ zu diesem Ordner). Das Ziel benötigt keine eigene Konfigurationsdatei | Keins (`docs` wird verwendet) |
| `roots` | Bei mehreren Dokumentsätzen deren Liste (Pfade relativ zu diesem Ordner, in Anzeigereihenfolge). In diesem Fall wird dieser Ordner zur Startseite | Keins |
| `excludes` | Ordner, die von der Ermittlung der Dokumentwurzeln ausgeschlossen werden (Pfade relativ zu diesem Ordner). Wird zu den Standardausschlüssen wie `node_modules` hinzugefügt | `[]` |
| `home.cards` | Ob die Startseite unter dem README die Karten der Dokumentsätze anzeigt. Setzen Sie es auf `false`, wenn Sie die Links im README selbst schreiben | `true` |

Die Dokumentwurzel wird in dieser Reihenfolge bestimmt. Von oben nach unten wird die erste gefundene verwendet.

1. Wenn eine Einstellung oder ein Befehl einen Ordner angibt, dieser Ordner
2. Das Ziel, auf das `defaultFolder` oder `roots` in der `lunascape-docs.json` direkt unter dem Repository verweist
3. Ein Ordner, der eine `lunascape-docs.json` enthält (liegen zwei oder mehr unter einem gemeinsamen übergeordneten Ordner, wird dieser zur Startseite)
4. Der Ordner `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Das Repository direkt selbst

> **Tipp**
>
> Wenn nichts angegeben ist, greift Punkt 4, sodass ein gewöhnliches Repository mit einem einzelnen `docs/` sich wie bisher verhält. Geben Sie `defaultFolder` nur an, wenn der Ordner anders heißen soll, etwa `manual`.

### Beispiel für eine Karte

```json
{
  "title": "Lunascape Hilfe",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Rangfolge der Einstellungen

Anzeigebezogene Felder haben in dieser Reihenfolge Vorrang.

1. Die Anzeigeeinstellungen des Benutzers (Panel [Anzeigeeinstellungen])
2. Die Einstellungen von VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Die Standardwerte des Produkts

Nur die Sprachen (`defaultLocale`, `fallbackLocale`, `locales`) bilden eine Ausnahme: Hier ist `lunascape-docs.json` maßgeblich. Die Sprachen des Projekts können nicht über die persönlichen Einstellungen von VS Code überschrieben werden.

> **Hinweis**
>
> Ein Standard Pack kann auch als `standard` in `docs-lint.config.json` angegeben werden. Sind beide vorhanden, hat `docs-lint.config.json` Vorrang.

## Verwandte Themen

- [Prüfregeln ändern](rules.md)
- [Anzeigeeinstellungen ändern](../02-reading/display-settings.md)
- [Liste der VS-Code-Einstellungen](../08-reference/settings.md)
