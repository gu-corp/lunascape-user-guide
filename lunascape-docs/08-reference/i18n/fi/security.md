# Tietoturva ja kirjoitusrajat

Rajat, joita Lunascape Docs ylläpitää suojatakseen dokumenttisi ja laitteesi.

## Näyttäminen

- Markdownista luotu HTML ja kaavioista luotu SVG puhdistetaan DOMPurify 3.4.14:llä ennen näyttämistä.
- MDX:n sisältämiä mielivaltaisia skriptejä ei suoriteta.
- KaTeX suoritetaan asetuksilla `trust: false`, `maxSize: 50` ja `maxExpand: 1000`, eikä se luota ulkoiseen HTML:ään eikä mielivaltaisiin komentoihin.
- Markmapin, WaveDromin, Svgbobin, Vega-Liten ja Penrosen piirtokirjastot ladataan laitteessa kiinnitettyinä versioina vain silloin, kun vastaava lohko on olemassa. Viittaukset ulkoisiin resursseihin, raaka HTML ja suoritettavat merkinnät eivät ole sallittuja, ja luodusta SVG:stä poistetaan skriptit, ulkoiset kuvat sekä `link`, `style` ja `foreignObject`.
- TikZ-piirto ei käynnistä koneen LaTeXia, vaan se suoritetaan peräkkäin WebAssembly-pohjaisessa TeX-työntekijässä, jolla on muistinvarainen tiedostojärjestelmä. Syötteelle, jonolle, muistille, suoritusajalle (15 sekuntia) ja SVG-tulosteelle on ylärajat, ja tiedosto-I/O-käskyt hylätään.

## Pääsy dokumentteihin ja tiedostoihin

- Dokumenttien linkit ja tiedostotoiminnot eivät pääse dokumenttijuuren ulkopuolelle.
- INDEXistä tehtävät luonnit, uudelleennimeämiset, siirrot ja poistot tarkistetaan laajennuksen puolella uudelleen — dokumenttijuuri, INDEXin versio, alkuperäisdokumentin polku, kohteen tyyppi, symbolisten linkkien rajat ja tallentamattomat dokumentit — ennen kuin ne otetaan käyttöön. Vanhentuneesta valikosta tai toisesta dokumenttijuuresta tulevia toimintopyyntöjä ei oteta käyttöön.
- INDEXin muokkaustoiminnot ovat pois käytöstä, kun dokumenttia muokataan tai kun toista INDEX-toimintoa otetaan käyttöön.
- Mallista luominen tarkistaa esikatselun jälkeen uudelleen työtilan luotettavuuden, dokumenttijuuren todellisuuden, INDEXin version, Standard Packin ja luotavan sisällön, tallennuskohteen sekä symbolisten linkkien rajat. Se ei korvaa olemassa olevaa tiedostoa eikä luo sisältöä, joka poikkeaa esikatselusta tai jonka purettu koko ylittää 4 MiB.
- Asetustiedoston tallennus tarkistaa version välittömästi ennen tallennusta ja keskeytyy, jos ulkoinen muutos havaitaan.

## Lähettäminen ulkopuolelle

- Dokumentteja ei lähetetä ulkopuolelle lukemista, muokkaamista tai tarkistamista varten. Dokumenttitarkistukset suoritetaan laitteessa deterministisesti.
- Vain käännös (tämän sivun käännös, eräkäännös) lähettää dokumentteja kielimallille: se näyttää ensin kohteen ja lähetettävän laajuuden ja lähettää vain nimenomaisesti hyväksyttynä. <!-- ai-only -->
- Käännösehdotukset esitetään erotuksena, ja alkuperäisdokumentin ja kohteen versiot tarkistetaan uudelleen; ehdotus otetaan käyttöön vain, kun ihminen tallentaa sen nimenomaisesti. <!-- ai-only -->
- AI-agenteille tarkoitettu määrittelytyökalu ei palauta dokumenttien sisältöä, työtilojen nimiä eikä paikallisia polkuja. <!-- ai-only -->

## Git

- Tallennus vain kirjoittaa tiedostoon. Mikään toiminto ei lisää muutoksia Gitin valmistelualueelle eikä tee commitia automaattisesti.
- Olemassa olevia tiedostoja, kuten `_meta.json`, ei poisteta eikä muuteta hiljaisesti. Myöskään orpoja käännösversioita ei poisteta eikä siirretä automaattisesti.

## Aiheeseen liittyvää

- [Tärkeimmät määrittelyt](README.md)
- [Käyttö tekoälystä](ai-agents.md)
