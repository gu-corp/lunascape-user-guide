# Skrive matematikk

Matematikk skrives i TeX-notasjon og tegnes opp på enheten din med KaTeX. Nettverket brukes ikke.

## Notasjon

| Type | Skilletegn | Eksempel |
|---|---|---|
| Innebygd matematikk (i en setning) | `$...$` eller `\(...\)` | `Masse og energi henger sammen ved $E = mc^2$.` |
| Frittstående matematikk (på egen linje) | `$$...$$` eller `\[...\]` | Se nedenfor |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Det trengs ingen mellomrom rundt skilletegnene. Matematikk som står rett inntil japansk tekst, for eksempel `値は$V=-H$である`, blir gjenkjent.
- En `$` inne i innebygd kode eller en kodeblokk beholdes som ren tekst.
- Beløpslignende tekst som `$5 and $10` behandles ikke som matematikk.

## Redigere

I visuell visning vises matematikk opptegnet. For å endre den trykker du [Markdown] i redigeringsvisningen og redigerer kilden. Når du lagrer fra visuell visning, beholdes TeX-kilden og den opprinnelige formen på skilletegnet (`$` eller `\(`) uendret.

> **Merk**
>
> - Av sikkerhetsgrunner kjører KaTeX med `trust: false` og har grenser for størrelse (`maxSize: 50`) og antall makroutvidelser (`maxExpand: 1000`). Matematikk som overskrider disse grensene, tegnes ikke opp.
> - En `tikzpicture` skrevet inne i `$$...$$` eller `\[...\]` i et eksisterende dokument gjenkjennes som et TikZ-diagram, ikke som matematikk.

## Relaterte emner

- [Skrive diagrammer og grafer](diagrams.md)
- [Diagrammer, matematikk eller bilder vises ikke](../07-troubleshooting/rendering.md)
