# Yksityisen säilön lukeminen

Kun kirjaudut sisään GitHubilla, voit lukea yksityisten säilöjen dokumentteja, kuitenkin vain niistä säilöistä, joihin sinulla on lukuoikeus. Lunascape Docsilla ei koskaan ole omia tilejä tai käyttöoikeuksia.

## Kirjaudu sisään ja avaa

1. Avaa <https://docs.lunascape.org/>.
   Jos määrität yksityisen dokumentin tai et ole vielä kirjautunut sisään, näkyviin tulee kirjautumisnäkymä.
2. Paina [Kirjaudu sisään GitHubilla].
   GitHubin tunnistautumisnäkymä avautuu ponnahdusikkunaan.
3. Kun kirjautuminen on valmis, paina työkalurivin [Avaa dokumentteja] ja valitse avattava säilö kohdasta [Valitse luettavissa olevista säilöistä].

> **Vihje**
>
> - Sisäänkirjautuneen tilin nimi näkyy työkalurivillä. Sieltä voit myös valita [Kirjaudu ulos] tai [Kirjaudu sisään toisella tilillä].
> - Luettelossa näkyvät niiden tilien (organisaatioiden tai henkilöiden) säilöt, joihin GitHub App ”Lunascape Docs” on asennettu, kuitenkin vain ne, joihin sinulla on lukuoikeus.

## Säilön omistajan tekemät asetukset

Jos haluttu säilö ei näy luettelossa, säilön omistajan tai organisaation ylläpitäjän on asennettava GitHub App ”Lunascape Docs”.

- Pyydettävät käyttöoikeudet ovat Contents (luku ja kirjoitus) sekä Pull requests (luku ja kirjoitus). Luku on tarkoitettu lukemiseen ja kirjoitus verkosta lähetettävään julkaisupyyntöön (Pull Request). Lunascape Docs ei tallenna dokumenttien sisältöä.
- Asennus tehdään tilikohtaisesti (organisaatio tai henkilö). Määrität, koskeeko se kohdetta ”All repositories” (mukaan lukien automaattisesti myöhemmin luotavat säilöt) vai vain valittuja säilöjä.

| Tilanne | Vaiheet |
|---|---|
| Käyttöönotto uudessa organisaatiossa tai henkilötilillä | Tee se [asennussivulta](https://github.com/apps/lunascape-docs/installations/new) |
| Säilöjen lisääminen organisaatiossa, jossa se on jo käytössä | Määritä organisaation Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Vaikka sovellus asennettaisiin koko organisaatiolle, kukin jäsen näkee vain ne säilöt, joihin hänellä on lukuoikeus. Julkaisupyynnön voi lähettää vain niihin säilöihin, joihin hänellä on kirjoitusoikeus.

> **Vihje**
> - Uutta asennusta tehtäessä pyydettävät käyttöoikeudet näkyvät luettelona asennusnäkymässä, ja niiden hyväksyminen tapahtuu, kun painat ”Install”. Muita toimia ei tarvita.
> - Organisaatiolle, joka oli asentanut sovelluksen ennen käyttöoikeuden lisäämistä, lähetetään ylläpitäjille vahvistusviesti, ja hyväksymispainike näkyy kohdan organisaation Settings → GitHub Apps → Lunascape Docs → Configure yläosassa. Ennen hyväksyntää kyseisessä organisaatiossa voi vain lukea, ja julkaisupyyntöä lähetettäessä näkyy ilmoitus ”Kirjoitusoikeuden myöntäminen vaaditaan”.
> - Voimassa olevat käyttöoikeudet näet samasta Configure-näkymästä. Henkilötilillä se on Settings → Applications → Installed GitHub Apps.
> - Jos poistit kohdesäilön vahingossa tai poistit sovelluksen, voit palauttaa tilanteen asentamalla sen uudelleen [asennussivulta](https://github.com/apps/lunascape-docs/installations/new). Hylätyn julkaisupyynnön viestissä on linkki korjausnäkymään.
> - Jos et halua ottaa säilössä vastaan julkaisupyyntöjä, kirjoita tiedostoon `lunascape-docs.json` merkintä `"publish": { "enabled": false }`. Lukeminen toimii silti entiseen tapaan.

## Katso myös

- [GitHub-säilön avaaminen](open-repository.md)
- [Verkkoversiota ei voi avata tai siihen ei voi kirjautua](../07-troubleshooting/web.md)
