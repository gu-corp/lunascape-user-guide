# Perustoiminnot

Perustoiminnot dokumenttien avaamisesta haluamallesi sivulle siirtymiseen.

## Dokumenttien avaaminen

1. Avaa säilö VS Codessa.
2. Suorita komentopaletista (`⇧⌘P` / `Ctrl+Shift+P`) komento ”Lunascape Docs: Avaa määrittelykatselin”.
   Lähin dokumenttijuuri (oletuksena `docs`-kansio) haetaan ja sen aloitussivu avautuu.

> **Vihje**
>
> - Napsauta Markdown-tiedostoa hiiren kakkospainikkeella Resurssienhallinnassa ja valitse [Lunascape Docs: Avaa määrittelykatselimessa], niin voit aloittaa kyseisestä tiedostosta.
> - Kun avaat Markdown-tiedoston, joka ei kuulu mihinkään dokumenttijuureen, sen kansio näytetään väliaikaisena dokumenttijuurena.

## Sivujen välillä siirtyminen

| Toiminto | Miten |
|---|---|
| Avaaminen sisällysluettelosta | Paina dokumentin nimeä vasemmalla olevassa INDEX-paneelissa |
| Linkin seuraaminen | Paina tekstissä olevaa linkkiä. Se avautuu samaan näkymään |
| Historiassa liikkuminen | Työkalurivin [Takaisin] ja [Eteenpäin] tai `Alt`+`←` / `Alt`+`→` |
| Paluu aloitussivulle | Työkalurivin [Määrittelyn etusivu] |
| Siirtyminen ylemmälle tasolle | Työkalurivin [Ylätason INDEX] tai navigointipolun kohta |
| Sivun sisällä siirtyminen | Paina otsikkoa oikealla olevassa Tällä sivulla -luettelossa |

## Dokumentin etsiminen

Kun kirjoitat sanan INDEX-paneelin yläpuolella olevaan [Rajaa dokumentteja] -kenttään, näkyviin jäävät vain ne kohdat, joiden dokumentin nimi vastaa hakua. Kun tyhjennät kentän, kaikki tulee taas näkyviin.

## Sisällön päivittäminen

Kun tallennat Markdown-tiedoston VS Coden editorissa, näkymä päivittyy automaattisesti. Jos muutat tiedostoja ulkoisella työkalulla, paina työkalurivin [Lataa uudelleen] -painiketta.

> **Huomautus**
>
> - Tekstissä olevat ulkoiset linkit (esimerkiksi `https://`) avautuvat oletusselaimessa. Dokumenttijuuren ulkopuolella oleviin tiedostoihin johtavat linkit eivät avaudu.
> - Dokumentit käsitellään laitteessasi. Dokumentteja ei lähetetä mihinkään lukemista varten.

## Aiheeseen liittyvää

- [INDEX-paneelin käyttäminen](index-panel.md)
- [Dokumenttijuuren vaihtaminen](roots.md)
- [Dokumentin muokkaaminen](../03-editing/README.md)
