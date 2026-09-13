# Diagrammer, matematik eller billeder vises ikke

## En TikZ-figur vises som sammenklappet kildekode

- Den distribuerede udvidelse indeholder ikke en TikZ-gengivelsesmotor. Dette er den forventede visning.
- Til udvikling og evaluering kan du installere `node-tikzjax` 1.0.5 i roden af en browser, du har tillid til, og sætte indstillingen `lunascapeDocEditor.tikz.runtime` til `workspace`.
- Webviseren gengiver ikke TikZ.

## Matematik vises som almindelig tekst

- Kontrollér skilletegnene: `$...$` eller `\(...\)` for indlejret matematik, `$$...$$` eller `\[...\]` for fritstående matematik.
- Et `$` inde i indlejret kode eller en kodeblok bliver aldrig til matematik.
- Beløbsagtig tekst som `$5 and $10` behandles ikke som matematik.
- Meget stor matematik eller matematik med mange makroudvidelser, som overskrider grænserne (`maxSize: 50`, `maxExpand: 1000`), gengives ikke. Del den op.

## Et diagram siger, at det ikke kan gengives

- Fejlmeddelelsen fra Mermaid, Vega-Lite, WaveDrom med flere peger på syntaksproblemet. Kontrollér kildekoden i redigeringsvinduet med [Markdown].
- Vega-Lite: indlejr data i `data.values` eller `datasets`. Eksterne data-URL'er og billedmarkeringer kan ikke bruges.
- WaveDrom: skriv streng JSON. JavaScript-formen (nøgler uden anførselstegn og lignende) kan ikke bruges.
- Penrose: brug kun `@preset set-theory` øverst og de tilladte udtryk (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „Den genererede SVG indeholder usikre referencer" / „Den genererede SVG overskrider grænsen": diagrammer, der refererer til eksterne ressourcer, eller som er for store, vises ikke. Reducér indholdet, eller fjern referencerne.

## Et billede vises ikke

- Billedstier er relative til dokumentet. Billeder uden for dokumentroden vises ikke.
- `width` for et `<img>` tager kun et tal (`width="360"`).

## Diagrammer mangler på et eksporteret websted

Gengivelsesbibliotekerne til TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob og Penrose indlæses efter behov. Placér `vendor/`-mappen sammen med det eksporterede websted.

## Relaterede emner

- [Skrive matematik](../03-editing/math.md)
- [Skrive diagrammer og grafer](../03-editing/diagrams.md)
- [Justere billedstørrelse](../03-editing/images.md)
