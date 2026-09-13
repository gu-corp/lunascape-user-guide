# Käytettävissä olevat työt

Valitse [AI]-välilehden kohdasta [Työ]. Kukin työ muuttaa annettavaa ohjetta ja sen jälkeistä tarkistusta.

| Työ | Sisältö | Vaatimukset | API-tyyppi |
|---|---|---|---|
| Käännä tämä sivu | Kääntää näkyvissä olevan dokumentin valitulle kielelle | Kohdedokumentti avattuna, kohdekieli | ✓ |
| Käännä kaikki kääntämättömät | Kääntää valitun kielen kääntämättömät ja päivitettävät dokumentit järjestyksessä | Kohdekieli | Vain istuntotyyppinen |
| Oikolue tämä sivu | Tarkistaa ja korjaa termistön, tyylin ja dokumenttistandardin vaatiman lukurakenteen | Kohdedokumentti avattuna | ✓ |
| Luo uusi dokumentti | Luo uuden dokumentin dokumenttistandardin ja mallien mukaisesti | Aihe (valinnainen) | Vain istuntotyyppinen |

## Mitä ohje sisältää

| Nro | Sisältö |
|---|---|
| 1 | Dokumenttijuuren sijainti. Ohjeistaa olemaan muuttamatta mitään sen ulkopuolella |
| 2 | Oletuskieli (alkuperäisdokumentti) ja käännösten sijainti (`i18n/<kieli>/` samassa kansiossa kuin dokumentti) |
| 3 | Että `navigation.order` kuuluu vain alkuperäisdokumentille ja että käännös saa korvata vain kohdan `navigation.title` |
| 4 | Että vaatimustunnuksia, linkkejä, koodia, Mermaidia, TeX:ää tai front matterin rakennetta ei saa muuttaa |
| 5 | Dokumenttistandardi ja sanasto (`docs-lint.config.json`-tiedoston `terminology`) |
| 6 | Että lopuksi on suoritettava dokumenttitarkistus, raportoitava muutetut tiedostot eikä tehtävä Git-toimintoja |

> **Vihje**
>
> Työn ”Käännä kaikki kääntämättömät” kohteet muodostetaan luettelosta, enintään 200 dokumenttia kerrallaan. Jos dokumentteja on enemmän, suorita työ uudelleen.

## Aiheeseen liittyvää

- [Työn antaminen tekoälylle](README.md)
- [Luettelo ja tietueet](ledger.md)
