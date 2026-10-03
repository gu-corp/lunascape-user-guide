# Åpne et GitHub-repositorium

I nettversjonen kan du åpne og lese et GitHub-repositorium direkte, uten å klone det. Offentlige repositorier krever ingen pålogging.

## Åpne fra skjermen

1. Trykk på [Åpne dokumenter] (mappeikonet) på verktøylinjen. Skjermen «Åpne dokumenter» åpnes.
2. I feltet til venstre velger du hvor du vil åpne fra.

   | Sted | Hva som vises |
   |---|---|
   | Alle | Alt nedenfor. Det du har åpnet nylig, vises først |
   | Nylig åpnet | Repositorier og mapper du har åpnet tidligere |
   | Anbefalt | Håndbøker som nettstedet anbefaler |
   | GitHub-repositorier | Repositoriene du kan lese, når du er logget på med GitHub |
   | Denne datamaskinen | Mapper på denne enheten |

3. Trykk på [Åpne] på raden du vil åpne. Skriv i [Filtrer etter dokumentnavn eller repositorienavn] øverst for å begrense radene.

Et repositorium som ikke står i listen, angir du med [Skriv inn owner/repo og åpne] i feltet til venstre.

> **Tips**
>
> - GitHub-repositoriene i listen er de som har GitHub-appen «Lunascape Docs» installert, og som du har lesetilgang til. Hvis du ikke finner et repositorium, ber du eieren av repositoriet om å legge til appen.

## Se hvor dokumentet ligger

Det lille ikonet til venstre på verktøylinjen (stedsbrikken) viser hvor dokumentet du leser nå, ligger.

| Ikon | Sted |
|---|---|
| GitHub-merket | Leses fra GitHub. Ingenting er lagret på denne enheten |
| Mappe | En mappe på denne enheten |

Trykk på ikonet for å se stedet, statusen og hva du kan gjøre derfra, for eksempel [Vis på GitHub] og [Kopier lenke].

## Åpne med URL

Adressen består av repositoriet og plasseringen av dokumentet, i den rekkefølgen. Stien er plasseringen i repositoriet, så den har samme rekkefølge som GitHub-URL-en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Hva du angir | Skrivemåte |
|---|---|
| Bare repositoriet (standardgren) | `/github/owner/repo` |
| Et dokument i repositoriet | `/github/owner/repo/docs/01-product/vision.md` |
| En bestemt gren eller tagg | Legg til `?ref=v1.2.0` til slutt |

Adressen endres når du går til en annen side. Trykk på [Del dette dokumentet] på verktøylinjen for å dele en lenke til siden du leser. Nettleserens [Tilbake] og [Fram] fungerer også.

Den eldre `?source=`-formen kan fortsatt åpnes som før. Etter at siden er åpnet, skrives adressen om til den nye formen.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Merk**
>
> - Uten pålogging gjelder bruksgrensen for GitHub API (60 forespørsler i timen). For repositorier med mange dokumenter eller ved gjentatt lesing bør du bruke [Logg inn med GitHub].
> - Grennavn som inneholder `/` (for eksempel `feature/xxx`), kan angis med `?ref=` i adresseformen ovenfor. De kan ikke skrives i `?source=`-formen.
> - Dokumentene lastes inn med leserens egne GitHub-tillatelser. Personer uten lesetilgang ser dem ikke.

## Åpne dokumenter fra en lokal mappe

Trykk på [Åpne dokumenter] på verktøylinjen, og velg en mappe på enheten med [Åpne dokumenter fra en lokal mappe] i feltet til venstre. Filene behandles i nettleseren og sendes aldri ut. Dette fungerer i nettlesere som støtter valg av mappe (Chrome, Edge og andre).

## Relaterte emner

- [Lese et privat repositorium](private-repository.md)
- [Kan ikke åpne nettversjonen eller logge på](../07-troubleshooting/web.md)
