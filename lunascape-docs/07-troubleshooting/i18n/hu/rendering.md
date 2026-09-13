# Az ábrák, a képletek vagy a képek nem jelennek meg

## A TikZ-ábra összecsukott forrásként jelenik meg

- A terjesztett bővítmény nem tartalmaz TikZ-megjelenítő motort. Ez a megjelenés a normális.
- Fejlesztési és kiértékelési célra telepítse a `node-tikzjax` 1.0.5 csomagot egy megbízható munkaterület gyökerébe, és állítsa a `lunascapeDocEditor.tikz.runtime` beállítást `workspace` értékre.
- A webes megjelenítő nem rajzolja ki a TikZ-ábrákat.

## A képletek szövegként jelennek meg

- Ellenőrizze az elválasztójeleket: soron belül `$...$` vagy `\(...\)`, önálló képlethez `$$...$$` vagy `\[...\]`.
- A soron belüli kódban vagy kódblokkban lévő `$` soha nem lesz képlet.
- A pénzösszegre emlékeztető írásmód, például a `$5 and $10`, nem számít képletnek.
- A nagyon nagy vagy sok makrót kibontó képletek a korlátok (`maxSize: 50`, `maxExpand: 1000`) átlépése esetén nem jelennek meg. Bontsa őket részekre.

## Az ábránál az szerepel, hogy nem rajzolható ki

- A Mermaid, a Vega-Lite, a WaveDrom és a többi eszköz hibaüzenete megmutatja a szintaktikai hibát. A forrást a szerkesztőben a [Markdown] gombbal nézheti meg.
- Vega-Lite: az adatokat a `data.values` vagy a `datasets` mezőbe ágyazza be. Külső URL-ről származó adatok és képjelölők nem használhatók.
- WaveDrom: szigorú JSON formátumban írja. A JavaScript-forma (például az idézőjelek nélküli kulcsok) nem használható.
- Penrose: csak az elején álló `@preset set-theory` sort és az engedélyezett utasításokat (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`) használja.
- „A létrehozott SVG nem biztonságos hivatkozásokat tartalmaz”, „A létrehozott SVG meghaladja a korlátot”: a külső erőforrásokra hivatkozó vagy túl nagy ábrák nem jelennek meg. Csökkentse a tartalmat, vagy távolítsa el a hivatkozásokat.

## Egy kép nem jelenik meg

- A képek elérési útját a dokumentumhoz képest relatívan adja meg. A dokumentumgyökéren kívüli képek nem jelennek meg.
- Az `<img>` elem `width` értékeként csak számot adjon meg (`width="360"`).

## Az exportált webhelyen nem látszanak az ábrák

A TikZ, a Vega-Lite, a Markmap, a WaveDrom, a Svgbob és a Penrose megjelenítő programkönyvtárai megjelenítéskor töltődnek be. Az exportált webhellyel együtt a `vendor/` mappát is telepítse.

## Kapcsolódó témák

- [Képletek írása](../03-editing/math.md)
- [Ábrák és diagramok írása](../03-editing/diagrams.md)
- [Képek méretezése](../03-editing/images.md)
