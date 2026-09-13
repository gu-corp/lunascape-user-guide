# Muokkaaminen, tallentaminen tai järjestäminen ei onnistu

## [Muokkaa]-painiketta ei ole

- [Näyttöasetukset]-kohdan [Muokkauspainike] on pois käytöstä. Ota se käyttöön tai käytä dokumentin oikeassa yläkulmassa olevaa valintaa [⋯] → [Muokkaa] tai INDEX-kohdan valikon vaihtoehtoa [Muokkaa].
- Sama koskee tilannetta, jossa `lunascape-docs.json`-tiedoston `editor.showEditButton` on `false`.
- Muokkaaminen ei ole mahdollista, kun ohje on näkyvissä. Sulje ohje.

## Visuaaliseen näkymään ei voi vaihtaa

”Tässä dokumentissa on MDX-syntaksia, joten tavalliseen muokkausnäkymään ei voi vaihtaa”: dokumentit, joissa on MDX:n omaa syntaksia (komponentteja, `import` ja vastaavia), muokataan vain Markdown-näkymässä, jotta syntaksi säilyy.

## Matematiikkaa tai kaaviota ei voi muokata suoraan

Visuaalinen näkymä esittää piirretyn tuloksen. Paina muokkausnäkymässä [Markdown] ja muokkaa lähdettä.

## Järjestäminen tai vetäminen ei onnistu

- Järjestäminen ei onnistu suodatuksen aikana, dokumenttia muokattaessa eikä toisen INDEX-toiminnon ollessa kesken.
- Kun työtilaa ei ole merkitty luotetuksi, luonti-, järjestely- ja poistotoiminnot eivät ole käytettävissä. Merkitse työtila luotetuksi VS Codessa.
- ”INDEX on päivittynyt. Vedä uudelleen”: toinen muutos tuli juuri voimaan. Tee toiminto uudelleen.
- Aloitussivua (juuren `README.md`) ei voi siirtää.

## Näkyviin tulee ”Tallentamattomia muutoksia”

Kohdetiedostoa muokataan VS Coden editorissa. Tallenna muutokset tai hylkää ne ensin ja yritä sitten uudelleen.

## Nimeä ei voi muuttaa

Seuraavia nimiä ei voi käyttää.

- Nimet, jotka alkavat merkillä `.`, nimi `i18n` sekä Windowsin varatut nimet (kuten `CON`)
- Nimet, jotka päättyvät pisteeseen tai välilyöntiin, sekä nimet, joissa on ohjausmerkkejä tai tiedostonimessä kiellettyjä merkkejä
- Nimet, jotka ovat jo samassa kansiossa (mukaan lukien nimet, jotka eroavat vain kirjainkoon osalta)
- Dokumenttien nimet ilman Markdown-tiedostopäätettä

## Tallennus ei näy Gitissä tai muutoksia ei ole vahvistettu

Lunascape Docs vain kirjoittaa tiedostoon eikä lisää muutoksia Gitin valmistelualueelle tai vahvista niitä. Tarkista tilanne VS Coden lähdehallintanäkymästä ja vahvista muutokset tarvittaessa.

## Aiheeseen liittyvää

- [Dokumentin muokkaaminen](../03-editing/README.md)
- [Dokumenttien ja kansioiden luominen ja järjestely](../03-editing/organize.md)
- [Dokumenttien järjestyksen muuttaminen](../03-editing/reorder.md)
