# Diagramy, vzorce nebo obrázky se nezobrazují

## Obrázek TikZ se zobrazí jako sbalený zdrojový kód

- Distribuované rozšíření neobsahuje vykreslovací engine pro TikZ. Jde o očekávané zobrazení.
- Pro vývoj a vyhodnocení nainstalujte `node-tikzjax` 1.0.5 přímo do kořene důvěryhodného pracovního prostoru a nastavte `lunascapeDocEditor.tikz.runtime` na `workspace`.
- Webový prohlížeč TikZ nevykresluje.

## Vzorce se zobrazují jako prostý text

- Zkontrolujte oddělovače: pro vzorce v textu `$...$` nebo `\(...\)`, pro samostatné vzorce `$$...$$` nebo `\[...\]`.
- Znak `$` uvnitř kódu v textu nebo v bloku kódu se nikdy nestane vzorcem.
- Zápis připomínající peněžní částku, například `$5 and $10`, se jako vzorec nezpracuje.
- Velmi rozsáhlé vzorce nebo vzorce s mnoha rozvinutými makry se při překročení limitů (`maxSize: 50`, `maxExpand: 1000`) nevykreslí. Rozdělte je.

## U diagramu se objeví hlášení, že jej nelze vykreslit

- Chybová zpráva z Mermaid, Vega-Lite, WaveDrom a dalších ukazuje na problém v syntaxi. Zdrojový kód zkontrolujte v editoru pomocí [Markdown].
- Vega-Lite: data vložte do `data.values` nebo `datasets`. Externí adresy URL s daty ani obrázkové značky použít nelze.
- WaveDrom: pište striktní JSON. Zápis ve tvaru JavaScriptu (klíče bez uvozovek a podobně) použít nelze.
- Penrose: používejte pouze `@preset set-theory` na začátku a povolené příkazy (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „Vygenerovaný SVG obsahuje nebezpečné odkazy“ / „Vygenerovaný SVG překračuje limit“: diagramy, které odkazují na externí zdroje, nebo které jsou příliš velké, se nezobrazí. Zmenšete jejich obsah nebo odkazy odstraňte.

## Obrázek se nezobrazuje

- Cesty k obrázkům se zadávají relativně vůči dokumentu. Obrázky mimo kořen dokumentace se nezobrazí.
- Atribut `width` u `<img>` přijímá pouze číslo (`width="360"`).

## Na exportovaném webu chybí diagramy

Vykreslovací knihovny pro TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob a Penrose se načítají až při zobrazení. Spolu s exportovaným webem nasaďte i složku `vendor/`.

## Související témata

- [Psaní vzorců](../03-editing/math.md)
- [Psaní diagramů a grafů](../03-editing/diagrams.md)
- [Úprava velikosti obrázků](../03-editing/images.md)
