# Prüfung, Erstellung oder Übersetzung schlägt fehl

## Prüfung

### „docs-lint ist nicht verfügbar" wird angezeigt

- Die Laufzeitumgebung von docs-lint fehlt in der Erweiterung, oder die Konfiguration ist fehlerhaft. Installieren Sie die Erweiterung neu.
- „Vertrauen Sie diesem Arbeitsbereich in VS Code, damit lokales Pack und Konfiguration sicher geladen werden können": Für ein lokales Standard Pack ist ein vertrauenswürdiger Arbeitsbereich erforderlich.

### Das Ergebnis bleibt bei „Erneute Prüfung erforderlich"

Sobald Sie ein Dokument oder eine Einstellung ändern, wird das vorherige Ergebnis ungültig. Drücken Sie erneut [Dokumentwurzel prüfen]. Nicht gespeicherte Änderungen werden nicht berücksichtigt.

### Ein Befund lässt sich nicht durch Drücken öffnen

Einträge zur „gesamten Dokumentwurzel" sind keinem bestimmten Dokument zugeordnet und haben daher keine Position. Prüfen Sie das betreffende Dokument anhand des Befundtextes.

### Regeln lassen sich nicht speichern

- Ein vertrauenswürdiger Arbeitsbereich ist erforderlich.
- „Die Lint-Konfiguration wurde durch einen anderen Vorgang geändert": `docs-lint.config.json` wurde von außen geändert. Laden Sie den aktuellen Stand und versuchen Sie es erneut.
- Konfigurationsdateien, die symbolische Verknüpfungen sind oder außerhalb der Dokumentwurzel liegen, lassen sich nicht bearbeiten.

## Erstellen aus einer Vorlage

- „Die Vorschau der Vorlage ist abgelaufen" / „Die Eingaben wurden geändert": Drücken Sie erneut [Vorschau] und erstellen Sie dann das Dokument.
- „Am Zielort ist bereits ein Dokument vorhanden": Vorhandene Dateien werden nicht überschrieben. Geben Sie einen anderen Zielort an.
- Der Zielort benötigt einen Pfad relativ zur Dokumentwurzel und die Endung `.md` bzw. `.mdx`. Unterhalb von `i18n` lässt sich nichts erstellen.
- „Vertrauen Sie dem Arbeitsbereich, um Dokumente zu erstellen": Stufen Sie den Arbeitsbereich in VS Code als vertrauenswürdig ein.

<!-- ai-only:start -->
## Übersetzung

### Die Schaltflächen für die Übersetzung lassen sich nicht drücken

- „Für diese Dokumentwurzel ist die KI-Übersetzung nicht aktiviert": Setzen Sie `translation.enabled` in `lunascape-docs.json` auf `true`.
- „Die Standardsprache des Projekts ist nicht festgelegt": Speichern Sie die Standardsprache unter [Anzeigeeinstellungen ändern](../02-reading/display-settings.md).
- „Fügen Sie die Zielsprache zu den unterstützten Sprachen hinzu": Nehmen Sie die Zielsprache in `locales` auf.
- „Kein Originaldokument zum Übersetzen gefunden": Sie haben eine übersetzte Seite geöffnet. Wechseln Sie zur Seite in der Standardsprache.
- Bei einer vorübergehend geöffneten Ordneransicht lässt sich die Stapelübersetzung nicht verwenden. Legen Sie eine `lunascape-docs.json` in diesen Ordner, um ihn zur Dokumentwurzel zu machen.

### Ein Übersetzungsvorschlag wird abgelehnt oder muss neu erstellt werden

- „Das Originaldokument wurde geändert. Erstellen Sie den Übersetzungsvorschlag neu": Nach dem Erstellen des Vorschlags hat sich das Original oder das Ziel geändert. Übersetzen Sie erneut.
- Fehlen in der Antwort des Sprachmodells zu schützende Bezeichner oder Code, wird sie nicht angenommen. Den Inhalt der Antwort finden Sie im Ausgabebereich unter „Lunascape Docs 翻訳".
- „Die Stapelübersetzung umfasst höchstens 1000 Dokumente pro Durchlauf": Teilen Sie den Umfang nach Ordnern oder durch ausdrückliche Auswahl auf.
<!-- ai-only:end -->

## Verwandte Themen

- [Dokumente prüfen](../04-document-tools/check.md)
- [Ein Dokument aus einer Vorlage erstellen](../04-document-tools/templates.md)
- [Arbeit an eine KI übergeben](../05-ai/README.md)
