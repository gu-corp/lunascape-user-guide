# INDEXin käyttö

Näytön vasemmassa reunassa oleva INDEX on puunäkymä dokumenttijuuren kansioista ja dokumenteista.

## Rajaaminen

1. Kirjoita sana INDEXin yläpuolella olevaan kenttään [Rajaa dokumentteja].
2. Näkyviin jäävät vain ne kohteet, joiden dokumentin nimi täsmää. Kun tyhjennät kentän, kaikki palaa näkyviin.

> **Huomautus**
>
> Rajauksen ollessa käytössä järjestystä ei voi muuttaa vetämällä ja pudottamalla.

## Kansioiden avaaminen ja sulkeminen

- Paina kansion nimen vasemmalla puolella olevaa nuolta tai sellaisen kansion nimeä, jolla ei ole kansilehteä, niin kansio avautuu tai sulkeutuu.
- Jos kansiolla on kansilehti (`README.md` tai `index.md`, jossa on leipätekstiä), nimen painaminen avaa kansilehden. Jos haluat vain avata tai sulkea kansion, käytä kohdevalikon kohtaa [Avaa kansio] / [Sulje kansio].
- Kansioiden avaustila muistetaan käyttäjäkohtaisesti, eikä sitä kirjoiteta Gitin hallinnoimiin tiedostoihin.

## README ja kansion kansilehti

`README.md` on tiedosto, joka kertoo, mitä kansio sisältää.

- Kun kansiolla on README, kansion nimen painaminen näyttää kyseisen READMEn.
- Jos kansiolla ei ole READMEa, näytetään sen ylimmäinen dokumentti.
- READMEn otsikosta (H1) tulee kansion nimi INDEXissä.

README ei ole pakollinen. Voit lisätä sen myöhemmin valitsemalla kansion kohdevalikosta [Luo README] (näkyy vain kansioille, joilla ei ole READMEa).

## INDEXin näyttäminen ja piilottaminen

- Työkalurivin palkkisäätimien vasemmanpuoleisella kuvakkeella näytät tai piilotat INDEXin. Oikeanpuoleinen kuvake näyttää tai piilottaa Tällä sivulla ‑paneelin.
- Kapealla näytöllä INDEX on aluksi suljettuna. Kun painat [Takaisin]-painikkeen vasemmalla puolella näkyvää painiketta [Avaa INDEX] (kolme viivaa), INDEX avautuu leipätekstin päälle. Se sulkeutuu INDEXin sisällä olevasta [×]-painikkeesta, taustaa napsauttamalla, `Esc`-näppäimellä tai siirryttäessä toiseen dokumenttiin. Tämä tilapäinen avaus ei muuta leveän näytön asetusta.
- Jos dokumenttijuuressa näytetään vain yksi dokumentti, INDEX sulkeutuu automaattisesti ensimmäisellä kerralla. Voit avata sen uudelleen palkkikuvakkeesta. Toiminnon voi poistaa käytöstä kohdassa [Näyttöasetukset] valinnalla [Piilota, kun dokumentteja on vain yksi].

## Kohdevalikon käyttö

Avaa kohteen valikko viemällä hiiri INDEXin kohteen päälle ja painamalla näkyviin tulevaa [⋯]-painiketta tai napsauttamalla kohdetta hiiren oikealla painikkeella. Kohdat ovat seuraavassa järjestyksessä.

| Ryhmä | Kohdat |
|---|---|
| Usein käytetyt toiminnot | [Avaa kansio] / [Sulje kansio], [Avaa INDEX] (avaa kansion kansilehden), [Muokkaa], [Muuta otsikkoa], [Avaa VS Codessa], [Kopioi polku] |
| Luonti ja järjestely | [Luo README] (vain kansiot, joilla ei ole READMEa), [Uusi dokumentti], [Uusi kansio], [Monista], [Muuta tiedoston nimeä] / [Muuta kansion nimeä], [Siirrä ylemmäs], [Siirrä alemmas] |
| Poisto | [Siirrä roskakoriin] |

- Jos haluat luoda kohteen suoraan dokumenttijuureen, paina INDEXin otsikon oikeassa reunassa olevaa [⋯]-painiketta tai napsauta INDEXin tyhjää kohtaa hiiren oikealla painikkeella ja valitse [Uusi dokumentti] tai [Uusi kansio]. Samassa valikossa ovat [Muuta dokumentin nimeä] ja, jos dokumenttijuuressa ei ole READMEa, [Luo README]. Sama valikko avautuu myös napsauttamalla työkalurivillä näkyvää dokumentin nimeä hiiren oikealla painikkeella.
- Valikossa liikutaan näppäimillä `↑` `↓`, ja `Home` `End` siirtävät ensimmäiseen ja viimeiseen kohtaan. Kun suljet valikon `Esc`-näppäimellä, kohdistus palaa siihen kohtaan, jossa se oli ennen valikon avaamista.

> **Huomautus**
>
> Luonti-, järjestely- ja poistokohdat näkyvät vain, kun työtila on luotettu työtila VS Codessa. Ne eivät ole käytettävissä myöskään dokumentin muokkauksen aikana tai kun toista INDEX-toimintoa käsitellään.

## Ulkoasun muuttaminen

Kohdassa [Näyttöasetukset] voit muuttaa tiedostonimien näyttämistä, dokumenttien ja kansioiden kuvakkeita, kansioiden kohdemääriä, tasojen apuviivoja ja näyttötiheyttä. Lisätietoja on kohdassa [Näyttöasetusten muuttaminen](display-settings.md).

## Katso myös

- [Dokumenttien ja kansioiden luonti ja järjestely](../03-editing/organize.md)
- [Dokumenttien järjestyksen muuttaminen](../03-editing/reorder.md)
