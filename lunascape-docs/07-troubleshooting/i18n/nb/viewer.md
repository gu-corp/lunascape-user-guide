# Dokumenter vises ikke

## «Finner ingen Markdown- eller docs-mappe å åpne» vises

- Arbeidsområdet har ingen `docs`-mappe, eller bruker et annet navn enn `docs`.
  - Legg en `lunascape-docs.json` i mappen, så gjenkjennes den som dokumentrot uansett navn.
  - Eller legg til mappenavnet i innstillingen `lunascapeDocEditor.rootDirectoryNames`.
- Hvis du ennå ikke har dokumenter, oppretter du dem med «Lunascape Docs: Opprett dokumentasjon fra mal».
- Du kan også åpne en Markdown-fil i editoren og deretter kjøre «Lunascape Docs: Åpne i spesifikasjonsviser».

## Et dokument vises ikke i INDEX

- Kontroller at filendelsen er `.md`, `.markdown` eller `.mdx`.
- Disse mappene vises ikke: mapper som begynner med `.`, `node_modules`, og mapper angitt i `ignoredDirectories` (standard er `99-archive`).
- Oversatte versjoner under `i18n/` vises ikke enkeltvis i INDEX. Bytt til dem fra språkmenyen.
- Hvis en fil du nettopp har lagt til, ikke vises, trykker du [Last inn på nytt].
- Du ser kanskje på en annen dokumentrot. Kontroller dokumentrotnavnet lengst til venstre på verktøylinjen.

## Ingenting vises når du trykker på en mappe

Mappens `README.md` er en «konfigurasjonsbeskrivelse» som bare har front matter og ingen brødtekst. Åpne mappen i INDEX og velg et dokument inni den.

## Feil dokumentrot åpnes

- Når innstillingen `lunascapeDocEditor.rootMode` er `fixed`, åpnes alltid `lunascapeDocEditor.root`.
- Med `auto` velges dokumentroten som er nærmest den åpnede Markdown-filen. Du kan bytte med nedtrekksmenyen lengst til venstre på verktøylinjen.

## Dokumentroten har et annet navn enn forventet

Navnet bestemmes i denne rekkefølgen: `title` i `lunascape-docs.json` → `navigation.title` i rotens `README.md` → dens H1 → `index.md` → mappenavnet. Angi `title` hvis du vil fastsette det.

## INDEX forsvant

- I en dokumentrot med bare ett dokument lukkes INDEX automatisk første gang. Du kan åpne den igjen med kolonnevisningsikonet på verktøylinjen. Du kan slå det av med [Skjul når det bare finnes ett dokument] under [Visningsinnstillinger].
- Når skjermen er smal, åpner du den fra [Åpne INDEX] (tre streker) til venstre for [Tilbake].

## En lenke åpnes ikke

- «Finner ikke lenkemålet»: målfilen finnes ikke. Du kan kontrollere interne lenker med [Kontroll] i Dokumentverktøy.
- «Åpnet ikke en usikker eller ikke-støttet lenke»: lenker utenfor dokumentroten, eller til andre skjemaer enn `https://` og `mailto:`, åpnes ikke.

## Feil språk vises

- Kontroller språket for siden som vises og grunnlaget for det, i språkmenyen.
- Visningsspråket du valgte sist, huskes. Velg standardspråket på nytt i språkmenyen.
- Hvis den personlige innstillingen `lunascapeDocEditor.locale` er satt, foretrekkes oversettelsen på det språket.

## Relaterte emner

- [Bytte dokumentrot](../02-reading/roots.md)
- [Dokumentrøtter og filkonvensjoner](../04-document-tools/structure.md)
