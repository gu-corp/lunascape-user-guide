# Näyttöasetusten muuttaminen

Työkalurivin [Näyttöasetukset] (ratas) -painikkeesta jokainen käyttäjä voi muuttaa INDEX-paneelin ulkoasua ja muokkauspainikkeen näkymistä.

1. Paina työkalurivin [Näyttöasetukset].
2. Vaihda haluamiesi kohtien tila. Muutokset tulevat voimaan heti.
3. Sulje paneeli painamalla [Näyttöasetukset] uudelleen tai napsauttamalla paneelin ulkopuolelle.

## Määritettävät kohdat

| Osa | Kohta | Toiminto |
|---|---|---|
| Dokumentin kieli | (nykyinen tila) | Näyttää projektin oletuskielen ja käytössä olevan näyttökielen. [Määritä projektin kielet…] avaa projektin kieliasetukset |
| Sisältö | [Tiedostonimet] | Näyttää dokumentin nimen sijasta tiedostonimen |
| | [Dokumenttikuvakkeet] | Näyttää kuvakkeen dokumenttien kohdalla |
| | [Kansiokuvakkeet] | Näyttää kuvakkeen kansioiden kohdalla |
| | [Kohteiden määrät] | Näyttää kansion sisältämien dokumenttien määrän |
| | [Sisennysviivat] | Näyttää hierarkiaa osoittavat apuviivat |
| | [Piilota, kun dokumentteja on vain yksi] | Sulkee INDEX-paneelin automaattisesti ensimmäisellä kerralla, kun dokumenttijuuressa on vain yksi dokumentti |
| | [Tiivistä dokumentin tiedot] | Tiivistää dokumentin alussa olevan hallintataulukon ”Dokumentin tiedot” -riviksi. Kun asetus on pois päältä, taulukko näkyy sellaisenaan |
| | [Näyttötiheys] | Valitsee INDEX-paneelin riviväliksi [Normaali] tai [Tiivis] |
| | [Muokkauspainike] | Näyttää [Muokkaa]-painikkeen tekstin oikeassa alakulmassa |
| Toiminnot | [Palauta projektin oletukset] | Poistaa kaikki omat muutoksesi ja palauttaa projektin asetukset |
| | [Avaa laajennuksen asetukset] | Avaa Lunascape Docsin asetukset VS Coden asetusnäkymässä |

> **Vinkki**
>
> - Näyttöasetukset tallennetaan käyttäjä- ja dokumenttijuurikohtaisesti, eikä niitä kirjoiteta Gitin hallitsemiin tiedostoihin.
> - Asetukset ovat voimassa järjestyksessä ”käyttäjän näyttöasetukset → VS Coden asetukset → `lunascape-docs.json` → tuotteen oletukset”. Tiimin yhteiset oletusarvot määritetään tiedoston `lunascape-docs.json` kohdissa `tree` ja `editor`.

## Väriteeman vaihtaminen

Työkalurivin teemanvaihto (aurinko/kuu) vaihtaa valkoisen taustan ja VS Coden väriteeman välillä. Avattaessa käytettävän teeman määrittää asetus `lunascapeDocEditor.appearance` (`light` tai `auto`).

## Aiheeseen liittyvää

- [INDEX-paneelin käyttö](index-panel.md)
- [Projektin asetukset](../04-document-tools/project-configuration.md)
- [VS Coden asetukset](../08-reference/settings.md)
