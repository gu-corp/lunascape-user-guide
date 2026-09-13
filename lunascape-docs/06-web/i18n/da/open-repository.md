# Åbn et GitHub-lager

I Web-visningen åbner du dokumenter ved at angive et GitHub-lager. Offentlige lagre kræver ikke login.

## Åbn fra skærmen

1. Åbn <https://docs.lunascape.org/>.
2. Tryk på [Åbn dokumenter] (mappeikonet) på værktøjslinjen.
3. Indtast lageret under [Angiv et lager], og tryk på [Åbn].
   Når du er logget ind på GitHub, kan du også vælge fra en liste under [Vælg blandt lagre, du kan læse].

> **Tip**
>
> - GitHub-ikonet ved siden af åbner det dokument, du læser nu, på github.com. Det åbner ikke dokumenter her.

## Åbn via URL

Adressen angiver lageret og dokumentets placering i den rækkefølge, de står i lageret. Stien er placeringen inde i lageret, så den følger samme rækkefølge som GitHub-URL'en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Angivelse | Sådan skrives det |
|---|---|
| Kun lageret (standardgren) | `/github/owner/repo` |
| Et dokument inde i lageret | `/github/owner/repo/docs/01-product/vision.md` |
| Angiv en gren eller et mærkat | tilføj `?ref=v1.2.0` til sidst |

Adressen ændrer sig, når du navigerer. Tryk på [Del dette dokument] på værktøjslinjen for at give nogen et link til den side, du læser nu. Browserens knapper [Tilbage] og [Frem] virker også.

Den ældre `?source=`-form kan stadig åbnes som hidtil. Efter åbningen skrives den om til den nye form.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Bemærk**
>
> - Når du ikke er logget ind, gælder der en grænse for brug af GitHub API (60 gange i timen). Log ind med [Log ind med GitHub] ved lagre med mange dokumenter eller ved gentagen læsning.
> - Grennavne, der indeholder `/` (som `feature/xxx`), kan angives med `?ref=` i adresseformen ovenfor. De kan ikke skrives i `?source=`-formen.
> - Dokumenter indlæses med læserens egne GitHub-rettigheder. De vises ikke for personer uden læserettigheder.

## Åbn dokumenter fra en lokal mappe

Tryk på [Åbn dokumenter] på værktøjslinjen, og vælg en mappe på enheden via [Åbn dokumenter fra en lokal mappe] under listen. Filerne behandles inde i browseren og sendes aldrig ud. Det virker i browsere, der understøtter valg af mappe (Chrome, Edge med flere).

## Relaterede emner

- [Læs et privat lager](private-repository.md)
- [Web-visningen kan ikke åbne eller logge ind](../07-troubleshooting/web.md)
