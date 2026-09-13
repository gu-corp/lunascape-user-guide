# Käyttö tekoälyagenteista

Laajennus rekisteröi VS Codeen vain luku -tilassa toimivan Language Model Tool -työkalun `lunascape_getDocsSpecification`. Kun yhteensopivalta VS Coden agentilta kysytään Lunascape Docsin ominaisuuksista, asetuksista tai dokumenttikäytännöistä, se voi hakea tämän ohjeen sisällön (yleisen määrittelyn) tällä työkalulla.

## Käyttö

Kysy VS Coden keskustelussa merkinnällä `#lunascapeDocs` tai kysy suoraan Lunascape Docsin asetuksista tai dokumenttien rakenteesta.

```text
#lunascapeDocs Miten otan englanninkielisen käännöksen käyttöön tiedostossa lunascape-docs.json?
```

## Työkalun argumentit

| Argumentti | Sisältö |
|---|---|
| `topic` | Haettava luku: `all`, `usage` (Perustoiminnot), `structure` (Dokumenttijuuret ja tiedostokäytännöt), `editing` (Dokumentin muokkaus), `configuration` (Projektin asetukset), `security` (Tietoturva ja tallennusrajat) tai `ai` (Käyttö tekoälyagenteista) |
| `locale` | Ohjeen kieli (mukana toimitetun ohjeen kielitunnus, esimerkiksi `ja` tai `en`). Jos argumentti jätetään pois, käytetään VS Coden näyttökieltä ja muutoin japaninkielistä ohjetta |

> **Huomautus**
>
> - Työkalu ei lähetä dokumenttien sisältöä minnekään.
> - Työkalu ei palauta työtilojen nimiä eikä paikallisia polkuja.
> - Työkalu ei muuta tiedostoja.
> - Se toimii yhteensopivista VS Coden agenteista ilman `AGENTS.md`-tiedostoa. Sitä ei jaeta automaattisesti muille tekoälyasiakkaille, jotka eivät käytä laajennuksen työkalurajapintaa.

## Aiheeseen liittyvää

- [Ohjeen näyttäminen](../02-reading/help.md)
- [Tietoturva ja tallennusrajat](security.md)
