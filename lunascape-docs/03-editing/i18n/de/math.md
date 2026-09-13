# Formeln schreiben

Formeln werden in TeX-Notation geschrieben und mit KaTeX auf dem Gerät dargestellt. Es wird kein Netzwerk verwendet.

## Schreibweise

| Art | Notation | Beispiel |
|---|---|---|
| Formel im Text (innerhalb eines Satzes) | `$...$` oder `\(...\)` | `Masse und Energie hängen über $E = mc^2$ zusammen.` |
| Abgesetzte Formel (in einer eigenen Zeile) | `$$...$$` oder `\[...\]` | siehe unten |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Um die Trennzeichen herum sind keine Leerzeichen nötig. Auch direkt an japanischen Text angrenzende Formeln wie `値は$V=-H$である` werden erkannt.
- Ein `$` innerhalb von Inline-Code oder eines Codeblocks wird nicht als Formel behandelt, sondern unverändert angezeigt.
- Geldbeträge wie `$5 and $10` werden nicht als Formel behandelt.

## Bearbeiten

In der visuellen Ansicht werden Formeln als fertige Darstellung angezeigt. Um den Inhalt zu ändern, drücken Sie im Bearbeitungsfenster auf [Markdown] und bearbeiten Sie die Quelle. Beim Speichern aus der visuellen Ansicht bleiben der TeX-Quelltext und die ursprüngliche Form der Trennzeichen (`$` oder `\(`) unverändert erhalten.

> **Hinweis**
>
> - Aus Sicherheitsgründen läuft KaTeX mit `trust: false` und begrenzt die Größe (`maxSize: 50`) sowie die Anzahl der Makroerweiterungen (`maxExpand: 1000`). Formeln, die diese Grenzen überschreiten, werden nicht dargestellt.
> - Ein `tikzpicture`, das in einem vorhandenen Dokument innerhalb von `$$...$$` oder `\[...\]` steht, wird als TikZ-Abbildung erkannt, nicht als Formel.

## Verwandte Themen

- [Diagramme und Grafiken schreiben](diagrams.md)
- [Diagramme, Formeln oder Bilder werden nicht angezeigt](../07-troubleshooting/rendering.md)
