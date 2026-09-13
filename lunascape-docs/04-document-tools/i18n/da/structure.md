# Dokumentrødder og filkonventioner

Reglerne, som Lunascape Docs følger for at finde dokumenter og bygge INDEX. Filsystemet er selv originalen, så der er ikke brug for et register eller en byggekonfiguration.

## Dokumentrod

- Den nærmeste `docs`-mappe, eller en mappe med `lunascape-docs.json`, bliver dokumentroden.
- Med en `lunascape-docs.json` behøver mappen ikke at hedde `docs`.
- Åbner du en Markdown-fil uden for en dokumentrod, vises dens mappe som en midlertidig dokumentrod.

## Filer, der vises i INDEX

- Filerne `.md`, `.markdown` og `.mdx` vises. Nye filer vises altid, også uden front matter eller navigationsoplysninger.
- Mapper, der begynder med `.`, `node_modules` og de mapper, der er angivet i `ignoredDirectories` (som standard `99-archive`), vises ikke.
- Alt under `i18n/` behandles som oversættelser og vises ikke særskilt i INDEX.

## Mappens forside

- En `README.md` (eller `index.md`, hvis der ikke er en README) med indhold er mappens forside. Tryk på mappenavnet i INDEX for at åbne den.
- En `README.md`, der kun består af front matter uden indhold, behandles som en "beskrivelse udelukkende til opsætning" og vises ikke som en side. Brug den, når en mappe kun skal have en titel eller en rækkefølge.
- Findes både `README.md` og `index.md`, har `README.md` forrang.

## Standardsprog og oversættelser

- Dokumenter på standardsproget (originaldokumenterne) bliver, hvor de er.
- En oversættelse lægges i `i18n/<sprog>/` i samme mappe som originaldokumentet og med samme filnavn. Genopbygger du mappestrukturen under `i18n/`, genkendes den ikke.
- Det er det eneste sted, en oversættelse findes. Den samme fil lagt et andet sted er en løsrevet fil, som intet dokument regner for sin oversættelse.

```text
docs/
  lunascape-docs.json
  README.md                  ← dokumentrodens forside (startside)
  i18n/en/README.md          ← den engelske udgave
  01-product/
    README.md                ← mappens forside
    requirements.md
    i18n/en/README.md        ← de engelske udgaver af de to ovenstående
    i18n/en/requirements.md
  99-archive/                ← udeladt af INDEX som standard
```

## Om `_meta.json`

Nextras `_meta.json` bruges ikke til navigation. Eksisterende filer bliver hverken ændret eller slettet. Fremover håndteres de kun af en udtrykkelig funktion til import og eksport.

## Relaterede emner

- [Angiv navigationsoplysninger](navigation-metadata.md)
- [Projektindstillinger](project-configuration.md)
- [Skift dokumentrod](../02-reading/roots.md)
