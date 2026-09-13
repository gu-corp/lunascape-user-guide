# Skift dokumentrod

En dokumentrod er den øverste mappe i ét sæt dokumenter. INDEX, filtrering, kontrol og oversættelse arbejder alle pr. dokumentrod.

## Sådan findes en dokumentrod

Lunascape Docs følger de overordnede mapper op fra den åbnede Markdown-fil og bruger den nærmeste mappe, der svarer til en af følgende, som dokumentrod.

- En mappe, der indeholder `lunascape-docs.json` (mappens navn er uden betydning)
- En mappe med navnet `docs` (du kan tilføje flere navne med indstillingen `lunascapeDocEditor.rootDirectoryNames`)

Når du kører "Lunascape Docs: Åbn specifikationsfremviser", åbnes dokumentroden fra indstillingen `lunascapeDocEditor.root` (standard `docs`).

## Skift til en anden dokumentrod

Når arbejdsområdet har flere dokumentrødder, bliver dokumentrodens navn yderst til venstre på værktøjslinjen til en rullemenu.

1. Tryk på dokumentrodens navn yderst til venstre på værktøjslinjen.
2. Vælg en dokumentrod på listen.
   Startsiden for den valgte dokumentrod vises, og INDEX skifter.

> **Tip**
>
> Navnene på listen bestemmes i denne rækkefølge. De ændrer sig ikke, når du skifter visningssprog.
>
> 1. `title` i `lunascape-docs.json`
> 2. `navigation.title` i rodens `README.md`, ellers dens H1
> 3. `navigation.title` i rodens `index.md`, ellers dens H1
> 4. Mappens navn (for en standardmappe `docs` navnet på den overordnede mappe)

## Åbn en Markdown-fil uden for en dokumentrod

Når du åbner en Markdown-fil, der ikke ligger i en dokumentrod, vises filens mappe som en midlertidig dokumentrod. INDEX viser de Markdown-filer, der ligger i den mappe og under den.

- Tryk på [Til mappen ovenfor] på værktøjslinjen for at udvide visningen til den overordnede mappe i arbejdsområdet.
- I denne visning kan projektets sprogindstillinger og samlet oversættelse ikke bruges. Læg en `lunascape-docs.json` i mappen for at gøre den til en dokumentrod, så de kan bruges.

## Åbn altid en bestemt dokumentrod

Sæt indstillingen `lunascapeDocEditor.rootMode` til `fixed`, så dokumentroden i `lunascapeDocEditor.root` altid åbnes, uanset hvilken Markdown-fil du åbner.

## Relaterede emner

- [Dokumentrødder og filkonventioner](../04-document-tools/structure.md)
- [Projektindstillinger](../04-document-tools/project-configuration.md)
- [Oversigt over VS Code-indstillinger](../08-reference/settings.md)
