# AI-asetukset

Valitse AI ja malli, joille työ annetaan. Tämä näyttö käyttää omia pudotusvalikoitaan, ei VS Coden pikavalintaa.

1. Paina [Dokumenttityökalut] → [AI]-välilehti → [AI-asetukset…].
2. Valitse [Palveluntarjoaja].
   Tässä ympäristössä käyttökelvottomat näkyvät valintakelvottomina, ja syy on kerrottu.
3. Valitse [Malli]. Vaihtoehdot vaihtelevat palveluntarjoajan mukaan.
4. Sulje näyttö. Valinta tallennetaan käyttäjäkohtaisesti ja on käytössä myös ensi kerralla.

## Palveluntarjoajat

| Palveluntarjoaja | Muoto | Tunnistustapa |
|---|---|---|
| Claude Code | Istuntopohjainen | `claude`-komennon olemassaolo |
| Codex | Istuntopohjainen | `codex`-komennon olemassaolo |
| VS Coden kielimallit | API-pohjainen | VS Code Language Model API:in rekisteröidyt mallit |
| Anthropic API | API-pohjainen | Rekisteröity API-avain |
| OpenAI-yhteensopiva API | API-pohjainen | Rekisteröity API-avain ja päätepiste |

**Istuntopohjainen** palveluntarjoaja lukee ja kirjoittaa tiedostot itse ja suorittaa myös dokumenttitarkistuksen itse. Tulokset kirjoitetaan suoraan työpuuhun, ja ne tarkastetaan Gitin erotuksesta.

**API-pohjainen** palveluntarjoaja palauttaa yhden dokumentin verran Markdownia, ja laajennus näyttää erotuksen ennen tallennusta.

## API-avaimen rekisteröinti

Anthropic API ja OpenAI-yhteensopiva API ovat käytettävissä, kun API-avain on rekisteröity.

1. Valitse rekisteröintikohde kohdasta [Palveluntarjoaja]. API-avaimen syöttökenttä tulee näkyviin.
2. Syötä [API-avain]. OpenAI-yhteensopivassa syötä myös [Päätepiste] (esimerkiksi `https://api.openai.com/v1`).
3. Paina [Tallenna]. Näkyviin tulee ”Avain rekisteröity”.

> **Huomautus**
>
> - Avain tallennetaan VS Coden SecretStorageen, eikä sitä näytetä enää uudelleen. Sitä ei myöskään kirjoiteta tiedostoon `settings.json` eikä dokumentteihin. Voit poistaa sen painikkeella [Poista avain].
> - Malliluettelo haetaan kustakin palvelusta rekisteröidyllä avaimella. Siihen asti näytetään tunnettu luettelo.
> - API-pohjaisella voi suorittaa vain toiminnot ”Käännä tämä sivu” ja ”Oikolue tämä sivu”. Useiden dokumenttien läpikäynti ja dokumenttien luonti tehdään istuntopohjaisella.

> **Vihje**
>
> Jos yhtään palveluntarjoajaa ei löydy, asenna Claude Code tai Codex tai rekisteröi API-avain. Kun avaat [AI-asetukset…] uudelleen, se tunnistetaan.

## Aiheeseen liittyvää

- [Työn antaminen AI:lle](README.md)
- [VS Coden asetusluettelo](../08-reference/settings.md)
