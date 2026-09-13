# Diagram, matematik eller bilder visas inte

## En TikZ-figur visas som ihopfälld källkod

- Den distribuerade tillägget innehåller ingen renderingsmotor för TikZ. Detta är den förväntade visningen.
- För utveckling och utvärdering kan du installera `node-tikzjax` 1.0.5 direkt under en betrodd arbetsyta och ställa in inställningen `lunascapeDocEditor.tikz.runtime` på `workspace`.
- I webbläsarversionen renderas inte TikZ.

## Matematik visas som vanlig text

- Kontrollera avgränsarna. Infogad matematik skrivs `$...$` eller `\(...\)`, fristående matematik `$$...$$` eller `\[...\]`.
- Ett `$` inuti infogad kod eller ett kodblock blir aldrig matematik.
- Text som ser ut som belopp, till exempel `$5 and $10`, behandlas inte som matematik.
- Mycket stor matematik eller matematik med många makroexpansioner renderas inte när gränserna (`maxSize: 50`, `maxExpand: 1000`) överskrids. Dela upp den.

## Ett diagram säger att det inte kan renderas

- Felmeddelandet från Mermaid, Vega-Lite, WaveDrom med flera pekar ut syntaxproblemet. Kontrollera källkoden i redigeringsvyn med [Markdown].
- Vega-Lite: bädda in data i `data.values` eller `datasets`. Data från externa URL:er och bildmärken går inte att använda.
- WaveDrom: skriv strikt JSON. JavaScript-formen (nycklar utan citattecken och så vidare) går inte att använda.
- Penrose: använd bara `@preset set-theory` överst och de tillåtna satserna (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- ”Den genererade SVG-filen innehåller osäkra referenser” / ”Den genererade SVG-filen överskrider gränsen”: diagram som refererar till externa resurser, eller som är för stora, visas inte. Minska innehållet eller ta bort referenserna.

## En bild visas inte

- Sökvägen till en bild anges relativt dokumentet. Bilder utanför dokumentroten visas inte.
- `width` i `<img>` anges bara som ett tal (`width="360"`).

## Diagram saknas på en exporterad webbplats

Renderingsbiblioteken för TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob och Penrose läses in vid visningen. Placera även mappen `vendor/` tillsammans med den exporterade webbplatsen.

## Relaterade ämnen

- [Skriva matematik](../03-editing/math.md)
- [Skriva diagram och grafer](../03-editing/diagrams.md)
- [Justera bildstorlek](../03-editing/images.md)
