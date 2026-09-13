# Il controllo, la creazione o la traduzione non riescono

## Controllo

### Viene visualizzato «docs-lint non è disponibile»

- L'estensione non include l'ambiente di esecuzione di docs-lint oppure la configurazione presenta un problema. Reinstallare l'estensione.
- «Per caricare in modo sicuro il pacchetto locale e la configurazione, considerare attendibile questa area di lavoro in VS Code»: per usare uno Standard Pack locale è necessaria un'area di lavoro attendibile.

### Il risultato resta su «nuova convalida necessaria»

Se si modifica un documento o un'impostazione, il risultato precedente non è più valido. Premere di nuovo [Controlla la radice della documentazione]. Le modifiche non salvate non vengono considerate.

### Premendo una segnalazione non si apre nulla

Le voci relative all'«intera radice della documentazione» non sono collegate a un documento specifico e quindi non hanno una posizione. Verificare i documenti indicati nel contenuto della segnalazione.

### Non è possibile salvare le regole

- È necessaria un'area di lavoro attendibile.
- «La configurazione di lint è stata modificata da un'altra operazione»: `docs-lint.config.json` è stato modificato dall'esterno. Caricare lo stato più recente e riprovare.
- Non è possibile modificare i collegamenti simbolici né i file di configurazione esterni alla radice della documentazione.

## Creazione da un modello

- «L'anteprima del modello è scaduta» / «I dati immessi sono cambiati»: premere di nuovo [Anteprima] prima di creare il documento.
- «Nella destinazione esiste già un documento»: i file esistenti non vengono mai sovrascritti. Indicare un'altra destinazione.
- La destinazione richiede un percorso relativo alla radice della documentazione e l'estensione `.md` o `.mdx`. Non è possibile creare documenti sotto `i18n`.
- «Per creare documenti, considerare attendibile l'area di lavoro»: rendere attendibile l'area di lavoro in VS Code.

<!-- ai-only:start -->
## Traduzione

### I pulsanti di traduzione non sono attivi

- «La traduzione con l'AI non è abilitata per questa radice della documentazione»: impostare `translation.enabled` su `true` in `lunascape-docs.json`.
- «La lingua predefinita del progetto non è impostata»: salvare la lingua predefinita come descritto in [Modificare le impostazioni di visualizzazione](../02-reading/display-settings.md).
- «Aggiungere la lingua di destinazione alle lingue supportate»: aggiungere la lingua di destinazione a `locales`.
- «Nessun documento canonico da tradurre»: è aperta una pagina tradotta. Passare alla pagina nella lingua predefinita.
- La traduzione in blocco non è disponibile quando una cartella è aperta temporaneamente. Inserire un file `lunascape-docs.json` nella cartella per renderla una radice della documentazione.

### Una proposta viene rifiutata o deve essere rigenerata

- «Il documento canonico è cambiato. Rigenerare la proposta di traduzione»: dopo la creazione della proposta, il documento canonico o la destinazione è cambiato. Eseguire di nuovo la traduzione.
- Una risposta del modello linguistico in cui mancano identificatori o codice da preservare non viene accettata. Il contenuto della risposta è consultabile nel pannello di output «Lunascape Docs 翻訳».
- «La traduzione in blocco elabora al massimo 1000 documenti per volta»: suddividere l'ambito per cartella o tramite una selezione esplicita.
<!-- ai-only:end -->

## Argomenti correlati

- [Controllare i documenti](../04-document-tools/check.md)
- [Creare un documento da un modello](../04-document-tools/templates.md)
- [Affidare il lavoro a un'AI](../05-ai/README.md)
