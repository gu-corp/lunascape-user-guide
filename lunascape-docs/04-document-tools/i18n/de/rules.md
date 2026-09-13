# Prüfregeln ändern

Sie können die Meldungsstufe jeder Prüfung (Fehler, Warnung, Information) ändern oder eine Prüfung abschalten. Die Änderungen werden in der Datei `docs-lint.config.json` in der Dokumentwurzel gespeichert und im Team geteilt.

## Meldungsstufe ändern

1. Drücken Sie in der Symbolleiste [Dokumentwerkzeuge] und öffnen Sie die Registerkarte [Prüfung].
2. Drücken Sie [Regeln prüfen und ändern].
   Die Liste der Prüfungen klappt innerhalb derselben Karte auf. Zu jeder Prüfung werden ihr Zweck und die Herkunft der aktuellen Einstellung angezeigt (Project, Profile, Pack oder Default).
3. Wählen Sie die Meldungsstufe der Prüfung, die Sie ändern möchten.
4. Drücken Sie [Speichern und erneut prüfen].
   Die Einstellung wird gespeichert, und die gesamte Dokumentwurzel wird mit der neuen Einstellung erneut geprüft.

| Auswahl | Bedeutung |
|---|---|
| [Standardeinstellung (…)] | Entfernt die Überschreibung und stellt die Standardeinstellung wieder her, die sich aus Profil, Standard Pack und Vorgabewert in dieser Reihenfolge ergibt |
| [Aus] | Diese Prüfung wird nicht ausgeführt |
| [Information] / [Warnung] / [Fehler] | Meldet auf dieser Stufe |

> **Hinweis**
>
> - Zum Speichern ist ein vertrauenswürdiger Arbeitsbereich erforderlich.
> - Gespeichert wird nur die Meldungsstufe jeder Prüfung. Die Optionen der einzelnen Prüfungen bleiben unverändert. Das Standard Pack und das Profil selbst werden auf diesem Bildschirm nicht geändert.
> - Wenn `docs-lint.config.json` unmittelbar vor dem Speichern von außen geändert wurde, wird das Speichern abgebrochen. Laden Sie den aktuellen Stand neu und versuchen Sie es erneut.
> - Ist keine `docs-lint.config.json` vorhanden, wird sie beim Speichern angelegt.

## Die Konfigurationsdateien direkt bearbeiten

- Mit [Vollständige Einstellungen öffnen] öffnen Sie `docs-lint.config.json` in VS Code.
- Öffnen Sie [Woher die Regeln stammen und die Projekteinstellungen] und drücken Sie [Projekteinstellungen bearbeiten], um `lunascape-docs.json` in VS Code zu öffnen. Das Standard Pack und das Profil wählen Sie dort aus.

Für beide Dateien stehen Eingabevervollständigung und Beschreibungen aus den JSON-Schemas zur Verfügung, die der Erweiterung beiliegen.

## Standard Pack und Profile

Ein Standard Pack ist ein Dokumentationsstandard, der die erforderlichen Dokumentarten, die Kapitelgliederung, die Terminologie und die Vorlagen zusammenfasst. Sie wählen es in `lunascape-docs.json` unter `documentStandards` aus.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Das mitgelieferte Pack `builtin:gu-corp-software` enthält die Profile `base`, `web-application`, `api-service`, `regulated-financial-product` und `smart-contract`.

## Verwandte Themen

- [Dokumente prüfen](check.md)
- [Projekteinstellungen](project-configuration.md)
