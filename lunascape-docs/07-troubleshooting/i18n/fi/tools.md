# Tarkistus, luonti tai käännös ei onnistu

## Tarkistus

### Näkyviin tulee ”docs-lint ei ole käytettävissä”

- Laajennuksesta puuttuu docs-lintin suoritusympäristö, tai asetuksissa on ongelma. Asenna laajennus uudelleen.
- ”Luota tähän työtilaan VS Codessa, jotta paikallinen Pack ja asetukset voidaan ladata turvallisesti”: paikallisen Standard Packin käyttö edellyttää luotettua työtilaa.

### Tulos jää tilaan ”uudelleentarkistus tarvitaan”

Kun muutat dokumenttia tai asetusta, edellinen tulos mitätöityy. Paina [Tarkista dokumenttijuuri] uudelleen. Tallentamattomat muutokset eivät tule mukaan.

### Havainnon painaminen ei avaa mitään

Kohdat, joiden kohteena on ”koko dokumenttijuuri”, eivät liity tiettyyn dokumenttiin, joten niillä ei ole sijaintia. Tarkista havainnon sisällön mukainen dokumentti.

### Sääntöjä ei voi tallentaa

- Luotettu työtila vaaditaan.
- ”Lint-asetuksia muutettiin toisessa toiminnossa”: `docs-lint.config.json` on muuttunut ohjelman ulkopuolella. Lataa uusin tila ja yritä uudelleen.
- Symbolisia linkkejä tai dokumenttijuuren ulkopuolisia asetustiedostoja ei voi muokata.

## Mallista luominen

- ”Mallin esikatselu on vanhentunut” / ”Syötetyt tiedot ovat muuttuneet”: paina [Esikatselu] uudelleen ja luo dokumentti vasta sen jälkeen.
- ”Kohteessa on jo dokumentti”: olemassa olevia tiedostoja ei korvata. Valitse toinen tallennuskohde.
- Tallennuskohde tarvitsee dokumenttijuureen nähden suhteellisen polun ja tunnisteen `.md` tai `.mdx`. `i18n`-kansion alle ei voi luoda.
- ”Luota työtilaan, jotta voit luoda dokumentteja”: luota työtilaan VS Codessa.

<!-- ai-only:start -->
## Käännös

### Käännöspainikkeita ei voi painaa

- ”AI-käännöstä ei ole otettu käyttöön tässä dokumenttijuuressa”: aseta `lunascape-docs.json`-tiedostossa `translation.enabled` arvoon `true`.
- ”Projektin oletuskieltä ei ole määritetty”: tallenna oletuskieli ohjeen [Näyttöasetusten muuttaminen](../02-reading/display-settings.md) mukaan.
- ”Lisää kohdekieli tuettuihin kieliin”: lisää kohdekieli `locales`-luetteloon.
- ”Käännettävää alkuperäisdokumenttia ei löydy”: avoinna on käännetty sivu. Vaihda oletuskielen sivulle.
- Joukkokäännöstä ei voi käyttää, kun kansio on avattu tilapäisesti. Tee kansiosta dokumenttijuuri lisäämällä siihen `lunascape-docs.json`.

### Käännösehdotus hylätään tai se on tehtävä uudelleen

- ”Alkuperäisdokumentti on muuttunut. Tee käännösehdotus uudelleen”: alkuperäisdokumentti tai käännöskohde muuttui ehdotuksen tekemisen jälkeen. Käännä uudelleen.
- Jos kielimallin vastauksesta puuttuu suojattavia tunnisteita tai koodia, vastausta ei hyväksytä. Vastauksen sisällön voi tarkistaa tulostepaneelin kohdasta ”Lunascape Docs -käännös”.
- ”Joukkokäännös käsittelee enintään 1000 dokumenttia kerralla”: jaa alue kansioittain tai valitsemalla dokumentit erikseen.
<!-- ai-only:end -->

## Liittyvät aiheet

- [Dokumenttien tarkistaminen](../04-document-tools/check.md)
- [Dokumentin luominen mallista](../04-document-tools/templates.md)
- [Työn antaminen tekoälylle](../05-ai/README.md)
