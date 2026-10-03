# Rediger et dokument

Dokumenter kan redigeres direkte inde i visningsprogrammet. Redigeringsvisningen har en "visuel visning", hvor du redigerer det, du ser, og en "Markdown-kildevisning"; du skifter mellem dem med én knap.

## Begynd at redigere

Tryk på en af følgende. De åbner alle den samme redigeringsvisning.

- [Rediger] nederst til højre i dokumentet
- [⋯] (Flere handlinger) øverst til højre i dokumentet → [Rediger]
- Elementmenuen i INDEX → [Rediger]

## Rediger

1. Rediger teksten direkte.
   På værktøjslinjen øverst i redigeringsvisningen kan du bruge afsnitsformat (brødtekst, overskrift 1-4, citat, kode), [Fed], [Kursiv], [Punktliste], [Nummereret liste], [Link], [Indsæt tabel], [Billedstørrelse], [Fortryd] og [Gentag].
2. Tryk på [Markdown], når du vil redigere Markdown-kilden direkte.
   Tryk igen for at vende tilbage til den visuelle visning. Den senest brugte visning huskes og gendannes, næste gang du trykker på [Rediger].
3. Tryk på [Gem] (du kan også gemme med Ctrl+S/⌘S).
   Der skrives til Markdown-filen, og du vender tilbage til læsevisningen. Tryk på [Kassér redigeringer] for at stoppe med at redigere og vende tilbage til det senest gemte indhold.

## Begynd altid i redigeringsvisningen (redigeringstilstand)

Tryk på [Redigeringstilstand] på værktøjslinjen for at slå den til: derefter begynder hvert dokument i redigeringsvisningen. Brug den, når du skriver videre som i en notesblok.

- Så længe den er slået til, lukker redigeringsvisningen ikke, når du trykker på [Gem]. [Kassér redigeringer] vender tilbage til det senest gemte indhold og lader redigeringsvisningen være.
- Tryk igen for at slå den fra og vende tilbage til læsevisningen. Til/fra huskes for hver enkelt bruger.
- Den vises ikke i en dokumentrod, der ikke kan skrives til (f.eks. skrivebeskyttet på GitHub).

## Redigeringer, der ikke er gemt

Redigeringer, du ikke har gemt, bevares automatisk på denne enhed. De går ikke tabt, selv om du skifter til et andet dokument eller lukker fanen eller vinduet.

- [Ikke gemt] i redigeringsvisningen betyder, at der er forskel i forhold til det senest gemte indhold.
- Næste gang du åbner det samme dokument, fortsætter det fra de bevarede redigeringer og oplyser om det. Hvis det oprindelige dokument er blevet opdateret siden da, oplyses der også om det. Med [Kassér redigeringer] kan du vende tilbage til det nyeste indhold.
- De bevarede redigeringer forsvinder med [Gem] eller [Kassér redigeringer]. De er ikke gemt, så de optræder ikke i Git eller blandt kladder.

> **Bemærk**
>
> - Ved lagring skrives der kun til filen. Staging og commit i Git sker aldrig automatisk.
> - Matematik og diagrammer som Mermaid, TikZ og Vega-Lite vises som gengivet resultat i den visuelle visning. Skift til [Markdown] for at ændre deres indhold.
> - Dokumenter, der indeholder MDX-specifik syntaks (komponenter, `import` og lignende), redigeres kun i Markdown-visningen for at bevare syntaksen.
> - Front matter (indstillingerne omgivet af `---` i toppen) bevares, også når du redigerer i den visuelle visning.

> **Tip**
>
> - Tryk på [Åbn i VS Code] for at åbne filen i den almindelige teksteditor. Når du gemmer i teksteditoren, opdateres visningen i visningsprogrammet også automatisk.
> - Når du ikke vil have [Rediger]-knappen vist, skal du slå [Redigeringsknappen] fra under [Visningsindstillinger]. For at skjule den i hele projektet skal du sætte `editor.showEditButton` til `false` i `lunascape-docs.json`.
> - Standardvisningen, der åbnes først (visuel/Markdown), kan ændres med indstillingen `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Se også

- [Opret og organiser dokumenter og mapper](organize.md)
- [Juster størrelsen på billeder](images.md)
- [Skriv matematik](math.md)
- [Tegn diagrammer og grafer](diagrams.md)
