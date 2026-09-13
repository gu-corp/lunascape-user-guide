# Åpne et GitHub-repositorium

I Web-versjonen åpner du dokumenter ved å angi et GitHub-repositorium. For offentlige repositorier trengs ingen pålogging.

## Åpne fra skjermen

1. Åpne <https://docs.lunascape.org/>.
2. Trykk på [Åpne dokumenter] (mappeikonet) på verktøylinjen.
3. Skriv inn repositoriet under [Angi et repositorium direkte] og trykk på [Åpne].
   Når du er logget på GitHub, kan du også velge fra en liste under [Velg blant repositorier du kan lese].

> **Tips**
>
> - GitHub-ikonet ved siden av åpner dokumentet du leser nå på github.com. Det er ikke en handling for å åpne dokumenter.

## Åpne med URL

Adressen setter opp plasseringen av repositoriet og dokumentet slik den er. Banen er plasseringen inne i repositoriet, så den følger samme rekkefølge som GitHub-URL-en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Angivelse | Skrivemåte |
|---|---|
| Bare repositoriet (standardgren) | `/github/owner/repo` |
| Et dokument inne i repositoriet | `/github/owner/repo/docs/01-product/vision.md` |
| Angi en gren eller tagg | Legg til `?ref=v1.2.0` på slutten |

Adressen endres når du bytter side. Trykk på [Del dette dokumentet] på verktøylinjen for å gi videre en lenke til siden du leser nå. Nettleserens [Tilbake] og [Fram] fungerer også.

Den tidligere `?source=`-formen kan fortsatt åpnes som før. Etter at den er åpnet, skrives den om til den nye formen.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Merk**
>
> - Når du ikke er logget på, gjelder en bruksgrense for GitHub API (60 ganger per time). For repositorier med mange dokumenter eller ved gjentatt lesing bør du [Logg inn med GitHub].
> - Grennavn som inneholder `/` (for eksempel `feature/xxx`) kan angis med `?ref=` i adresseformen ovenfor. De kan ikke skrives i `?source=`-formen.
> - Dokumenter lastes inn med leserens egne GitHub-rettigheter. De vises ikke for personer uten leserettighet.

## Åpne dokumenter fra en lokal mappe

Trykk på [Åpne dokumenter] på verktøylinjen, og velg en mappe på enheten din via [Åpne dokumenter fra en lokal mappe] nederst i listen. Filene behandles inne i nettleseren og sendes aldri ut. Dette fungerer i nettlesere som støtter mappevalg (Chrome, Edge med flere).

## Relaterte emner

- [Lese et privat repositorium](private-repository.md)
- [Web-versjonen kan ikke åpne eller logge på](../07-troubleshooting/web.md)
