# Installare l'estensione

L'estensione VS Code «Lunascape Docs Pro» è distribuita come file VSIX. È gratuita; «Pro» indica l'edizione che affida il lavoro a un'IA e si aggiorna da sola.

## Requisiti

- VS Code 1.90 o successivo
- Le funzioni che scrivono file — creare documenti, organizzare l'INDEX, salvare le impostazioni dei controlli, tradurre — funzionano solo in un'area di lavoro che hai contrassegnato come attendibile in VS Code.

## Installare

1. Ottieni il file VSIX. Questo collegamento punta sempre alla versione più recente.

   [Scarica lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Apri la vista Estensioni (`⇧⌘X` / `Ctrl+Shift+X`).
3. Dal menu `…` in alto a destra scegli [Installa da VSIX...] e indica il file che hai scaricato.

### Da riga di comando

Una sola riga, se preferisci non lasciare il terminale. Scarica e installa.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Nota**
> Se `code` non viene trovato, esegui [Comando shell: installa il comando 'code' nel PATH] dalla Palette dei comandi (`⇧⌘P` / `Ctrl+Shift+P`).

## Aggiornare

Quando viene pubblicata una versione più recente, l'estensione la scarica e la installa. VS Code propone di ricaricare la finestra: è a quel punto che inizi a usarla. Le impostazioni e i documenti restano invariati.

Il controllo avviene una volta al giorno. Per verificare subito, esegui [Lunascape Docs: Controlla la presenza di aggiornamenti] dalla Palette dei comandi (`⇧⌘P` / `Ctrl+Shift+P`).

Il comportamento si cambia con l'impostazione `lunascapeDocEditor.update.check`.

| Impostazione | Comportamento |
|---|---|
| Installa una versione più recente quando ne viene pubblicata una | Predefinito |
| Avvisami e lasciami decidere ogni volta | Compare un avviso e nulla cambia finché non premi [Aggiorna] |
| Non controllare mai | Non succede nulla |

### Quando non si riesce ad aggiornare

Se compare «Impossibile scaricare l'aggiornamento: No Servers», la versione installata è la 0.22.18 o precedente. Il suo meccanismo di aggiornamento fallisce sempre all'ultimo passaggio dopo lo scaricamento, quindi non riesce a passare da solo a una versione più recente. Reinstalla una volta a mano, come sopra; da quel momento in poi si aggiorna da solo.

## Verificare la versione

Apri «Lunascape Docs Pro» nella vista Estensioni per vedere la versione installata. Ti servirà quando segnali un problema.

## Argomenti correlati

- [Creare i primi documenti](first-documents.md)
- [Segnalare un problema](../07-troubleshooting/report.md)
