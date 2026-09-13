# Die Erweiterung installieren

Die VS Code-Erweiterung „Lunascape Docs Pro" wird als VSIX-Datei verteilt. Sie ist kostenlos; „Pro" kennzeichnet die Ausgabe, die Arbeit an eine KI übergibt und sich selbst aktualisiert.

## Systemvoraussetzungen

- VS Code 1.90 oder neuer
- Funktionen, die schreiben — Dokumente erstellen, den INDEX ordnen, Prüfeinstellungen speichern, übersetzen — funktionieren nur in einem Arbeitsbereich, den Sie in VS Code als vertrauenswürdig markiert haben.

## Installieren

1. Beschaffen Sie die VSIX-Datei. Dieser Link verweist immer auf die aktuelle Version.

   [lunascape-docs-pro.vsix herunterladen](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Öffnen Sie die Erweiterungsansicht (`⇧⌘X` / `Ctrl+Shift+X`).
3. Wählen Sie im Menü `…` oben rechts [Aus VSIX installieren…] und geben Sie die heruntergeladene Datei an.

### Über die Befehlszeile

Eine Zeile, wenn Sie das Terminal nicht verlassen möchten. Sie lädt herunter und installiert.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Hinweis**
> Wenn `code` nicht gefunden wird, führen Sie in der Befehlspalette (`⇧⌘P` / `Ctrl+Shift+P`) den Befehl [Shell-Befehl: Befehl 'code' in PATH installieren] aus.

## Aktualisieren

Wenn eine neuere Version veröffentlicht wird, holt und installiert die Erweiterung sie selbst. VS Code bietet an, das Fenster neu zu laden, und dann wechseln Sie zur neuen Version. Ihre Einstellungen und Dokumente bleiben unverändert erhalten.

Geprüft wird einmal am Tag. Wenn Sie sofort nachsehen möchten, führen Sie in der Befehlspalette (`⇧⌘P` / `Ctrl+Shift+P`) den Befehl [Lunascape Docs: Auf neuere Version prüfen] aus.

Das Verhalten lässt sich über die Einstellung `lunascapeDocEditor.update.check` ändern.

| Einstellung | Verhalten |
|---|---|
| Eine neuere Version installieren, sobald sie veröffentlicht wird | Standard |
| Benachrichtigen und jedes Mal selbst entscheiden | Eine Benachrichtigung erscheint, und es ändert sich nichts, bis Sie [Aktualisieren] drücken |
| Nie prüfen | Es passiert nichts |

### Wenn keine Aktualisierung möglich ist

Erscheint „Aktualisierung konnte nicht abgerufen werden: No Servers", dann ist die installierte Version 0.22.18 oder älter. Deren Aktualisierungsvorgang schlägt jedes Mal beim letzten Schritt fehl, sodass sie sich nicht selbst auf eine neuere Version bringen kann. Installieren Sie einmal von Hand wie oben beschrieben; danach aktualisiert sie sich selbst.

## Die Version prüfen

Öffnen Sie „Lunascape Docs Pro" in der Erweiterungsansicht, um die installierte Version zu sehen. Sie benötigen sie, wenn Sie einen Fehler melden.

## Verwandte Themen

- [Ihre ersten Dokumente erstellen](first-documents.md)
- [Einen Fehler melden](../07-troubleshooting/report.md)
