# Sicherheit und Schreibgrenzen

Die Grenzen, die Lunascape Docs zum Schutz Ihrer Dokumente und Ihres Geräts einhält.

## Anzeige

- HTML, das aus Markdown erzeugt wird, und SVG, das aus Diagrammen erzeugt wird, werden vor der Anzeige mit DOMPurify 3.4.14 bereinigt.
- Beliebige Skripte in MDX werden niemals ausgeführt.
- KaTeX läuft mit `trust: false`, `maxSize: 50` und `maxExpand: 1000` und vertraut weder externem HTML noch beliebigen Befehlen.
- Die Zeichenbibliotheken von Markmap, WaveDrom, Svgbob, Vega-Lite und Penrose werden nur dann, wenn der entsprechende Block vorhanden ist, in festgelegten Versionen lokal auf dem Gerät geladen. Verweise auf externe Ressourcen, rohes HTML und ausführbare Notationen sind nicht erlaubt, und aus dem erzeugten SVG werden Skripte, externe Bilder, `link`, `style` und `foreignObject` entfernt.
- Das Zeichnen von TikZ startet nicht das LaTeX des Hosts, sondern läuft nacheinander in einem WebAssembly-TeX-Worker mit einem speicherinternen Dateisystem. Eingabe, Warteschlange, Speicher, Laufzeit (15 Sekunden) und SVG-Ausgabe sind begrenzt, und Datei-E/A-Befehle werden abgelehnt.

## Zugriff auf Dokumente und Dateien

- Dokumentverknüpfungen und Dateivorgänge können die Dokumentwurzel nicht verlassen.
- Erstellen, Umbenennen, Verschieben und Löschen aus dem INDEX werden auf der Erweiterungsseite erneut geprüft – Dokumentwurzel, INDEX-Version, Pfad des Originaldokuments, Zieltyp, Grenzen symbolischer Verknüpfungen und ungespeicherte Dokumente – bevor sie angewendet werden. Anfragen aus einem veralteten Menü oder von einer anderen Dokumentwurzel werden nicht angewendet.
- Während ein Dokument bearbeitet wird oder ein anderer INDEX-Vorgang angewendet wird, sind Änderungsvorgänge am INDEX deaktiviert.
- Das Erstellen aus einer Vorlage prüft nach der Vorschau erneut die Vertrauenswürdigkeit des Arbeitsbereichs, die Identität der Dokumentwurzel, die INDEX-Version, den Standard Pack und den erzeugten Inhalt, den Speicherort sowie die Grenzen symbolischer Verknüpfungen. Es überschreibt keine bestehende Datei und erstellt keinen Inhalt, der von der Vorschau abweicht oder ein Ergebnis von mehr als 4 MiB ergibt.
- Beim Speichern einer Konfigurationsdatei wird unmittelbar zuvor die Version geprüft; wird eine externe Änderung erkannt, wird der Vorgang abgebrochen.

## Senden nach außen

- Dokumente werden zum Lesen, Bearbeiten oder Prüfen niemals nach außen gesendet. Die Dokumentprüfung läuft deterministisch auf dem Gerät.
- Nur die Übersetzung (Übersetzung dieser Seite, Sammelübersetzung) zeigt Ziel und Umfang der Übertragung vorab an und sendet Dokumente an ein Sprachmodell, wenn dies ausdrücklich genehmigt wurde. <!-- ai-only -->
- Übersetzungsvorschläge werden als Unterschied dargestellt; nach erneuter Prüfung der Version von Originaldokument und Übersetzungsziel werden sie nur angewendet, wenn eine Person sie ausdrücklich speichert. <!-- ai-only -->
- Das Spezifikationswerkzeug für KI-Agenten gibt weder den Inhalt eines Dokuments noch Namen von Arbeitsbereichen oder lokale Pfade zurück. <!-- ai-only -->

## Git

- Beim Speichern wird nur die Datei geschrieben. Keine Funktion führt automatisch ein Staging oder einen Commit in Git durch.
- Bestehende Dateien wie `_meta.json` werden niemals stillschweigend gelöscht oder geändert. Verwaiste Übersetzungen werden ebenfalls niemals automatisch gelöscht oder verschoben.

## Verwandte Themen

- [Wichtige Spezifikationen](README.md)
- [Nutzung durch KI](ai-agents.md)
