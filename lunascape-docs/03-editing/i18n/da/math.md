# Skrive matematik

Matematik skrives i TeX-notation og gengives på din enhed med KaTeX. Der bruges ikke netværk.

## Notation

| Type | Skilletegn | Eksempel |
|---|---|---|
| Matematik i teksten (inline) | `$...$` eller `\(...\)` | `Sammenhængen mellem masse og energi er $E = mc^2$.` |
| Matematik på egen linje (display) | `$$...$$` eller `\[...\]` | Se nedenfor |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Der skal ikke være mellemrum omkring skilletegnene. Matematik, der støder direkte op til japansk tekst, f.eks. `値は$V=-H$である`, genkendes også.
- Et `$` inde i kode i teksten eller i en kodeblok behandles ikke som matematik og vises, som det står.
- Beløbslignende skrivemåder som `$5 and $10` opfattes ikke som matematik.

## Rediger

I den visuelle visning vises matematik som det færdige resultat. Du ændrer indholdet ved at trykke på [Markdown] i redigeringsvisningen og rette kilden. Når du gemmer fra den visuelle visning, bevares TeX-kilden og de oprindelige skilletegn (`$` eller `\(`) uændret.

> **Bemærk**
>
> - Af hensyn til sikkerheden kører KaTeX med `trust: false` og har grænser for størrelse (`maxSize: 50`) og antal makroudvidelser (`maxExpand: 1000`). Matematik ud over disse grænser gengives ikke.
> - Et `tikzpicture` skrevet inde i `$$...$$` eller `\[...\]` i et eksisterende dokument genkendes som et TikZ-diagram og ikke som matematik.

## Relaterede emner

- [Skrive diagrammer og grafer](diagrams.md)
- [Diagrammer, matematik eller billeder vises ikke](../07-troubleshooting/rendering.md)
