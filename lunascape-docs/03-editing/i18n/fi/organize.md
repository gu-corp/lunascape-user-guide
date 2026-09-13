# Dokumenttien ja kansioiden luominen ja järjestäminen

INDEX-paneelin kohdevalikosta voit luoda, monistaa, nimetä uudelleen ja poistaa dokumentteja ja kansioita. Tiedot syötetään pienessä valintaikkunassa katseluohjelman sisällä, joten lukeminen ei keskeydy.

> **Huomautus**
>
> Nämä toiminnot ovat käytettävissä vain, kun työtila on luotettu VS Codessa. Niitä ei voi suorittaa dokumentin muokkauksen aikana, toisen toiminnon ollessa käynnissä eikä silloin, kun kohteessa on tallentamattomia muutoksia.

## Dokumentin tai kansion luominen

1. Avaa kohdekansion kohdevalikko ([⋯] tai napsautus hiiren kakkospainikkeella).
   Jos haluat luoda kohteen suoraan dokumenttijuureen, käytä INDEX-otsikon oikeassa reunassa olevaa [⋯]-painiketta tai napsauta INDEX-paneelin tyhjää kohtaa hiiren kakkospainikkeella.
2. Valitse [Uusi dokumentti] tai [Uusi kansio].
3. Kirjoita nimi ja paina [Luo].
   Dokumentin nimessä on oltava Markdown-tiedostopääte (`.md`, `.markdown`, `.mdx` ja niin edelleen).

Uudet dokumentit luodaan oletuskielen dokumentteina (alkuperäisdokumentteina).

## Dokumentin monistaminen

1. Avaa dokumentin kohdevalikko ja valitse [Monista].
2. Kirjoita uusi nimi ja paina [Luo].

Vain alkuperäisdokumentti monistetaan; sen käännöksiä ei monisteta.

## Otsikon muuttaminen

Muuttaa dokumentin otsikkoa (H1). Tiedoston nimi pysyy ennallaan.

1. Avaa dokumentin tai kansion kohdevalikko ja valitse [Muuta otsikkoa].
2. Kirjoita uusi otsikko yhdelle riville ja paina [Muuta].

Kansion kohdalla muutetaan sen `README.md`-tiedoston otsikkoa. Kun näkyvissä on käännös, muutetaan kyseisen kielen dokumentin otsikko.

## Dokumentin nimen muuttaminen

Muuttaa työkalurivillä näkyvää dokumentin nimeä (dokumenttijuuren nimeä).

1. Napsauta työkalurivin dokumentin nimeä hiiren kakkospainikkeella. Sama valikko avautuu myös INDEX-otsikon oikeassa reunassa olevasta [⋯]-painikkeesta.
2. Valitse [Muuta dokumentin nimeä] ja kirjoita uusi nimi.

Kun mitään ei ole määritetty, näkyvissä on kansion nimi sellaisenaan.

Asettamasi nimi kirjoitetaan **siihen paikkaan, josta dokumentin nimi tällä hetkellä tulee**, jotta näkyvissä oleva otsikko ei jää huomiotta.

| Nykytilanne | Kirjoituskohde |
|---|---|
| `lunascape-docs.json` sisältää nimen | `lunascape-docs.json` päivitetään |
| Nimeä ei ole, mutta dokumenttijuuressa on README | README-tiedoston otsikko (H1) kirjoitetaan uudelleen |
| Kumpaakaan ei ole | `lunascape-docs.json` luodaan ja nimi tallennetaan siihen |

Muutoksen jälkeen näkyvässä viestissä kerrotaan, kumpaan nimi kirjoitettiin.

> **Vihje**
>
> Dokumentin nimi määräytyy tässä järjestyksessä: `lunascape-docs.json`-tiedoston nimi, sitten dokumenttijuuren README-tiedoston otsikko, sitten kansion nimi.

## Tiedoston tai kansion nimen muuttaminen

1. Avaa kohdevalikko ja valitse [Muuta tiedoston nimeä] tai [Muuta kansion nimeä].
2. Kirjoita uusi nimi ja paina [Muuta].

Vastaavat käännökset (sama polku hakemistossa `i18n/<kieli>/`) nimetään uudelleen samalla.

## Poistaminen

1. Avaa kohdevalikko ja valitse [Siirrä roskakoriin].
2. Tarkista vahvistusviestin sisältö ja hyväksy siirto.

Kohde siirretään käyttöjärjestelmän roskakoriin, joten sen voi tarvittaessa palauttaa. Käännöksiä ei poisteta, vaan ne jäävät paikoilleen.

## Nimet, joita ei voi käyttää

- Nimet, jotka alkavat merkillä `.` (ne eivät näkyisi INDEX-paneelissa)
- `i18n` (varattu käännöstiedostoille)
- Windowsin varaamat nimet (`CON`, `PRN` ja niin edelleen)
- Nimet, jotka päättyvät pisteeseen tai välilyöntiin
- Nimet, joissa on ohjausmerkkejä tai tiedostonimissä kiellettyjä merkkejä
- Nimet, jotka ovat jo samassa kansiossa (mukaan lukien nimet, jotka eroavat vain kirjainkoon osalta)

> **Huomautus**
>
> Aloitussivun (yleensä juuren `README.md`) nimeä ei voi muuttaa eikä sivua siirtää. Muuta ensin `startPage`-asetusta tiedostossa `lunascape-docs.json`.

## Aiheeseen liittyvää

- [Dokumenttien järjestyksen muuttaminen](reorder.md)
- [INDEX-paneelin käyttäminen](../02-reading/index-panel.md)
