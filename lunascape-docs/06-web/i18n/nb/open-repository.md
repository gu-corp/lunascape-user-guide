# Åpne et GitHub-repositorium

I nettversjonen og i Lunascape kan du åpne og lese et GitHub-repositorium direkte, uten å klone det. Offentlige repositorier krever ikke innlogging.

## Åpne fra skjermen

1. Trykk på [Åpne dokumenter] (mappeikonet) på verktøylinjen. Skjermbildet «Åpne dokumenter» åpnes.
2. Velg i feltet til venstre hvor du vil åpne fra.

   | Sted | Hva som vises |
   |---|---|
   | Alle | Alt nedenfor. Det du har åpnet nylig, står først |
   | Nylig åpnet | Repositorier og mapper du har åpnet tidligere |
   | Anbefalt | Håndbøker som nettstedet anbefaler |
   | GitHub-repositorier | Repositoriene du kan lese, når du er logget inn med GitHub |
   | Denne datamaskinen | Mapper på denne enheten. I Lunascape vises også repositorier du har klonet, her |

3. Trykk på [Åpne] på raden du vil åpne. Skriv i [Filtrer etter dokumentnavn eller repositorienavn] øverst for å begrense radene.

Et repositorium som ikke står i listen, angir du med [Skriv inn owner/repo for å åpne] i feltet til venstre.

> **Tips**
>
> - GitHub-repositoriene i listen er de som har GitHub-appen «Lunascape Docs» installert, og som du har lesetilgang til. Hvis du ikke finner et repositorium, ber du eieren av repositoriet om å legge til appen.

## Se hvor dokumentet ligger

Det lille ikonet til venstre på verktøylinjen (plasseringsbrikken) viser hvor dokumentet du leser nå, ligger.

| Ikon | Plassering |
|---|---|
| GitHub-merket | Du leser fra GitHub. Ingenting er lagret på denne enheten |
| Datamaskin | En mappe på denne enheten som Lunascape administrerer. Git-grenen og antall endrede filer vises også |
| Mappe | En mappe på denne enheten |

Trykk på ikonet for å se plassering, status og hva du kan gjøre derfra, for eksempel [Vis på GitHub] og [Kopier lenke].

## Klone et repositorium i Lunascape

I Lunascape kan du klone et GitHub-repositorium til denne enheten og deretter redigere og committe med Git.

- Trykk på [Dupliser] på raden til repositoriet i skjermbildet «Åpne dokumenter».
- Når du leser et repositorium som er åpnet fra GitHub, trykker du på plasseringsbrikken og deretter på [Klon til denne datamaskinen]. Når kloningen er ferdig, åpnes det samme dokumentet fra kopien på denne enheten.

Et klonet repositorium er merket med «På denne datamaskinen» i listen, og [Åpne på denne datamaskinen] står først.

## Åpne med URL

Adressen består av repositoriet og plasseringen til dokumentet, i samme rekkefølge. Stien er plasseringen i repositoriet, så rekkefølgen er den samme som i GitHub-URL-en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Hva du angir | Skrivemåte |
|---|---|
| Bare repositoriet (standardgren) | `/github/owner/repo` |
| Et dokument i repositoriet | `/github/owner/repo/docs/01-product/vision.md` |
| En gren eller tagg | Legg til `?ref=v1.2.0` på slutten |

Adressen endres når du går til en annen side. Trykk på [Del dette dokumentet] på verktøylinjen for å gi noen en lenke til siden du leser nå. Nettleserens [Tilbake] og [Fram] fungerer også.

Den eldre formen med `?source=` kan fortsatt åpnes. Når siden er åpnet, skrives adressen om til den nye formen.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Merk**
>
> - Uten innlogging gjelder bruksgrensen for GitHub API (60 forespørsler per time). For repositorier med mange dokumenter eller ved gjentatt lesing bør du bruke [Logg inn med GitHub].
> - Grennavn som inneholder `/` (for eksempel `feature/xxx`), kan angis med `?ref=` i adresseformen ovenfor. De kan ikke skrives i formen med `?source=`.
> - Dokumentene lastes inn med leserens egne GitHub-tillatelser. Personer uten lesetilgang ser dem ikke.

## Åpne dokumenter fra en lokal mappe

Trykk på [Åpne dokumenter] på verktøylinjen, og velg en mappe på enheten via [Åpne dokumenter fra en lokal mappe] i feltet til venstre. Filene behandles i nettleseren og sendes aldri ut. Dette fungerer i nettlesere som støtter valg av mappe (Chrome, Edge og andre).

## Relaterte emner

- [Lese et privat repositorium](private-repository.md)
- [Nettversjonen åpner ikke, eller du kan ikke logge inn](../07-troubleshooting/web.md)
