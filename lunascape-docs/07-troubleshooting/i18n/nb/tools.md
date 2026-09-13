# Kontroll, oppretting eller oversettelse fungerer ikke

## Kontroll

### «docs-lint er utilgjengelig» vises

- Utvidelsen mangler kjøremiljøet for docs-lint, eller det er et problem med konfigurasjonen. Installer utvidelsen på nytt.
- «For å laste inn den lokale pakken og konfigurasjonen på en trygg måte må du klarere dette arbeidsområdet i VS Code»: for å bruke en lokal Standard Pack kreves et klarert arbeidsområde.

### Resultatet blir stående på «må valideres på nytt»

Når du endrer et dokument eller en innstilling, blir det forrige resultatet ugyldig. Trykk [Kontroller dokumentroten] på nytt. Endringer du ikke har lagret, tas ikke med.

### Ingenting åpnes når du trykker på et funn

«Hele dokumentroten»-elementer er ikke knyttet til et bestemt dokument og har derfor ingen posisjon. Følg innholdet i funnet, og kontroller det aktuelle dokumentet.

### Reglene kan ikke lagres

- Et klarert arbeidsområde kreves.
- «Lint-konfigurasjonen ble endret av en annen operasjon»: `docs-lint.config.json` er endret eksternt. Last inn den nyeste tilstanden, og prøv igjen.
- Konfigurasjonsfiler som er symbolske lenker eller ligger utenfor dokumentroten, kan ikke redigeres.

## Oppretting fra en mal

- «Forhåndsvisningen av malen er utløpt» «Det du skrev inn, er endret»: trykk [Forhåndsvisning] på nytt før du oppretter.
- «Det finnes allerede et dokument på lagringsstedet»: eksisterende filer overskrives aldri. Angi et annet lagringssted.
- Lagringsstedet trenger en relativ bane fra dokumentroten og filtypen `.md` / `.mdx`. Ingenting kan opprettes under `i18n`.
- «Klarer arbeidsområdet for å opprette dokumenter»: klarer arbeidsområdet i VS Code.

<!-- ai-only:start -->
## Oversettelse

### Oversettelsesknappene er deaktivert

- «AI-oversettelse er ikke aktivert for denne dokumentroten»: sett `translation.enabled` til `true` i `lunascape-docs.json`.
- «Prosjektets standardspråk er ikke angitt»: lagre standardspråket i [Endre visningsinnstillinger](../02-reading/display-settings.md).
- «Legg oversettelsesmålet til blant språkene som støttes»: legg målspråket til i `locales`.
- «Finner ingen originaldokument å oversette»: du har åpnet en oversatt side. Bytt til siden på standardspråket.
- Samleoversettelse kan ikke brukes mens en mappe vises midlertidig. Legg en `lunascape-docs.json` i mappen for å gjøre den til en dokumentrot.

### Et forslag avvises eller må lages på nytt

- «Originaldokumentet er endret. Lag oversettelsesforslaget på nytt»: originalen eller målet endret seg etter at forslaget ble laget. Oversett på nytt.
- Hvis svaret fra språkmodellen mangler identifikatorer eller kode som skal beskyttes, godtas det ikke. Du kan se innholdet i svaret i utdatapanelet under «Lunascape Docs Oversettelse».
- «Samleoversettelse tar opptil 1000 dokumenter per kjøring»: del opp omfanget etter mappe eller ved eksplisitt utvalg.
<!-- ai-only:end -->

## Relaterte emner

- [Kontroller dokumenter](../04-document-tools/check.md)
- [Opprett et dokument fra en mal](../04-document-tools/templates.md)
- [Overlat arbeid til en AI](../05-ai/README.md)
