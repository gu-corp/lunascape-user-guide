# Dokumente werden nicht angezeigt

## Es erscheint „Es wurde kein Markdown- oder docs-Ordner zum Öffnen gefunden"

- Der Arbeitsbereich enthält keinen Ordner `docs`, oder es wird ein anderer Name als `docs` verwendet.
  - Legen Sie `lunascape-docs.json` in diesen Ordner, damit er unabhängig vom Namen als Dokumentwurzel erkannt wird.
  - Oder fügen Sie den Ordnernamen der Einstellung `lunascapeDocEditor.rootDirectoryNames` hinzu.
- Wenn noch keine Dokumente vorhanden sind, erstellen Sie sie mit „Lunascape Docs: Dokumentation aus Vorlage erstellen".
- Sie können auch eine Markdown-Datei im Editor öffnen und anschließend „Lunascape Docs: In der Spezifikationsansicht öffnen" ausführen.

## Ein Dokument erscheint nicht im INDEX

- Prüfen Sie, ob die Dateiendung `.md`, `.markdown` oder `.mdx` lautet.
- Folgende Ordner werden nicht angezeigt: Ordner, die mit `.` beginnen, `node_modules` sowie Ordner, die unter `ignoredDirectories` angegeben sind (Standard: `99-archive`).
- Übersetzungen unterhalb von `i18n/` werden nicht einzeln im INDEX aufgeführt. Wechseln Sie über das Sprachmenü zu ihnen.
- Wenn eine gerade hinzugefügte Datei nicht erscheint, drücken Sie [Neu laden].
- Möglicherweise sehen Sie eine andere Dokumentwurzel. Prüfen Sie den Namen der Dokumentwurzel ganz links in der Symbolleiste.

## Beim Drücken eines Ordners wird nichts angezeigt

Die `README.md` dieses Ordners ist ein „reiner Konfigurationsdeskriptor", der nur Front Matter, aber keinen Textkörper enthält. Öffnen Sie den Ordner im INDEX und wählen Sie ein Dokument darin aus.

## Es wird eine unerwartete Dokumentwurzel geöffnet

- Wenn die Einstellung `lunascapeDocEditor.rootMode` auf `fixed` steht, wird immer `lunascapeDocEditor.root` geöffnet.
- Bei `auto` wird die Dokumentwurzel gewählt, die der geöffneten Markdown-Datei am nächsten liegt. Über das Auswahlmenü ganz links in der Symbolleiste können Sie wechseln.

## Der Name der Dokumentwurzel entspricht nicht der Erwartung

Der Name wird in dieser Reihenfolge bestimmt: `title` in `lunascape-docs.json` → `navigation.title` der `README.md` der Wurzel → deren H1 → `index.md` → Ordnername. Wenn Sie ihn festlegen möchten, setzen Sie `title`.

## Der INDEX ist verschwunden

- In einer Dokumentwurzel mit nur einem Dokument schließt sich der INDEX beim ersten Mal automatisch. Über das Spaltensymbol in der Symbolleiste lässt er sich öffnen. Unter [Anzeigeeinstellungen] können Sie dies mit [Ausblenden, wenn nur ein Dokument vorhanden ist] abschalten.
- Auf einem schmalen Bildschirm öffnen Sie ihn über [INDEX öffnen] (drei Striche) links von [Zurück].

## Ein Link lässt sich nicht öffnen

- „Das Linkziel wurde nicht gefunden": Die verlinkte Datei ist nicht vorhanden. Mit [Prüfung] in den Dokumentwerkzeugen können Sie interne Links prüfen.
- „Ein unsicherer oder nicht unterstützter Link wurde nicht geöffnet": Links außerhalb der Dokumentwurzel oder mit einem anderen Schema als `https://` oder `mailto:` werden nicht geöffnet.

## Es wird eine andere Sprache angezeigt als erwartet

- Prüfen Sie im Sprachmenü die Sprache der angezeigten Seite und deren Begründung.
- Die zuletzt gewählte Anzeigesprache wird gespeichert. Wählen Sie im Sprachmenü die Standardsprache erneut aus.
- Wenn die persönliche Einstellung `lunascapeDocEditor.locale` gesetzt ist, wird die Übersetzung in dieser Sprache bevorzugt.

## Verwandte Themen

- [Dokumentwurzel wechseln](../02-reading/roots.md)
- [Dokumentwurzeln und Dateikonventionen](../04-document-tools/structure.md)
