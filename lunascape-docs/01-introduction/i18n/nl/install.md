# De extensie installeren

De VS Code-extensie "Lunascape Docs Pro" wordt verspreid als VSIX-bestand. Ze is gratis; "Pro" duidt de editie aan die werk aan een AI overdraagt en zichzelf bijwerkt.

## Systeemvereisten

- VS Code 1.90 of later
- Functies die schrijven — documenten maken, de INDEX ordenen, controle-instellingen opslaan, vertalen — werken alleen in een werkruimte die u in VS Code als vertrouwd hebt gemarkeerd.

## Installeren

1. Haal het VSIX-bestand op. Deze koppeling verwijst altijd naar de nieuwste versie.

   [lunascape-docs-pro.vsix downloaden](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Open de extensieweergave (`⇧⌘X` / `Ctrl+Shift+X`).
3. Kies [Installeren vanuit VSIX…] in het menu `…` rechtsboven en wijs het gedownloade bestand aan.

### Via de opdrachtregel

Eén regel, als u de terminal liever niet verlaat. Ze downloadt en installeert.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Opmerking**
> Als `code` niet wordt gevonden, voer dan [Shell-opdracht: 'code'-opdracht installeren in PATH] uit vanuit het opdrachtenpalet (`⇧⌘P` / `Ctrl+Shift+P`).

## Bijwerken

Wanneer er een nieuwere versie wordt gepubliceerd, haalt de extensie die op en installeert ze die. VS Code stelt voor het venster opnieuw te laden, en dan gaat u ermee aan de slag. Uw instellingen en documenten blijven ongewijzigd.

De controle gebeurt eenmaal per dag. Om nu meteen te controleren, voert u [Lunascape Docs: Controleren op een nieuwere versie] uit vanuit het opdrachtenpalet (`⇧⌘P` / `Ctrl+Shift+P`).

De instelling `lunascapeDocEditor.update.check` verandert wat er gebeurt.

| Instelling | Wat er gebeurt |
|---|---|
| Een nieuwere versie installeren zodra die wordt gepubliceerd | Standaard |
| Melden en per keer laten beslissen | Er verschijnt een melding, en er verandert niets totdat u op [Bijwerken] drukt |
| Niet controleren | Er gebeurt niets |

### Als het bijwerken niet lukt

"De update kon niet worden opgehaald: No Servers" betekent dat de geïnstalleerde versie 0.22.18 of ouder is. Het bijwerkpad van die versie mislukt telkens bij de laatste stap, zodat ze zichzelf niet naar een nieuwere versie kan brengen. Installeer één keer met de hand, zoals hierboven; daarna werkt ze zichzelf bij.

## De versie controleren

Open "Lunascape Docs Pro" in de extensieweergave om de geïnstalleerde versie te zien. U hebt die nodig bij het melden van een probleem.

## Verwante onderwerpen

- [Uw eerste documenten maken](first-documents.md)
- [Een probleem melden](../07-troubleshooting/report.md)
