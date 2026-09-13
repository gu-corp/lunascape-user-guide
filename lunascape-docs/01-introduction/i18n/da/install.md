# Installer udvidelsen

VS Code-udvidelsen »Lunascape Docs Pro« distribueres som en VSIX-fil. Den er gratis. »Pro« angiver den udgave, der kan give arbejde videre til en AI og opdatere sig selv.

## Systemkrav

- VS Code 1.90 eller nyere
- Funktioner, der skriver filer — oprettelse af dokumenter, organisering fra INDEX, lagring af kontrolindstillinger, oversættelse — fungerer kun i et arbejdsområde, du har markeret som betroet i VS Code.

## Installer

1. Hent VSIX-filen. Dette link peger altid på den nyeste version.

   [Download lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Åbn udvidelsesvisningen (`⇧⌘X` / `Ctrl+Shift+X`).
3. Vælg [Installer fra VSIX...] i `…`-menuen øverst til højre, og angiv den fil, du har hentet.

### Fra kommandolinjen

Du kan også klare det med én linje fra terminalen. Den henter og installerer i ét hug.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Bemærk**
> Hvis `code` ikke findes, skal du køre [Shell-kommando: Installer 'code'-kommandoen i PATH] fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

## Opdatér

Når en nyere version udgives, henter og installerer udvidelsen den selv. VS Code beder dig genindlæse vinduet, og det er dér, den skiftes ind. Dine indstillinger og dokumenter forbliver, som de er.

Den søger én gang om dagen. Hvis du vil søge med det samme, skal du køre [Lunascape Docs: Søg efter en nyere version] fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

Du kan ændre adfærden med indstillingen `lunascapeDocEditor.update.check`.

| Indstilling | Adfærd |
|---|---|
| Installer en nyere version, når en udgives | Standard |
| Giv besked, og lad mig bestemme hver gang | En besked vises, og intet ændres, før du trykker på [Opdatér] |
| Søg aldrig | Der sker ingenting |

### Når den ikke kan opdatere

Hvis der står »Opdateringen kunne ikke hentes: No Servers«, er den installerede version 0.22.18 eller ældre. Dens opdateringsfunktion fejler altid i det sidste trin efter hentningen, så den kan ikke selv komme til en nyere version. Installer den én gang manuelt som beskrevet ovenfor; derefter opdaterer den sig selv.

## Kontrollér versionen

Åbn »Lunascape Docs Pro« i udvidelsesvisningen for at se den installerede version. Du får brug for den, når du rapporterer et problem.

## Relaterede emner

- [Opret dine første dokumenter](first-documents.md)
- [Rapportér et problem](../07-troubleshooting/report.md)
