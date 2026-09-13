# Prosjektinnstillinger

`lunascape-docs.json` rett under dokumentroten er den teamdelte konfigurasjonen for den roten. Den håndteres i Git.

## Opprett eller rediger konfigurasjonsfilen

- Trykk på [Dokumentverktøy] i verktøylinjen → fanen [Kontroll] → [Hvor reglene kommer fra, og dokumentinnstillingene] → [Rediger dokumentinnstillingene] for å åpne filen i VS Code. Finnes ikke filen, opprettes en startfil i det øyeblikket.
- Filnavnet `lunascape-docs.json` knyttes automatisk til det medfølgende JSON Schema, som gir fullføring og en beskrivelse for hvert felt. En `$schema`-oppføring er ikke nødvendig.

## Eksempel

```json
{
  "id": "product-docs",
  "title": "Produktdokumentasjon",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Felter

| Felt | Betydning | Standard |
|---|---|---|
| `id` | Nøkkelen som visningsinnstillingene per bruker lagres under. Gi den en fast verdi for å beholde innstillingene når mappen flyttes | Mappebanen |
| `title` | Navnet som vises helt til venstre i verktøylinjen og i listen over dokumentrøtter. Det endres ikke med visningsspråket | Overskriften i rotens README/index, ellers mappenavnet |
| `indexTitle` | Overskriften til INDEX | `INDEX` |
| `startPage` | Dokumentet som åpnes først (relativt til dokumentroten) | `README.md` |
| `appearance` | Fargetema: `light` (alltid lyst) eller `auto` (følger VS Code-temaet) | `light` |
| `defaultLocale` | Standardspråket (språket til originaldokumentene) som en BCP 47-kode, for eksempel `ja`, `en` eller `zh-Hant`. Det er kilden for oversettelse | Ikke satt (utledet fra teksten kun for visning) |
| `fallbackLocale` | Språket som først vises til lesere hvis miljøspråk ikke samsvarer med noen av de støttede språkene. Angi et språk som finnes i `locales` | Ikke satt (`defaultLocale` brukes) |
| `locales` | De støttede språkene, inkludert `defaultLocale`. De vises i språkmenyen og er målspråkene for oversettelse | Bare `defaultLocale` |
| `ignoredDirectories` | Mappenavn som utelates fra INDEX, søk og kontroller. Å angi det erstatter standarden | `["99-archive"]` |
| `tree` | Standardverdier for hvordan INDEX vises. Brukere kan overstyre dem i Visningsinnstillinger | Som i eksempelet over |
| `editor.defaultMode` | Redigeringsvisningen som brukes inntil en bruker bytter: `visual` eller `source` | `visual` |
| `editor.showEditButton` | Om [Rediger] vises nederst til høyre i dokumentet | `true` |
| `documentStandards.pack` | Standard Pack som brukes til kontroller og maler: `builtin:<navn>` eller en bane relativt til dokumentroten | Ingen |
| `documentStandards.profile` | Et profilnavn definert av pakken | Ingen |
| `translation.enabled` | Aktiverer oversettelsesforslag og masseoversettelse | `true` |
| `translation.contextFiles` | Originale Markdown-filer (relativt til dokumentroten) som sendes til oversettelse som referanse for terminologi og stil | `[]` |
| `translation.maxContextCharacters` | Øvre grense for den samlede størrelsen på referansedokumentene (maksimalt 1048576) | `49152` |
| `description` | En linje om dokumentsettet, vist på kortene på et repositoriums hjemmeside. Som `title` kan den være en streng eller et objekt per språk | Ingen |

## Angi hvor dokumentene er

En `lunascape-docs.json` øverst i et repositorium kan inneholde et **kart over repositoriet** i stedet for innstillinger for den mappen. Å skrive et av de to første feltene under gjør den til et kart, og mappen som inneholder den er da ikke selv en dokumentrot.

| Felt | Hva det gjør | Standard |
|---|---|---|
| `defaultFolder` | Hvilken mappe som inneholder dokumentene (en bane relativt til denne mappen). Mappen den navngir trenger ingen egen konfigurasjon | Ingen (`docs` gjelder) |
| `roots` | Dokumentsettene, når det er flere (baner relativt til denne mappen, i visningsrekkefølge). Denne mappen blir da hjemmesiden | Ingen |
| `excludes` | Mapper som skal holdes utenfor rotoppdagelse (baner relativt til denne mappen). Legges til de innebygde utelatelsene som `node_modules` | `[]` |
| `home.cards` | Om en hjemmeside viser kortene for settene sine under README-en sin. Sett den til `false` hvis du skriver lenkene selv | `true` |

En dokumentrot finnes i denne rekkefølgen, første treff vinner.

1. En mappe angitt av en innstilling eller av kommandoen du kjørte
2. Det `defaultFolder` eller `roots` peker på i `lunascape-docs.json` øverst
3. En mappe som har en `lunascape-docs.json` (to eller flere under en felles overordnet mappe gjør den overordnede mappen til en hjemmeside)
4. En mappe kalt `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Selve toppen av repositoriet

> **Tips**
>
> Uten noe skrevet gjelder trinn 4, så et vanlig repositorium med én enkelt `docs/` oppfører seg akkurat som før. Skriv `defaultFolder` bare når mappen heter noe annet, for eksempel `manual`.

### Et eksempelkart

```json
{
  "title": "Lunascape-hjelp",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Prioritetsrekkefølge

Visningsrelaterte felter gjelder i denne rekkefølgen.

1. Brukerens visningsinnstillinger (panelet [Visningsinnstillinger])
2. VS Code-innstillinger (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Produktets standardverdier

Språk (`defaultLocale`, `fallbackLocale`, `locales`) er unntaket: `lunascape-docs.json` er autoritativ. Personlige VS Code-innstillinger kan ikke overstyre prosjektets språk.

> **Merk**
>
> En Standard Pack kan også angis som `standard` i `docs-lint.config.json`. Når begge finnes, vinner `docs-lint.config.json`.

## Relaterte emner

- [Endre kontrollregler](rules.md)
- [Endre visningsinnstillinger](../02-reading/display-settings.md)
- [Oversikt over VS Code-innstillinger](../08-reference/settings.md)
