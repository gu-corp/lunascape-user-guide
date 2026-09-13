# Installera tillägget

VS Code-tillägget ”Lunascape Docs Pro” distribueras som en VSIX-fil. Det är kostnadsfritt. ”Pro” anger att det är den utgåva som lämnar över arbete till en AI och uppdaterar sig själv.

## Systemkrav

- VS Code 1.90 eller senare
- Funktioner som innebär skrivning – att skapa dokument, ordna INDEX, spara kontrollinställningar, översätta med mera – fungerar bara i en arbetsyta som du har markerat som ”betrodd” i VS Code.

## Installera

1. Hämta VSIX-filen. Den här länken pekar alltid på den senaste versionen.

   [Ladda ner lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Öppna tilläggsvyn i VS Code (`⇧⌘X` / `Ctrl+Shift+X`).
3. Välj [Installera från VSIX...] i menyn `…` uppe till höger och ange filen du hämtade.

### Installera från kommandoraden

Du kan klara det på en rad från terminalen. Den hämtar och installerar i följd.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Obs**
> Om `code` inte hittas kör du [Skalkommando: Installera kommandot code i PATH] från kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

## Uppdatera

När en nyare version publiceras hämtar och installerar tillägget den själv. När VS Code ber dig läsa in fönstret igen är det då den träder i kraft. Dina inställningar och dokument lämnas orörda.

Kontrollen sker en gång om dagen. Vill du kontrollera direkt kör du [Lunascape Docs: Sök efter uppdatering] från kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

Beteendet kan ändras med inställningen `lunascapeDocEditor.update.check`.

| Inställning | Beteende |
|---|---|
| Installera en nyare version när den publiceras | Standard |
| Meddela mig och låt mig avgöra varje gång | Ett meddelande visas, och inget byts ut förrän du trycker på [Uppdatera] |
| Kontrollera aldrig | Inget händer |

### När uppdatering inte går

Om meddelandet ”Uppdateringen kunde inte hämtas: No Servers” visas är den installerade versionen 0.22.18 eller tidigare. Den versionens uppdateringsfunktion misslyckas alltid i steget efter hämtningen, så den kan inte förnya sig själv. Installera om den för hand en gång enligt stegen ovan. Därefter uppdaterar den sig själv.

## Kontrollera versionen

Öppna ”Lunascape Docs Pro” i tilläggsvyn för att se vilken version som är installerad. Du behöver den när du rapporterar ett fel.

## Relaterade ämnen

- [Skapa dina första dokument](first-documents.md)
- [Rapportera ett fel](../07-troubleshooting/report.md)
