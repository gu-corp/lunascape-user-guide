# GitHub-säilön avaaminen

Verkkoversiossa ja Lunascapessa voit avata GitHub-säilön ja lukea sitä sellaisenaan kloonaamatta sitä. Julkiset säilöt eivät vaadi kirjautumista.

## Avaaminen näkymästä

1. Paina työkalurivin painiketta [Avaa dokumentteja] (kansiokuvake). ”Avaa dokumentteja” -näkymä avautuu.
2. Valitse vasemmasta sarakkeesta paikka, josta avaat.

   | Paikka | Mitä luettelossa on |
   |---|---|
   | Kaikki | Kaikki alla olevat. Viimeksi avatut ovat ensimmäisinä |
   | Viimeksi avatut | Säilöt ja kansiot, jotka olet avannut aiemmin |
   | Suositellut | Sivuston esittelemät käyttöoppaat |
   | GitHub-säilöt | Kun olet kirjautunut sisään GitHubilla, säilöt, joita voit lukea |
   | Tämä tietokone | Tämän laitteen kansiot. Lunascapessa myös kloonatut säilöt näkyvät tässä |

3. Paina avattavan rivin painiketta [Avaa]. Voit rajata rivejä kirjoittamalla yläreunan kenttään [Suodata dokumentin tai säilön nimellä].

Luettelosta puuttuvan säilön voit avata vasemman sarakkeen kohdasta [Kirjoita owner/repo ja avaa].

> **Vihje**
>
> - Luettelossa näkyvät ne GitHub-säilöt, joihin GitHub-sovellus ”Lunascape Docs” on asennettu ja joihin sinulla on lukuoikeus. Jos säilö puuttuu, pyydä sen omistajaa lisäämään sovellus.

## Dokumentin sijainnin tarkistaminen

Työkalurivin vasemmassa reunassa oleva pieni kuvake (sijaintisiru) näyttää, missä lukemasi dokumentti on.

| Kuvake | Sijainti |
|---|---|
| GitHubin logo | Luet dokumenttia GitHubista. Sitä ei ole tallennettu tähän laitteeseen |
| Tietokone | Lunascapen hallitsema kansio tässä laitteessa. Myös Git-haara ja muutettujen tiedostojen määrä näytetään |
| Kansio | Kansio tässä laitteessa |

Kun painat kuvaketta, näet sijainnin, sen tilan ja toiminnot, jotka ovat sieltä käytettävissä (esimerkiksi [Näytä GitHubissa] ja [Kopioi linkki]).

## Säilön kloonaaminen Lunascapessa

Lunascapessa voit kloonata GitHub-säilön tähän laitteeseen ja muokata sitä ja tehdä committeja Gitin avulla.

- Paina ”Avaa dokumentteja” -näkymässä säilön rivin painiketta [Monista].
- Kun luet GitHubista avattua säilöä, paina sijaintisirua ja sitten [Monista tälle tietokoneelle]. Kun kloonaus on valmis, sama dokumentti avautuu tämän laitteen kopiosta.

Kloonattu säilö merkitään luettelossa tekstillä ”Tällä tietokoneella”, ja sen rivillä [Avaa tällä tietokoneella] on ensimmäisenä.

## Avaaminen URL-osoitteella

Osoitteessa ovat peräkkäin säilö ja dokumentin sijainti. Polku on sijainti säilön sisällä, joten järjestys on sama kuin GitHubin URL-osoitteessa.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Määritys | Muoto |
|---|---|
| Vain säilö (oletushaara) | `/github/owner/repo` |
| Säilön sisällä oleva dokumentti | `/github/owner/repo/docs/01-product/vision.md` |
| Haara tai tagi | Lisää loppuun `?ref=v1.2.0` |

Osoite muuttuu, kun siirryt sivulta toiselle. Painamalla työkalurivin painiketta [Jaa tämä dokumentti] voit antaa linkin lukemaasi sivuun. Voit käyttää myös selaimen painikkeita [Takaisin] ja [Eteenpäin].

Vanha `?source=`-muoto avautuu edelleen. Avaamisen jälkeen osoite muutetaan uuteen muotoon.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Huomio**
>
> - Kirjautumattomana GitHub API:n käyttöraja on 60 pyyntöä tunnissa. Jos säilössä on paljon dokumentteja tai luet sitä toistuvasti, kirjaudu sisään painamalla [Kirjaudu sisään GitHubilla].
> - `/`-merkin sisältävät haaranimet (kuten `feature/xxx`) voi määrittää yllä olevan osoitemuodon `?ref=`-parametrilla. `?source=`-muodossa niitä ei voi kirjoittaa.
> - Dokumentit ladataan lukijan omilla GitHub-oikeuksilla. Ne eivät näy henkilöille, joilla ei ole lukuoikeutta.

## Dokumenttien avaaminen paikallisesta kansiosta

Paina työkalurivin painiketta [Avaa dokumentteja], valitse vasemmasta sarakkeesta [Avaa dokumentteja paikallisesta kansiosta] ja valitse kansio laitteestasi. Tiedostot käsitellään selaimessa, eikä niitä lähetetä minnekään. Toiminto on käytettävissä selaimissa, jotka tukevat kansion valintaa (esimerkiksi Chrome ja Edge).

## Aiheeseen liittyvää

- [Yksityisen säilön lukeminen](private-repository.md)
- [Verkkoversio ei avaudu tai sisäänkirjautuminen ei onnistu](../07-troubleshooting/web.md)
