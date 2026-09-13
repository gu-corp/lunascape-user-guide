# Kaaviot, matematiikka tai kuvat eivät näy

## TikZ-kaavio näkyy kutistettuna lähdekoodina

- Jaettavassa laajennuksessa ei ole mukana TikZ:n piirtomoottoria. Tämä on normaali näkymä.
- Kehitystä ja arviointia varten: asenna `node-tikzjax` 1.0.5 luotetun työtilan juureen ja aseta asetus `lunascapeDocEditor.tikz.runtime` arvoon `workspace`, jolloin kaavio piirretään.
- Selainversio ei piirrä TikZ-kaavioita.

## Matematiikka näkyy tavallisena tekstinä

- Tarkista erotinmerkit. Rivin sisäisissä kaavoissa ne ovat `$...$` tai `\(...\)`, erillisissä kaavoissa `$$...$$` tai `\[...\]`.
- Rivin sisäisessä koodissa tai koodilohkossa oleva `$` ei muutu matematiikaksi.
- Rahasummalta näyttävää kirjoitustapaa, kuten `$5 and $10`, ei tulkita matematiikaksi.
- Erittäin suuria tai paljon makrolaajennuksia sisältäviä kaavoja ei piirretä, jos ne ylittävät rajat (`maxSize: 50`, `maxExpand: 1000`). Jaa kaava osiin.

## Kaavion kohdalla lukee ”Ei voida piirtää”

- Mermaidin, Vega-Liten, WaveDromin ja muiden virheilmoitus kertoo, missä syntaksissa on ongelma. Tarkista lähde muokkausnäkymässä valinnalla [Markdown].
- Vega-Lite: upota tiedot kohtaan `data.values` tai `datasets`. Ulkoisessa URL-osoitteessa olevia tietoja tai kuvamerkkejä ei voi käyttää.
- WaveDrom: kirjoita tiukkaa JSON-muotoa. JavaScript-muotoa (esimerkiksi lainausmerkittömiä avaimia) ei voi käyttää.
- Penrose: käytä vain alussa olevaa riviä `@preset set-theory` ja sallittuja lauseita (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- ”Luodussa SVG:ssä on turvattomia viittauksia” tai ”Luotu SVG ylittää enimmäiskoon”: kaavioita, jotka viittaavat ulkoisiin resursseihin tai jotka ovat liian suuria, ei näytetä. Vähennä sisältöä tai poista viittaukset.

## Kuva ei näy

- Anna kuvan polku suhteessa dokumenttiin. Dokumenttijuuren ulkopuolella olevia kuvia ei näytetä.
- `<img>`-elementin `width` ottaa vain numeron (`width="360"`).

## Kaaviot eivät näy viedyllä sivustolla

TikZ:n, Vega-Liten, Markmapin, WaveDromin, Svgbobin ja Penrosen piirtokirjastot ladataan vasta näytettäessä. Sijoita `vendor/`-kansio viedyn sivuston mukana.

## Aiheeseen liittyvää

- [Matematiikan kirjoittaminen](../03-editing/math.md)
- [Kaavioiden ja graafien kirjoittaminen](../03-editing/diagrams.md)
- [Kuvan koon säätäminen](../03-editing/images.md)
