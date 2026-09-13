# Eigene Dokumente im Web veröffentlichen

Sie können die Dokumente Ihres eigenen Repositorys als Website über GitHub Pages oder ein beliebiges statisches Hosting veröffentlichen. Dafür gibt es zwei Wege. Diese Anleitung richtet sich an Entwickler, die das Repository von Lunascape Docs klonen und `npm` verwenden können.

## Weg 1: Die zwei Dateien des Viewers ablegen

Hierbei legen Sie nur den Viewer selbst ab (`index.html` und `lsdoc.js`) und lassen die Dokumente von GitHub laden. Die Dokumente selbst sind nicht Teil der Website, daher ist dieser Weg auch für nicht öffentliche Repositorys sicher (die Leser melden sich bei GitHub an).

1. Führen Sie im Repository von Lunascape Docs den folgenden Befehl aus.

   ```sh
   npm run build:viewer
   ```

   In `dist/viewer/` werden `index.html` und `lsdoc.js` erzeugt.
2. Legen Sie die beiden Dateien in `docs/` des Repositorys ab, das Sie veröffentlichen möchten.
3. Aktivieren Sie GitHub Pages.

Die anzuzeigende Dokumentwurzel wird in dieser Reihenfolge bestimmt.

1. Die Einstellung `source` in `index.html`
2. Der Eintrag `repository` in einer `lunascape-docs.json` im selben Ordner
3. Ableitung aus der `*.github.io`-URL und dem Aufbau der Branches

## Weg 2: Eine statische Website samt Dokumenten exportieren

Hierbei exportieren Sie den Viewer zusammen mit den Dokumentdateien und hosten das Ergebnis unverändert.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Ausgegeben werden der vollständige Viewer, die Dokumente unterhalb von `docs/`, die Übersichtsdatei `lunascape-docs-manifest.json` und `.nojekyll`. Legen Sie das Ergebnis auf S3 oder GitHub Pages ab, um es zu veröffentlichen. Ein Beispiel für die automatische Veröffentlichung mit GitHub Actions finden Sie im Repository unter `examples/workflows/publish-docs-pages.yml`.

> **Hinweis**
>
> - **Exportieren Sie die Dokumente eines nicht öffentlichen Repositorys nicht auf GitHub Pages.** GitHub Pages außerhalb von Enterprise Cloud ist für jeden lesbar. Wenn Sie die Veröffentlichung beschränken müssen, verwenden Sie Weg 1 und lassen Sie die Leser sich bei GitHub anmelden.
> - `index.html` direkt über `file://` zu öffnen, funktioniert nicht. Browser verbieten dabei das Laden benachbarter Dateien und das Ausführen von ES-Modulen. Verwenden Sie zum Prüfen vor Ort die VS Code-Version oder einen HTTP-Server.
> - Die Zeichenbibliotheken für TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob und Penrose werden bei der Anzeige geladen. Legen Sie bei einer exportierten Website auch den Ordner `vendor/` mit ab.

## Verwandte Themen

- [Was die Web-Version kann](README.md)
- [Ein nicht öffentliches Repository lesen](private-repository.md)
