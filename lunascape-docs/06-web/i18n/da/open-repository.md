# Åbn et GitHub-lager

I webversionen kan du åbne et GitHub-lager og læse det direkte uden at klone det. Offentlige lagre kræver ikke, at du logger ind.

## Åbn fra skærmen

1. Tryk på [Åbn dokumenter] (mappeikonet) på værktøjslinjen. Skærmen »Åbn dokumenter« åbnes.
2. Vælg i listen til venstre, hvor du vil åbne fra.

   | Sted | Det, der vises |
   |---|---|
   | Alle | Alt nedenfor. Det, du senest har åbnet, står øverst |
   | Senest åbnet | De lagre og mapper, du har åbnet |
   | Anbefalet | De vejledninger, som webstedet anbefaler |
   | GitHub-lagre | De lagre, du kan læse, når du er logget ind med GitHub |
   | Denne computer | Mapper på denne enhed |

3. Tryk på [Åbn] i den række, du vil åbne. Skriv i [Filtrér efter dokument- eller lagernavn] øverst for at indsnævre rækkerne.

Et lager, der ikke står på listen, angiver du med [Indtast owner/repo for at åbne] i listen til venstre.

> **Tip**
>
> - De GitHub-lagre, der står på listen, er dem, hvor GitHub-appen »Lunascape Docs« er installeret, og som du har læseadgang til. Hvis et lager mangler, så bed lagerets ejer om at tilføje appen.

## Se, hvor dokumentet ligger

Det lille ikon i venstre side af værktøjslinjen (placeringschippen) viser, hvor det dokument, du læser, ligger.

| Ikon | Placering |
|---|---|
| GitHub-logoet | Læses fra GitHub. Det er ikke gemt på denne enhed |
| Mappe | En mappe på denne enhed |

Tryk på ikonet for at se placeringen, status og det, du kan gøre derfra (fx [Vis på GitHub] og [Kopiér link]).

## Åbn med en URL

Adressen består af lageret og dokumentets placering i rækkefølge. Stien er placeringen i lageret, så den følger samme rækkefølge som GitHub-URL'en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Hvad der angives | Skrivemåde |
|---|---|
| Kun lageret (standardgren) | `/github/owner/repo` |
| Et dokument i lageret | `/github/owner/repo/docs/01-product/vision.md` |
| En bestemt gren eller et tag | Tilføj `?ref=v1.2.0` til sidst |

Adressen skifter, når du går til en anden side. Tryk på [Del dette dokument] på værktøjslinjen for at give andre et link til den side, du læser. Browserens [Tilbage] og [Frem] virker også.

Den tidligere `?source=`-form kan stadig åbnes som før. Når siden er åbnet, skrives adressen om til den nye form.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Bemærk**
>
> - Når du ikke er logget ind, gælder GitHub API'ets begrænsning (60 forespørgsler i timen). Til lagre med mange dokumenter eller gentagen læsning skal du trykke på [Log ind med GitHub].
> - Grennavne, der indeholder `/` (fx `feature/xxx`), kan angives med `?ref=` i adresseformen ovenfor. De kan ikke skrives i `?source=`-formen.
> - Dokumenterne indlæses med læserens egne GitHub-rettigheder. Personer uden læseadgang kan ikke se dem.

## Åbn dokumenter fra en lokal mappe

Tryk på [Åbn dokumenter] på værktøjslinjen, og vælg en mappe på enheden med [Åbn dokumenter fra en lokal mappe] i listen til venstre. Filerne behandles i browseren og sendes aldrig ud. Det virker i browsere, der understøtter valg af mapper (fx Chrome og Edge).

## Relaterede emner

- [Læs et privat lager](private-repository.md)
- [Kan ikke åbne eller logge ind i webversionen](../07-troubleshooting/web.md)
