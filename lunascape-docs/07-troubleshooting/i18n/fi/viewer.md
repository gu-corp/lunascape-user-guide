# Dokumentit eivät näy

## Näkyviin tulee ”Avattavaa Markdown-tiedostoa tai docs-kansiota ei löydy”

- Työtilassa ei ole `docs`-kansiota, tai kansiolla on jokin muu nimi.
  - Sijoita `lunascape-docs.json` kyseiseen kansioon, niin se tunnistetaan dokumenttijuureksi nimestä riippumatta.
  - Tai lisää kansion nimi asetukseen `lunascapeDocEditor.rootDirectoryNames`.
- Jos dokumentteja ei vielä ole, luo ne komennolla ”Lunascape Docs: Luo dokumentaatio mallista”.
- Voit myös avata Markdown-tiedoston editorissa ja suorittaa komennon ”Lunascape Docs: Avaa määrittelykatselimessa”.

## Dokumentti ei näy INDEX-paneelissa

- Tarkista, että tiedostopääte on `.md`, `.markdown` tai `.mdx`.
- Seuraavat kansiot eivät näy: `.`-merkillä alkavat kansiot, `node_modules` ja `ignoredDirectories`-asetuksessa määritetyt kansiot (oletus `99-archive`).
- `i18n/`-kansion alla olevat käännökset eivät näy erikseen INDEX-paneelissa. Vaihda niihin kielivalikosta.
- Jos juuri lisäämäsi tiedosto ei näy, paina [Lataa uudelleen].
- Katselet ehkä toista dokumenttijuurta. Tarkista dokumenttijuuren nimi työkalurivin vasemmasta reunasta.

## Kansion painaminen ei näytä mitään

Kansion `README.md` on ”vain asetuksia varten tarkoitettu kuvaus”, jossa on front matter mutta ei leipätekstiä. Avaa kansio INDEX-paneelissa ja valitse sen sisältä dokumentti.

## Avautuu väärä dokumenttijuuri

- Jos asetus `lunascapeDocEditor.rootMode` on `fixed`, avautuu aina `lunascapeDocEditor.root`.
- Asetuksella `auto` valitaan avattua Markdown-tiedostoa lähinnä oleva dokumenttijuuri. Voit vaihtaa sen työkalurivin vasemman reunan pudotusvalikosta.

## Dokumenttijuuren nimi ei ole odotettu

Nimi määräytyy järjestyksessä `lunascape-docs.json`-tiedoston `title` → juuren `README.md`-tiedoston `navigation.title` → sen H1 → `index.md` → kansion nimi. Jos haluat kiinnittää nimen, aseta `title`.

## INDEX katosi

- Dokumenttijuuressa, jossa on vain yksi dokumentti, INDEX sulkeutuu automaattisesti ensimmäisellä kerralla. Voit avata sen työkalurivin sarakekuvakkeesta. Voit poistaa toiminnon käytöstä kohdasta [Näyttöasetukset] > [Piilota, kun dokumentteja on vain yksi].
- Kapealla näytöllä avaa se [Takaisin]-painikkeen vasemmalla puolella olevasta painikkeesta [Avaa INDEX] (kolme viivaa).

## Linkki ei aukea

- ”Linkin kohdetta ei löydy”: linkin kohdetiedostoa ei ole. Voit tarkistaa sisäiset linkit dokumenttityökalujen [Tarkistus]-toiminnolla.
- ”Turvatonta tai tukematonta linkkiä ei avattu”: dokumenttijuuren ulkopuolelle vieviä linkkejä tai muita kuin `https://`- ja `mailto:`-skeemoja ei avata.

## Näkyvä kieli ei ole odotettu

- Tarkista kielivalikosta näkyvän sivun kieli ja sen peruste.
- Viimeksi valitsemasi näyttökieli muistetaan. Valitse oletuskieli uudelleen kielivalikosta.
- Jos henkilökohtainen asetus `lunascapeDocEditor.locale` on määritetty, kyseisen kielen käännös on etusijalla.

## Aiheeseen liittyvää

- [Dokumenttijuuren vaihtaminen](../02-reading/roots.md)
- [Dokumenttijuuret ja tiedostokäytännöt](../04-document-tools/structure.md)
