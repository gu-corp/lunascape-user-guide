# Dokumentrot og filkonvensjoner

Reglene Lunascape Docs følger for å finne dokumenter og bygge INDEX. Filsystemet er selv fasiten, så det trengs ingen fortegnelse eller byggekonfigurasjon.

## Dokumentrot

- Den nærmeste `docs`-mappen, eller en mappe som inneholder `lunascape-docs.json`, blir dokumentroten.
- Med en `lunascape-docs.json` trenger ikke mappen å hete `docs`.
- Åpner du en Markdown-fil utenfor enhver dokumentrot, vises mappen dens som en midlertidig dokumentrot.

## Filer som vises i INDEX

- Filene `.md`, `.markdown` og `.mdx` vises. Nye filer vises alltid, også uten front matter eller navigasjonsinformasjon.
- Mapper som begynner med `.`, `node_modules`, og mappene som er oppført i `ignoredDirectories` (standard `99-archive`) vises ikke.
- Alt under `i18n/` behandles som oversettelser og oppføres ikke separat i INDEX.

## Forsider for mapper

- En `README.md` (eller `index.md` når det ikke finnes noen README) med brødtekst er forsiden til mappen sin. Trykker du på mappenavnet i INDEX, åpnes forsiden.
- En `README.md` som bare består av front matter, uten brødtekst, behandles som en «deskriptor kun for innstillinger» og vises ikke som en side. Bruk den når en mappe bare trenger en tittel eller en rekkefølge.
- Når både `README.md` og `index.md` finnes, har `README.md` forrang.

## Standardspråk og oversettelser

- Dokumenter på standardspråket (originaldokumentet) blir liggende der de er.
- En oversettelse legges i en `i18n/<språk>/`-mappe ved siden av dokumentet, med samme filnavn. Å gjenskape mappestrukturen under `i18n/` gjenkjennes ikke.
- Det er det eneste stedet en oversettelse hentes fra. Den samme filen lagt et hvilket som helst annet sted blir en foreldreløs fil som ingen dokumenter gjør krav på som sin oversettelse.

```text
docs/
  lunascape-docs.json
  README.md                  ← forsiden til roten (startside)
  i18n/en/README.md          ← den engelske oversettelsen av den
  01-product/
    README.md                ← forsiden til mappen
    requirements.md
    i18n/en/README.md        ← de engelske oversettelsene av de to over
    i18n/en/requirements.md
  99-archive/                ← utelatt fra INDEX som standard
```

## Om `_meta.json`

Nextras `_meta.json` brukes ikke til navigasjon. Eksisterende filer blir verken endret eller slettet. En fremtidig, eksplisitt import-/eksportfunksjon blir det eneste som håndterer dem.

## Relaterte emner

- [Angi navigasjonsinformasjon](navigation-metadata.md)
- [Prosjektkonfigurasjon](project-configuration.md)
- [Bytte dokumentrot](../02-reading/roots.md)
