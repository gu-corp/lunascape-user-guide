# Ændre visningsindstillinger

Under [Visningsindstillinger] (tandhjul) på værktøjslinjen kan hver bruger ændre, hvordan INDEX vises, og om redigeringsknappen vises.

1. Tryk på [Visningsindstillinger] på værktøjslinjen.
2. Slå de punkter til eller fra, du vil ændre. Ændringerne træder i kraft med det samme.
3. Tryk på [Visningsindstillinger] igen, eller tryk uden for panelet, for at lukke det.

## Punkter, du kan indstille

| Afsnit | Punkt | Funktion |
|---|---|---|
| Dokumentets sprog | (aktuel tilstand) | Viser projektets standardsprog og det sprog, der vises nu. [Angiv projektets sprog…] åbner projektets sprogindstillinger |
| Indhold | [Filnavne] | Viser filnavne i stedet for dokumentnavne |
| | [Dokumentikoner] | Viser et ikon ved hvert dokument |
| | [Mappeikoner] | Viser et ikon ved hver mappe |
| | [Antal i mappen] | Viser antallet af dokumenter i mappen |
| | [Niveaulinjer] | Viser hjælpelinjer, der angiver niveauerne |
| | [Skjul automatisk, hvis der kun er ét dokument] | Lukker INDEX automatisk, men kun første gang, i en dokumentrod med kun ét dokument |
| | [Fold dokumentoplysningerne sammen] | Folder administrationstabellen øverst i dokumentet sammen til linjen "Dokumentoplysninger". Når indstillingen er slået fra, vises tabellen, som den er |
| | [Visningstæthed] | Vælger linjeafstanden i INDEX mellem [Normal] og [Kompakt] |
| | [Redigeringsknappen] | Viser [Rediger] nederst til højre i teksten |
| Handlinger | [Gendan projektets standarder] | Fjerner alle dine ændringer og vender tilbage til projektets indstillinger |
| | [Åbn indstillingerne for udvidelsen] | Åbner indstillingerne for Lunascape Docs i VS Code's indstillinger |

> **Tip**
>
> - Visningsindstillingerne gemmes for hver bruger og hver dokumentrod og skrives aldrig til filer, der er under Git.
> - Indstillingerne har prioritet i rækkefølgen "brugerens visningsindstillinger → VS Code-indstillinger → `lunascape-docs.json` → produktets standarder". Fælles standarder for teamet fastlægges med `tree` og `editor` i `lunascape-docs.json`.

## Skifte farver

Tryk på temaskiftet (sol/måne) på værktøjslinjen for at skifte mellem hvid baggrund og VS Code's farver. Hvilke farver der bruges ved åbning, bestemmes af indstillingen `lunascapeDocEditor.appearance` (`light` eller `auto`).

## Relaterede emner

- [Brug af INDEX](index-panel.md)
- [Projektindstillinger](../04-document-tools/project-configuration.md)
- [Oversigt over VS Code-indstillinger](../08-reference/settings.md)
