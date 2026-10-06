# GitHub-säilön avaaminen

Verkkoversiossa voit avata GitHub-säilön ja lukea sitä sellaisenaan kloonaamatta sitä. Julkisiin säilöihin ei tarvitse kirjautua sisään.

## Avaaminen näytöltä

1. Paina työkalurivin [Avaa dokumentteja] -painiketta (kansiokuvake). ”Avaa dokumentteja” -näkymä avautuu.
2. Valitse vasemmasta sarakkeesta paikka, josta avaat.

   | Paikka | Mitä näkyy |
   |---|---|
   | Kaikki | Kaikki alla olevat. Viimeksi avatut näkyvät ensimmäisinä |
   | Viimeksi avatut | Aiemmin avaamasi säilöt ja kansiot |
   | Suositellut | Sivuston esittelemät käyttöoppaat |
   | GitHub-säilöt | Kun olet kirjautunut sisään GitHubiin: säilöt, joita voit lukea |
   | Tämä tietokone | Tämän laitteen kansiot |

3. Paina avattavan rivin [Avaa] -painiketta. Voit rajata rivejä kirjoittamalla yläreunan kenttään [Suodata dokumentin tai säilön nimellä].

Jos säilö ei ole luettelossa, määritä se vasemman sarakkeen kohdasta [Avaa owner/repo].

> **Vihje**
>
> - Luettelossa näkyvät ne GitHub-säilöt, joihin GitHub App ”Lunascape Docs” on asennettu ja joihin sinulla on lukuoikeus. Jos säilöä ei löydy, pyydä säilön omistajaa lisäämään sovellus.

## Dokumentin sijainnin tarkistaminen

Työkalurivin vasemmassa reunassa oleva pieni kuvake (sijaintimerkki) näyttää, missä parhaillaan lukemasi dokumentti on.

| Kuvake | Sijainti |
|---|---|
| GitHub-merkki | Luet dokumenttia GitHubista. Sitä ei ole tallennettu tälle laitteelle |
| Kansio | Tämän laitteen kansio |

Kun painat kuvaketta, näkyviin tulevat sijainti, tila ja toiminnot, jotka sieltä voi tehdä (esimerkiksi [Näytä GitHubissa] ja [Kopioi linkki]).

## Avaaminen URL-osoitteella

Osoitteessa säilö ja dokumentin sijainti ovat sellaisinaan peräkkäin. Polku on sijainti säilön sisällä, joten järjestys on sama kuin GitHubin URL-osoitteessa.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Määritys | Kirjoitustapa |
|---|---|
| Vain säilö (oletushaara) | `/github/owner/repo` |
| Dokumentti säilön sisällä | `/github/owner/repo/docs/01-product/vision.md` |
| Haaran tai tagin määrittäminen | Lisää loppuun `?ref=v1.2.0` |

Kun siirryt sivulta toiselle, myös osoite muuttuu. Painamalla työkalurivin [Jaa tämä dokumentti] -painiketta voit antaa linkin parhaillaan lukemaasi sivuun. Voit käyttää myös selaimen painikkeita [Takaisin] ja [Eteenpäin].

Myös aiempi `?source=`-muoto avautuu edelleen. Avaamisen jälkeen osoite muutetaan uuteen muotoon.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Huomio**
>
> - Kun et ole kirjautunut sisään, GitHub API:n käyttörajoitus (60 pyyntöä tunnissa) on voimassa. Jos säilössä on paljon dokumentteja tai luet niitä toistuvasti, kirjaudu sisään valitsemalla [Kirjaudu sisään GitHubilla].
> - Haaranimet, joissa on `/` (esimerkiksi `feature/xxx`), voi määrittää yllä olevan osoitemuodon `?ref=`-parametrilla. `?source=`-muodossa niitä ei voi kirjoittaa.
> - Dokumentit ladataan lukijan GitHub-oikeuksilla. Ne eivät näy henkilöille, joilla ei ole lukuoikeutta.

## Paikallisen kansion dokumenttien avaaminen

Paina työkalurivin [Avaa dokumentteja] -painiketta ja valitse laitteen kansio vasemman sarakkeen kohdasta [Avaa dokumentteja paikallisesta kansiosta]. Tiedostot käsitellään selaimessa, eikä niitä lähetetä minnekään. Toiminto on käytettävissä selaimissa, jotka tukevat kansion valintaa (esimerkiksi Chrome ja Edge).

## Liittyvät aiheet

- [Yksityisen säilön lukeminen](private-repository.md)
- [Verkkoversio ei avaudu tai kirjautuminen ei onnistu](../07-troubleshooting/web.md)
