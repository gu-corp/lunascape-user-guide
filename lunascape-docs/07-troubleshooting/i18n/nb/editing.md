# Kan ikke redigere, lagre eller endre rekkefølge

## Det finnes ingen [Rediger]-knapp

- [Redigeringsknappen] i [Visningsinnstillinger] er slått av. Slå den på, eller bruk [⋯] → [Rediger] øverst til høyre i brødteksten, eller INDEX-elementets meny → [Rediger].
- Det samme gjelder når `editor.showEditButton` i `lunascape-docs.json` er `false`.
- Du kan ikke redigere mens hjelpen vises. Lukk hjelpen.

## Kan ikke bytte til visuell visning

«Dette dokumentet inneholder MDX-syntaks og kan derfor ikke åpnes i den vanlige redigeringsvisningen»: dokumenter som inneholder MDX-spesifikk syntaks (komponenter, `import` og lignende) redigeres bare i Markdown-visningen for å bevare syntaksen.

## Kan ikke redigere matematikk eller diagram direkte

Den visuelle visningen viser det gjengitte resultatet. Trykk [Markdown] i redigeringsvisningen og rediger kilden.

## Kan ikke endre rekkefølge eller dra

- Du kan ikke endre rekkefølgen mens du filtrerer, mens du redigerer et dokument, eller mens en annen INDEX-handling behandles.
- Når du ikke har klarert arbeidsområdet, er handlingene for å opprette, organisere og slette utilgjengelige. Klarer arbeidsområdet i VS Code.
- «INDEX er oppdatert. Dra på nytt.»: en annen endring ble nettopp tatt i bruk. Gjenta handlingen.
- Startsiden (rotens `README.md`) kan ikke flyttes.

## «Det finnes ulagrede endringer» vises

Målfilen redigeres i VS Code-editoren. Lagre eller forkast endringene først, og prøv deretter på nytt.

## Kan ikke endre navn

Følgende navn kan ikke brukes.

- Navn som begynner med `.`, `i18n`, og reserverte navn i Windows (`CON` og lignende)
- Navn som slutter med et punktum eller et mellomrom, og navn som inneholder kontrolltegn eller tegn som ikke er tillatt i filnavn
- Navn som allerede finnes i samme mappe (inkludert navn som bare skiller seg i store og små bokstaver)
- Dokumentnavn uten en Markdown-filendelse

## Lagrede endringer vises ikke i Git eller blir ikke committet

Lunascape Docs skriver bare til filen. Den verken staget eller committer i Git. Sjekk kildekontrollvisningen i VS Code og commit ved behov.

## Relaterte emner

- [Redigere et dokument](../03-editing/README.md)
- [Opprette og organisere dokumenter og mapper](../03-editing/organize.md)
- [Endre rekkefølgen på dokumenter](../03-editing/reorder.md)
