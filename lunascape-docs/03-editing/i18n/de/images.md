# Bildgröße anpassen

In ein Dokument eingefügte Bilder passen sich automatisch an die Breite des Textes und die Höhe des Bildschirms an. Für ein Bild, das in einer bestimmten Größe erscheinen soll, können Sie die Breite festlegen.

## So funktioniert die automatische Anpassung

- Ein gewöhnliches Markdown-Bild (`![Beschreibung](./images/screen.png)`) wird so verkleinert, dass es in die Textbreite passt. Es wird nie über seine ursprüngliche Größe hinaus vergrößert.
- Ein hochformatiger Screenshot wird auf 72 % der Bildschirmhöhe oder 720px begrenzt, je nachdem, welcher Wert kleiner ist.

## Die Breite im Editor festlegen

1. Drücken Sie [Bearbeiten] und wählen Sie das Bild in der visuellen Ansicht aus.
2. Wählen Sie eine Breite unter [Bildgröße] in der Symbolleiste.
3. Drücken Sie [Speichern].

| Option | Breite |
|---|---|
| [Automatisch] | Nicht festgelegt (automatische Anpassung) |
| [Klein (360px)] | 360px |
| [Mittel (560px)] | 560px |
| [Groß (760px)] | 760px |
| [Textbreite (920px)] | 920px |
| [Benutzerdefiniert…] | Beliebige Ganzzahl von 16 bis 4096px |

## Die Breite in Markdown festlegen

Geben Sie dem HTML-`img`-Tag eine numerische `width`. Diese Schreibweise wird auch auf GitHub und in MDX als Bild dargestellt.

```html
<img src="./images/screen.png" alt="Einstellungsbildschirm" width="360" />
```

> **Hinweis**
>
> - `width` nimmt nur eine Zahl entgegen, ohne `px` oder `%`. Ein Wert, der größer als die Textbreite ist, passt sich bei der Anzeige trotzdem an die Textbreite an.
> - Bildpfade sind relativ zum Dokument. Bilder außerhalb der Dokumentwurzel werden nicht angezeigt.

## Verwandte Themen

- [Ein Dokument bearbeiten](README.md)
- [Diagramme, Formeln oder Bilder werden nicht dargestellt](../07-troubleshooting/rendering.md)
