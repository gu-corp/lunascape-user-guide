# Åbn et GitHub-lager

I webversionen og i Lunascape kan du åbne og læse et GitHub-lager direkte uden at duplikere det. Du behøver ikke at logge ind for at åbne et offentligt lager.

## Åbn fra skærmen

1. Tryk på [Åbn dokumenter] (mappeikonet) på værktøjslinjen. Skærmen »Åbn dokumenter« åbnes.
2. Vælg i feltet til venstre, hvorfra du vil åbne.

   | Sted | Det vises her |
   |---|---|
   | Alle | Alt nedenfor. Det, du senest har åbnet, står øverst |
   | Senest åbnet | De lagre og mapper, du tidligere har åbnet |
   | Udvalgte | De vejledninger, som webstedet fremhæver |
   | GitHub-lagre | Når du er logget ind med GitHub: de lagre, du kan læse |
   | Denne computer | Mapper på denne enhed. I Lunascape vises duplikerede lagre også her |

3. Tryk på [Åbn] i den række, du vil åbne. Skriv i [Filtrér efter dokument- eller lagernavn] øverst for at begrænse rækkerne.

Et lager, der ikke er på listen, angiver du med [Åbn owner/repo] i feltet til venstre.

> **Tip**
>
> - Listen viser de GitHub-lagre, hvor GitHub-appen »Lunascape Docs« er installeret, og som du har læseadgang til. Hvis et lager mangler, skal du bede lagerets ejer om at tilføje appen.

## Se, hvor dokumentet ligger

Det lille ikon i venstre side af værktøjslinjen (placeringschippen) viser, hvor det dokument, du læser, ligger.

| Ikon | Placering |
|---|---|
| GitHub-logoet | Du læser fra GitHub. Dokumentet er ikke gemt på denne enhed |
| Computer | En mappe på denne enhed, som Lunascape administrerer. Navnet på Git-grenen og antallet af ændrede filer vises også |
| Mappe | En mappe på denne enhed |

Tryk på ikonet for at se placeringen, status og de handlinger, du kan udføre derfra, f.eks. [Vis på GitHub] og [Kopiér link].

## Dupliker et lager i Lunascape

I Lunascape kan du duplikere et GitHub-lager til denne enhed og derefter redigere og lave commits med Git.

- Tryk på [Dupliker] i lagerets række på skærmen »Åbn dokumenter«.
- Når du læser et lager, der er åbnet fra GitHub, skal du trykke på placeringschippen og derefter på [Dupliker til denne computer]. Når duplikeringen er færdig, åbnes det samme dokument fra kopien på denne enhed.

Et duplikeret lager er markeret med »På denne computer« på listen, og [Åbn på denne computer] står først.

## Åbn med en URL

Adressen består af lageret efterfulgt af dokumentets placering. Stien er placeringen i lageret, så rækkefølgen er den samme som i GitHub-URL'en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Det skal åbnes | Skrivemåde |
|---|---|
| Kun lageret (standardgren) | `/github/owner/repo` |
| Et dokument i lageret | `/github/owner/repo/docs/01-product/vision.md` |
| En bestemt gren eller et bestemt tag | Tilføj `?ref=v1.2.0` til sidst |

Adressen skifter, når du går til en anden side. Tryk på [Del dette dokument] på værktøjslinjen for at give andre et link til den side, du læser. Du kan også bruge browserens [Tilbage] og [Frem].

Adresser i den ældre `?source=`-form kan stadig åbnes. Når siden er åbnet, omskrives adressen til den nye form.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Bemærk**
>
> - Når du ikke er logget ind, gælder GitHub API's forbrugsgrænse (60 kald i timen). Brug [Log ind med GitHub], hvis lageret har mange dokumenter, eller hvis du læser i det mange gange.
> - Grennavne med `/` (f.eks. `feature/xxx`) kan angives med `?ref=` i adresseformen ovenfor. De kan ikke angives i `?source=`-formen.
> - Dokumenterne indlæses med læserens egne GitHub-rettigheder. Personer uden læseadgang kan ikke se dem.

## Åbn dokumenter fra en lokal mappe

Tryk på [Åbn dokumenter] på værktøjslinjen, og vælg en mappe på enheden via [Åbn dokumenter fra en lokal mappe] i feltet til venstre. Filerne behandles i browseren og sendes aldrig videre. Det virker i browsere, der understøtter valg af mapper (Chrome, Edge m.fl.).

## Relaterede emner

- [Læs et privat lager](private-repository.md)
- [Kan ikke åbne eller logge ind i webversionen](../07-troubleshooting/web.md)
