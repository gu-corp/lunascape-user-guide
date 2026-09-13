# GitHub-säilön avaaminen

Web-versiossa avaat dokumentit nimeämällä GitHub-säilön. Julkisiin säilöihin ei tarvita kirjautumista.

## Avaaminen näytöltä

1. Avaa <https://docs.lunascape.org/>.
2. Paina työkalurivin [Avaa dokumentteja] (kansion kuvake).
3. Kirjoita säilö kohtaan [Anna säilö suoraan] ja paina [Avaa].
   Kun olet kirjautunut GitHubiin, voit myös valita säilön luettelosta kohdassa [Valitse luettavissa olevista säilöistä].

> **Vinkki**
>
> - Sen vieressä oleva GitHub-kuvake avaa parhaillaan luettavan dokumentin osoitteessa github.com. Se ei ole dokumenttien avaamistoiminto.

## Avaaminen URL-osoitteella

Osoite luettelee säilön ja dokumentin sijainnin sellaisenaan. Polku on sijainti säilön sisällä, joten se on samassa järjestyksessä kuin GitHubin URL-osoite.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Määritys | Kirjoitustapa |
|---|---|
| Vain säilö (oletushaara) | `/github/owner/repo` |
| Dokumentti säilön sisällä | `/github/owner/repo/docs/01-product/vision.md` |
| Haara tai tunniste | lisää loppuun `?ref=v1.2.0` |

Osoite muuttuu, kun siirryt sivulta toiselle. Kun painat työkalurivin [Jaa tämä dokumentti], voit antaa linkin parhaillaan luettavaan sivuun. Myös selaimen [Takaisin] ja [Eteenpäin] toimivat.

Myös aiempi `?source=`-muoto avautuu edelleen entiseen tapaan. Avaamisen jälkeen se kirjoitetaan uuteen muotoon.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Huomautus**
>
> - Kirjautumattomana GitHub API:n käyttörajoitus (60 kertaa tunnissa) on voimassa. Jos säilössä on paljon dokumentteja tai luet niitä toistuvasti, käytä [Kirjaudu sisään GitHubilla].
> - Haarojen nimet, joissa on `/` (kuten `feature/xxx`), voi määrittää yllä olevan osoitemuodon `?ref=`-osalla. `?source=`-muodossa niitä ei voi kirjoittaa.
> - Dokumentit ladataan lukijan omilla GitHub-oikeuksilla. Ne eivät näy henkilöille, joilla ei ole lukuoikeutta.

## Paikallisen kansion dokumenttien avaaminen

Paina työkalurivin [Avaa dokumentteja] ja valitse luettelon alta [Avaa dokumentteja paikallisesta kansiosta], minkä jälkeen valitse kansio laitteeltasi. Tiedostot käsitellään selaimen sisällä eikä niitä lähetetä ulkopuolelle. Toiminto on käytettävissä selaimissa, jotka tukevat kansion valintaa (Chrome, Edge ja muut).

## Aiheeseen liittyvää

- [Yksityisen säilön lukeminen](private-repository.md)
- [Web-versio ei avaudu tai kirjautuminen ei onnistu](../07-troubleshooting/web.md)
