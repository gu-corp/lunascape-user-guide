# Tarkistussääntöjen muuttaminen

Voit muuttaa kunkin tarkistuskohdan ilmoitustasoa (virhe, varoitus, tieto) tai poistaa kohdan käytöstä. Muutokset tallennetaan dokumenttijuuren tiedostoon `docs-lint.config.json`, ja ne jaetaan tiimin kesken.

## Ilmoitustason muuttaminen

1. Paina työkalurivin [Dokumenttityökalut] ja avaa [Tarkistus]-välilehti.
2. Paina [Tarkastele ja muuta sääntöjä].
   Tarkistuskohtien luettelo avautuu samaan korttiin. Kunkin kohdan kohdalla näkyvät sen tarkoitus ja nykyisen asetuksen lähde (Project, Profile, Pack tai Default).
3. Valitse muutettavan kohdan ilmoitustaso.
4. Paina [Tallenna ja tarkista uudelleen].
   Asetus tallennetaan ja koko dokumenttijuuri tarkistetaan uudelleen uusilla asetuksilla.

| Vaihtoehto | Merkitys |
|---|---|
| [Vakioasetus (…)] | Poistaa ohituksen ja palauttaa vakioasetuksen, joka määräytyy järjestyksessä profiilin, Standard Packin ja oletusarvon mukaan |
| [Ei käytössä] | Tätä kohtaa ei tarkisteta |
| [Tieto] / [Varoitus] / [Virhe] | Raportoidaan tällä ilmoitustasolla |

> **Huomautus**
>
> - Tallentaminen edellyttää luotettua työtilaa.
> - Tallennetaan vain kunkin kohdan ilmoitustaso. Kohtakohtaiset asetukset säilyvät ennallaan. Standard Packia ja profiilia ei muuteta tällä näytöllä.
> - Jos tiedostoa `docs-lint.config.json` on muutettu ulkopuolelta juuri ennen tallennusta, tallennus keskeytetään. Lataa uusin tila ja yritä uudelleen.
> - Jos tiedostoa `docs-lint.config.json` ei ole, se luodaan tallennettaessa.

## Asetustiedostojen muokkaaminen suoraan

- Kun painat [Avaa tarkemmat asetukset], tiedosto `docs-lint.config.json` avautuu VS Codessa.
- Avaa [Sääntöjen lähde ja dokumenttiasetukset] ja paina [Muokkaa dokumenttiasetuksia], niin tiedosto `lunascape-docs.json` avautuu VS Codessa. Standard Pack ja profiili valitaan täällä.

Molemmissa tiedostoissa ovat käytössä laajennuksen mukana toimitettujen JSON Schema -määritysten täydennykset ja kuvaukset.

## Standard Pack ja profiilit

Standard Pack on dokumentaatiostandardi, joka kokoaa yhteen tarvittavat dokumenttityypit, lukurakenteen, termistön ja mallit. Se valitaan tiedoston `lunascape-docs.json` kohdassa `documentStandards`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Mukana toimitettavassa paketissa `builtin:gu-corp-software` ovat profiilit `base`, `web-application`, `api-service`, `regulated-financial-product` ja `smart-contract`.

## Aiheeseen liittyvää

- [Dokumenttien tarkistaminen](check.md)
- [Projektiasetukset](project-configuration.md)
