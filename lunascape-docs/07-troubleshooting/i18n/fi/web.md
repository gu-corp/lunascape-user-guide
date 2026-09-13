# Verkkoversio ei avaudu tai kirjautuminen ei onnistu

## Kirjautumisen jälkeen säilö ei näy luettelossa

Kyseiselle tilille ei ole asennettu GitHub App ‑sovellusta ”Lunascape Docs”, tai kohdesäilö ei sisälly asennukseen. Pyydä säilön omistajaa tai organisaation ylläpitäjää asentamaan se kohdan [Yksityisen säilön lukeminen](../06-web/private-repository.md) ohjeiden mukaan.

## Kirjautumisnäytöstä ei pääse eteenpäin

- Sinulla ei ole lukuoikeutta kohdesäilöön. Pyydä säilön omistajaa myöntämään oikeus.
- ”Tälle sivustolle ei ole määritetty GitHub-kirjautumista”: itse sijoittamaasi katseluohjelmaan ei ole määritetty kirjautumispalvelua. Ylläpitäjän on määritettävä kirjautumispalvelu.

## Kirjautumisen ponnahdusikkuna ei avaudu

Selain estää ponnahdusikkunat. Salli ponnahdusikkunat tälle sivustolle ja yritä uudelleen.

## Näkyviin tulee ilmoitus ”Kirjautuminen on vanhentunut”

Kirjautuminen on vanhentunut. Paina uudelleen [Kirjaudu sisään GitHubilla].

## Julkisen säilön avaaminen johtaa virheeseen 404

- Tarkista merkintätapa `owner/repo@ref/dir`.
- Haaran nimeä, jossa on `/`, ei voi antaa.

## Lataaminen lakkaa toimimasta hetken kuluttua

Kun et ole kirjautuneena sisään, GitHubin API:ssa on käyttörajoitus (60 kertaa tunnissa). Jos näkyviin tulee ilmoitus ”Kutsujen enimmäismäärä on saavutettu”, odota hetki tai kirjaudu sisään painamalla [Kirjaudu sisään GitHubilla].

## Näkyviin tulee ilmoitus ”Tältä sivustolta ei voi näyttää tätä säilöä”

Jotta säilön voi avata itse sijoittamastasi katseluohjelmasta, sivuston URL-osoite on lisättävä säilön `lunascape-docs.json`-tiedoston kohtaan `viewer.origins`.

## `index.html`-tiedoston avaaminen ei näytä mitään

Suoraan `file://`-osoitteesta avattuna se ei toimi. Avaa se HTTP-palvelimen kautta tai käytä VS Code -versiota.

## Viedyllä sivustolla näkyy ilmoitus ”lunascape-docs-manifest.json ei löydy”

Sijoita `npm run export:web` ‑komennon tuottamat tiedostot kokonaisuudessaan (myös manifesti) sellaisinaan.

## Luonnosta ei voi tallentaa

- ”IndexedDB ei avaudu” tai ”Käytössä toisessa välilehdessä”: syynä on selaimen yksityinen tila tai toinen välilehti, jossa sama sivusto on auki. Avaa sivusto tavallisessa ikkunassa ja sulje muut välilehdet.
- Luonnokset tallennetaan laite- ja selainkohtaisesti. Ne eivät siirry toiselle laitteelle.

## Aiheeseen liittyvää

- [GitHub-säilön avaaminen](../06-web/open-repository.md)
- [Luonnoksen tallentaminen](../06-web/drafts.md)
