# Redigere et dokument

Dokumenter kan redigeres rett i visningsprogrammet. Redigeringsvinduet har en visuell visning, der du redigerer det du ser, og en Markdown-kildevisning; én knapp veksler mellom dem.

## Begynne å redigere

Trykk på ett av følgende. Alle åpner det samme redigeringsvinduet.

- [Rediger] nederst til høyre i teksten
- [⋯] (flere handlinger) øverst til høyre i teksten → [Rediger]
- Elementmenyen i INDEX → [Rediger]

## Redigere

1. Rediger teksten direkte.
   På verktøylinjen øverst i redigeringsvinduet kan du bruke avsnittsformat (brødtekst, overskrift 1–4, sitat, kode), [Fet], [Kursiv], [Punktliste], [Nummerert liste], [Lenke], [Sett inn tabell], [Bildestørrelse], [Angre] og [Gjør om].
2. Når du vil redigere Markdown-kilden direkte, trykker du på [Markdown].
   Trykk på den igjen for å gå tilbake til den visuelle visningen. Visningen du brukte sist, huskes og gjenopprettes neste gang du trykker på [Rediger].
3. Trykk på [Lagre] (du kan også lagre med Ctrl+S / ⌘S).
   Innholdet skrives til Markdown-filen, og du kommer tilbake til lesevisningen. Når du vil avslutte redigeringen og gå tilbake til det som sist ble lagret, trykker du på [Forkast endringer].

## Alltid begynne i redigeringsvinduet (redigeringsmodus)

Trykk på [Redigeringsmodus] på verktøylinjen for å slå den på: da begynner du i redigeringsvinduet hver gang du åpner et dokument. Bruk dette når du skriver videre, slik som i en notisblokk.

- Mens den er på, lukkes ikke redigeringsvinduet når du trykker på [Lagre]. [Forkast endringer] går tilbake til det som sist ble lagret, og lar redigeringsvinduet stå åpent.
- Trykk på den igjen for å slå den av og gå tilbake til lesevisningen. På/av huskes per bruker.
- Den vises ikke på en dokumentrot som ikke kan skrives til (for eksempel en skrivebeskyttet kilde på GitHub).

## Ikke lagrede endringer

Endringer du ikke har lagret, holdes automatisk på denne enheten. De går ikke tapt selv om du går til et annet dokument eller lukker fanen eller vinduet.

- [Ikke lagret] i redigeringsvinduet betyr at teksten skiller seg fra det som sist ble lagret.
- Neste gang du åpner det samme dokumentet, fortsetter du fra de bevarte endringene, og du får beskjed om det. Hvis selve dokumentet er blitt oppdatert siden, får du beskjed om det også. Med [Forkast endringer] kan du gå tilbake til det nyeste innholdet.
- De bevarte endringene forsvinner med [Lagre] eller [Forkast endringer]. Ettersom ingenting er lagret, vises de ikke i Git eller blant utkast.

> **Merk**
>
> - Lagring skriver bare til filen. Git-klargjøring og commit skjer aldri automatisk.
> - Matematikk og diagrammer som Mermaid, TikZ og Vega-Lite vises som ferdig opptegnet i den visuelle visningen. Bytt til [Markdown] for å endre innholdet i dem.
> - Dokumenter som inneholder MDX-spesifikk syntaks (komponenter, `import` og lignende) redigeres bare i Markdown-visningen, for å bevare syntaksen.
> - Front matter (innstillingene øverst omgitt av `---`) bevares selv om du redigerer i den visuelle visningen.

> **Tips**
>
> - [Åpne i VS Code] åpner filen i det vanlige tekstredigeringsprogrammet. Når du lagrer der, oppdateres visningsprogrammet automatisk.
> - Når du ikke vil vise [Rediger]-knappen, slår du av [Redigeringsknappen] i [Visningsinnstillinger]. For å skjule den for hele prosjektet setter du `editor.showEditButton` til `false` i `lunascape-docs.json`.
> - Standardvisningen som åpnes først (visuell eller Markdown), kan endres med innstillingen `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Se også

- [Opprette og organisere dokumenter og mapper](organize.md)
- [Justere bildestørrelse](images.md)
- [Skrive matematikk](math.md)
- [Skrive diagrammer og grafer](diagrams.md)
