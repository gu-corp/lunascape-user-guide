# Skriva matematik

Matematik skrivs med TeX-notation och renderas på enheten med KaTeX. Inget nätverk används.

## Notation

| Typ | Avgränsare | Exempel |
|---|---|---|
| Infogad matematik (i löpande text) | `$...$` eller `\(...\)` | `Sambandet mellan massa och energi uttrycks som $E = mc^2$.` |
| Fristående matematik (på egen rad) | `$$...$$` eller `\[...\]` | Se nedan |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Det behövs inga blanksteg runt avgränsarna. Matematik som står direkt intill japansk text, till exempel `値は$V=-H$である`, känns igen.
- Ett `$` inuti infogad kod eller ett kodblock behandlas inte som matematik utan visas som det är.
- Text som ser ut som belopp, till exempel `$5 and $10`, behandlas inte som matematik.

## Redigera

I den visuella vyn visas matematiken som renderat resultat. Tryck på [Markdown] i redigeringsvyn och redigera källtexten för att ändra innehållet. När du sparar från den visuella vyn behålls TeX-källan och den ursprungliga formen på avgränsarna (`$` eller `\(`) oförändrade.

> **Obs!**
>
> - Av säkerhetsskäl körs KaTeX med `trust: false` och har gränser för storlek (`maxSize: 50`) och antal makroexpansioner (`maxExpand: 1000`). Matematik som överskrider dessa gränser renderas inte.
> - En `tikzpicture` som i ett befintligt dokument är skriven inuti `$$...$$` eller `\[...\]` känns igen som en TikZ-figur, inte som matematik.

## Relaterade avsnitt

- [Skriva diagram och grafer](diagrams.md)
- [Diagram, matematik eller bilder visas inte](../07-troubleshooting/rendering.md)
