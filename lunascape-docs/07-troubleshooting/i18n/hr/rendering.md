# Dijagrami, matematički izrazi ili slike se ne prikazuju

## TikZ dijagram prikazuje se kao sažeti izvorni kod

- Distribuirano proširenje ne sadrži TikZ pogon za iscrtavanje. To je očekivani prikaz.
- Za potrebe razvoja i evaluacije instalirajte `node-tikzjax` 1.0.5 izravno u korijen pouzdanog radnog prostora i postavku `lunascapeDocEditor.tikz.runtime` postavite na `workspace`, čime se omogućuje iscrtavanje.
- U web-pregledniku TikZ se ne iscrtava.

## Matematički izrazi prikazuju se kao običan tekst

- Provjerite graničnike. Za izraze u retku upotrijebite `$...$` ili `\(...\)`, a za samostalne izraze `$$...$$` ili `\[...\]`.
- Znak `$` unutar koda u retku ili unutar bloka koda ne postaje matematički izraz.
- Zapisi nalik na novčane iznose, primjerice `$5 and $10`, ne tumače se kao matematički izrazi.
- Vrlo veliki izrazi ili izrazi s mnogo proširenja makronaredbi ne iscrtavaju se ako premaše ograničenja (`maxSize: 50`, `maxExpand: 1000`). Podijelite ih na manje dijelove.

## Dijagram javlja da se ne može iscrtati

- Poruka o pogrešci iz alata Mermaid, Vega-Lite, WaveDrom i drugih upućuje na problem u sintaksi. Izvorni kod provjerite u uređivaču pomoću [Markdown].
- Vega-Lite: podatke ugradite u `data.values` ili `datasets`. Podaci s vanjskih URL-ova i oznake slika ne mogu se upotrebljavati.
- WaveDrom: pišite u strogom JSON zapisu. Zapis u obliku JavaScripta (ključevi bez navodnika i slično) ne može se upotrebljavati.
- Penrose: upotrebljavajte samo `@preset set-theory` na početku i dopuštene izjave (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „Generirani SVG sadrži nesigurne reference” / „Generirani SVG premašuje ograničenje”: dijagrami koji upućuju na vanjske resurse ili su preveliki ne prikazuju se. Smanjite sadržaj ili uklonite reference.

## Slika se ne prikazuje

- Putanju do slike navedite kao relativnu putanju u odnosu na dokument. Slike izvan korijena dokumentacije ne prikazuju se.
- Atribut `width` elementa `<img>` prima samo broj (`width="360"`).

## Dijagrami nedostaju na izvezenom web-mjestu

Biblioteke za iscrtavanje za TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob i Penrose učitavaju se pri prikazu. Uz izvezeno web-mjesto postavite i mapu `vendor/`.

## Povezane teme

- [Pisanje matematičkih izraza](../03-editing/math.md)
- [Pisanje dijagrama i grafikona](../03-editing/diagrams.md)
- [Prilagodba veličine slika](../03-editing/images.md)
