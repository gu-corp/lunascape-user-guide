# Projektkonfiguration

`lunascape-docs.json` direkte under dokumentroden er indstillingerne for den dokumentrod, teamet deler. Den styres med Git.

## Opret eller rediger konfigurationsfilen

- Tryk på [Dokumentværktøjer] på værktøjslinjen → fanen [Kontrol] → [Hvor reglerne kommer fra, og dokumentindstillingerne] → [Rediger dokumentindstillingerne], så åbnes filen i VS Code. Findes filen ikke, oprettes en indledende fil på det tidspunkt.
- Filnavnet `lunascape-docs.json` knyttes automatisk til det medfølgende JSON Schema, der giver forslag under indtastning og en beskrivelse af hvert felt. En `$schema`-post er ikke nødvendig.

## Eksempel på konfiguration

```json
{
  "id": "product-docs",
  "title": "Produktdokumentation",
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

## Beskrivelse af felterne

| Felt | Indhold | Standard |
|---|---|---|
| `id` | Nøglen, som visningsindstillingerne pr. bruger gemmes under. Giv den et fast id, når du vil beholde indstillingerne, selvom mappen flyttes | Mappens sti |
| `title` | Navnet, der vises yderst til venstre på værktøjslinjen og i oversigten over dokumentrødder. Det ændrer sig ikke, når visningssproget skiftes | Overskriften i rodens README/index, ellers mappenavnet |
| `indexTitle` | Overskriften på INDEX | `INDEX` |
| `startPage` | Det dokument, der åbnes først (relativt til dokumentroden) | `README.md` |
| `appearance` | Farvesættet: `light` (altid lyst) eller `auto` (følger temaet i VS Code) | `light` |
| `defaultLocale` | Standardsproget (originaldokumentets sprog). Angives med et BCP 47-sprogmærke (`ja`, `en`, `zh-Hant` osv.). Det er kilden til oversættelser | Ikke angivet (udledes af teksten til visning) |
| `fallbackLocale` | Det sprog, der først vises til læsere, hvis miljøs sprog ikke matcher nogen af de understøttede sprog. Angiv et sprog, der findes i `locales` | Ikke angivet (`defaultLocale` bruges) |
| `locales` | Oversigten over understøttede sprog. Inkludér `defaultLocale`. De bliver til sprogmenuen og til de mulige oversættelsesmål | Kun `defaultLocale` |
| `ignoredDirectories` | Mappenavne, der udelukkes fra INDEX, søgning og kontroller. Angives det, erstatter det standarden | `["99-archive"]` |
| `tree` | Standardværdierne for INDEX' visning. Brugeren kan tilsidesætte dem i visningsindstillingerne | Som i eksemplet ovenfor |
| `editor.defaultMode` | Redigeringsvisningen, indtil brugeren selv skifter. `visual` eller `source` | `visual` |
| `editor.showEditButton` | Om [Rediger] vises nederst til højre i dokumentet | `true` |
| `documentStandards.pack` | Den Standard Pack, der bruges til dokumentkontrol og skabeloner. `builtin:<navn>` eller en sti relativt til dokumentroden | Ingen |
| `documentStandards.profile` | Navnet på en profil, som pakken definerer | Ingen |
| `translation.enabled` | Aktiverer oprettelse af oversættelsesforslag og samlet oversættelse | `true` |
| `translation.contextFiles` | Original-Markdown (relativt til dokumentroden), der sendes med som reference for termer og stil ved oversættelse | `[]` |
| `translation.maxContextCharacters` | Øvre grænse for det samlede antal tegn i referencedokumenterne (højst 1048576) | `49152` |
| `description` | En linjes beskrivelse af dokumentsamlingen. Vises på kortet på lagerets hjemmeside. Ligesom `title` kan den skrives som en streng eller som et objekt pr. sprog | Ingen |

## Angiv, hvor dokumenterne ligger i lageret

En `lunascape-docs.json`, der ligger direkte i lageret, kan indeholde et **kort over lageret** i stedet for indstillingerne for den mappe. Skriver du et af de følgende tre felter, bliver den til et kort, og selve mappen bliver ikke en dokumentrod.

| Felt | Indhold | Standard |
|---|---|---|
| `defaultFolder` | Hvilken mappe dokumenterne ligger i (relativt til lagerets rod). Den mappe, der peges på, behøver ingen konfigurationsfil | Ingen (`docs` bruges) |
| `roots` | Oversigten, når der er flere dokumentsamlinger (relativt til lagerets rod, i visningsrækkefølge). I det tilfælde bliver roden til hjemmesiden | Ingen |
| `excludes` | Mapper, der udelukkes fra fund af dokumentrødder (relativt til lagerets rod). Lægges til de indbyggede udelukkelser som `node_modules` | `[]` |
| `home.cards` | Om hjemmesiden viser kort over dokumentsamlingerne under sin README. Sæt den til `false`, når du selv skriver linkene i README | `true` |

En dokumentrod bestemmes i denne rækkefølge. Oppefra og ned bruges den, der først findes.

1. Den mappe, du har angivet i en indstilling eller en kommando
2. Det, som `defaultFolder` eller `roots` i lagerets `lunascape-docs.json` peger på
3. Den mappe, der har en `lunascape-docs.json` (er der to eller flere under en fælles overordnet mappe, bliver den overordnede til hjemmesiden)
4. `docs`-mappen (`lunascapeDocEditor.rootDirectoryNames`)
5. Selve lagerets rod

> **Tip**
>
> Skriver du ikke noget, træder punkt 4 i kraft, så et almindeligt lager med én `docs/` fungerer som hidtil. Skriv kun `defaultFolder`, når mappen skal hedde noget andet, f.eks. `manual`.

### Eksempel på et kort

```json
{
  "title": "Lunascape Hjælp",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Konfigurationens prioritering

Felter, der handler om visning, prioriteres i denne rækkefølge.

1. Brugerens visningsindstillinger (panelet [Visningsindstillinger])
2. Indstillinger i VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Produktets standardværdier

Kun sprogene (`defaultLocale`, `fallbackLocale`, `locales`) er en undtagelse: her er `lunascape-docs.json` det gældende. Projektets sprog kan ikke tilsidesættes med personlige indstillinger i VS Code.

> **Bemærk**
>
> En Standard Pack kan også angives som `standard` i `docs-lint.config.json`. Findes den begge steder, vinder `docs-lint.config.json`.

## Relaterede emner

- [Ændr kontrolregler](rules.md)
- [Ændr visningsindstillinger](../02-reading/display-settings.md)
- [Oversigt over VS Code-indstillinger](../08-reference/settings.md)
