# Diagrammer, matematikk eller bilder vises ikke

## En TikZ-figur vises som sammenfoldet kildekode

- Den distribuerte utvidelsen inkluderer ikke en tegnemotor for TikZ. Dette er forventet visning.
- For utvikling og evaluering kan du installere `node-tikzjax` 1.0.5 i roten av et klarert arbeidsområde og sette `lunascapeDocEditor.tikz.runtime` til `workspace`.
- Webviseren tegner ikke TikZ.

## Matematikk vises som ren tekst

- Kontroller skilletegnene: `$...$` eller `\(...\)` for innebygd, `$$...$$` eller `\[...\]` for frittstående matematikk.
- En `$` inne i innebygd kode eller en kodeblokk blir aldri matematikk.
- Beløpslignende tekst som `$5 and $10` behandles ikke som matematikk.
- Svært stor matematikk eller mye makroutvidelse som går ut over grensene (`maxSize: 50`, `maxExpand: 1000`) tegnes ikke. Del den opp.

## Et diagram sier at det ikke kan tegnes

- Feilmeldingen fra Mermaid, Vega-Lite, WaveDrom med flere peker på syntaksproblemet. Kontroller kildekoden i redigeringsvinduet med [Markdown].
- Vega-Lite: bygg inn data i `data.values` eller `datasets`. Eksterne data-URL-er og bildemerker kan ikke brukes.
- WaveDrom: skriv streng JSON. JavaScript-formen (nøkler uten anførselstegn og så videre) kan ikke brukes.
- Penrose: bruk bare `@preset set-theory` øverst og de tillatte setningene (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- «Den genererte SVG-en inneholder usikre referanser» / «Den genererte SVG-en overskrider grensen»: diagrammer som refererer til eksterne ressurser, eller som er for store, vises ikke. Reduser innholdet eller fjern referansene.

## Et bilde vises ikke

- Bildebaner angis som relative baner fra dokumentet. Bilder utenfor dokumentroten vises ikke.
- `width` for en `<img>` tar bare et tall (`width="360"`).

## Diagrammer mangler på et eksportert nettsted

Tegnebibliotekene for TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob og Penrose lastes ved behov. Plasser `vendor/`-mappen sammen med det eksporterte nettstedet.

## Relaterte emner

- [Skrive matematikk](../03-editing/math.md)
- [Skrive diagrammer og grafer](../03-editing/diagrams.md)
- [Justere bildestørrelse](../03-editing/images.md)
