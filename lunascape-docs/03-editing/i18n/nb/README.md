# Redigere et dokument

Dokumenter kan redigeres direkte i visningen. Redigeringsskjermen har en «visuell visning», der du redigerer det du ser, og en «Markdown-kildevisning»; én knapp veksler mellom dem.

## Starte redigeringen

Trykk på ett av følgende. Alle åpner den samme redigeringsskjermen.

- [Rediger] nederst til høyre i teksten
- [⋯] (flere handlinger) øverst til høyre i teksten → [Rediger]
- Elementmenyen i INDEX → [Rediger]

## Redigere

1. Rediger teksten direkte.
   På verktøylinjen øverst i redigeringsskjermen kan du bruke avsnittsformat (brødtekst, overskrift 1–4, sitat, kode), [Fet], [Kursiv], [Punktliste], [Nummerert liste], [Lenke], [Sett inn tabell], [Bildestørrelse], [Angre] og [Gjør om].
2. Når du vil redigere Markdown-kilden direkte, trykker du på [Markdown].
   Trykk en gang til for å gå tilbake til den visuelle visningen. Visningen du brukte sist, blir husket og gjenopprettet neste gang du trykker på [Rediger].
3. Trykk på [Lagre].
   Innholdet skrives til Markdown-filen, og visningen går tilbake til lesemodus. Trykk på [Avbryt] for å avslutte uten å lagre.

> **Merk**
>
> - Lagring skriver bare til filen. Git-staging og commit skjer aldri automatisk.
> - Matematikk og diagrammer som Mermaid, TikZ og Vega-Lite vises som gjengitt resultat i den visuelle visningen. Bytt til [Markdown] for å endre innholdet.
> - Dokumenter som inneholder MDX-spesifikk syntaks (komponenter, `import` og lignende) redigeres bare i Markdown-visningen for å bevare syntaksen.
> - Front matter (innstillingene øverst, omsluttet av `---`) bevares selv om du redigerer i den visuelle visningen.

> **Tips**
>
> - Trykk på [Åpne i VS Code] for å åpne filen i det vanlige tekstredigeringsprogrammet. Når du lagrer der, oppdateres visningen automatisk.
> - Når du ikke vil vise [Rediger]-knappen, slår du av [Redigeringsknappen] under [Visningsinnstillinger]. For å skjule den for hele prosjektet setter du `editor.showEditButton` til `false` i `lunascape-docs.json`.
> - Standardvisningen som åpnes først (visuell eller Markdown) kan du endre med innstillingen `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Relaterte emner

- [Opprette og organisere dokumenter og mapper](organize.md)
- [Justere bildestørrelsen](images.md)
- [Skrive matematikk](math.md)
- [Skrive diagrammer og grafer](diagrams.md)
