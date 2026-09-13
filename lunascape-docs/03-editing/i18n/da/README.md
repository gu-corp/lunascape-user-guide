# Rediger et dokument

Dokumenter kan redigeres direkte i fremviseren. Redigeringsvisningen har en visuel visning, hvor du redigerer det, du ser, og en visning af Markdown-kilden; én knap skifter mellem dem.

## Begynd at redigere

Tryk på en af følgende. De åbner alle den samme redigeringsvisning.

- [Rediger] nederst til højre i dokumentet
- [⋯] (Flere handlinger) øverst til højre i dokumentet → [Rediger]
- Menuen for et punkt i INDEX → [Rediger]

## Rediger

1. Rediger teksten direkte.
   Værktøjslinjen øverst i redigeringsvisningen giver dig afsnitsformat (brødtekst, overskrift 1-4, citat, kode), [Fed], [Kursiv], [Punktliste], [Nummereret liste], [Link], [Indsæt tabel], [Billedstørrelse], [Fortryd] og [Gentag].
2. Tryk på [Markdown], når du vil redigere Markdown-kilden direkte.
   Tryk på den igen for at vende tilbage til den visuelle visning. Den visning, du brugte sidst, huskes og gendannes, næste gang du trykker på [Rediger].
3. Tryk på [Gem].
   Markdown-filen skrives, og fremviseren vender tilbage til læsevisningen. Tryk på [Annuller], hvis du vil lade være.

> **Bemærk**
>
> - Når du gemmer, skrives filen blot. Git-staging og commit sker aldrig automatisk.
> - Matematik og diagrammer som Mermaid, TikZ og Vega-Lite vises færdigtegnet i den visuelle visning. Skift til [Markdown] for at ændre deres indhold.
> - Dokumenter med MDX-specifik syntaks (komponenter, `import` og lignende) redigeres kun i Markdown-visningen, så syntaksen bevares.
> - Front matter (indstillingerne mellem `---`-linjerne øverst) bevares, når du redigerer i den visuelle visning.

> **Tip**
>
> - Tryk på [Åbn i VS Code] for at åbne filen i det almindelige teksteditorvindue. Når du gemmer der, opdateres fremviseren automatisk.
> - Slå [Redigeringsknappen] fra under [Visningsindstillinger], hvis du ikke vil have vist knappen [Rediger]. Sæt `editor.showEditButton` til `false` i `lunascape-docs.json` for at skjule den i hele projektet.
> - Den visning, der åbnes først (visuel eller Markdown), ændrer du med indstillingen `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Relaterede emner

- [Opret og organiser dokumenter og mapper](organize.md)
- [Juster størrelsen på billeder](images.md)
- [Skriv matematik](math.md)
- [Tegn diagrammer og grafer](diagrams.md)
