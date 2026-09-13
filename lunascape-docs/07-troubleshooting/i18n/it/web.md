# Impossibile aprire la versione Web o accedere

## Anche dopo l'accesso il repository non compare nell'elenco

L'App GitHub «Lunascape Docs» non è installata su quell'account, oppure il repository non è incluso. Chiedere al proprietario del repository o all'amministratore dell'organizzazione di installarla seguendo la procedura descritta in [Consultare un repository privato](../06-web/private-repository.md).

## Non si riesce a superare la schermata di accesso

- Non si dispone dell'autorizzazione di lettura sul repository. Chiedere al proprietario del repository di concederla.
- «Per questo sito non è configurato l'accesso con GitHub»: nel visualizzatore installato autonomamente non è configurato alcun servizio di accesso. È necessario che un amministratore lo configuri.

## La finestra pop-up di accesso non si apre

Il browser sta bloccando i pop-up. Consentire i pop-up per questo sito e riprovare.

## Viene visualizzato «La sessione di accesso è scaduta»

La sessione di accesso è scaduta. Premere di nuovo [Accedi con GitHub].

## L'apertura di un repository pubblico restituisce 404

- Verificare la forma `owner/repo@ref/dir`.
- Non è possibile indicare nomi di ramo che contengono `/`.

## Dopo un po' non si riesce più a caricare

Senza aver effettuato l'accesso si applica il limite di utilizzo dell'API di GitHub (60 chiamate all'ora). Quando viene visualizzato «Limite di chiamate raggiunto», attendere qualche istante oppure eseguire l'accesso con [Accedi con GitHub].

## Viene visualizzato «Questo sito non può mostrare questo repository»

Per aprirlo da un visualizzatore installato autonomamente, occorre aggiungere l'URL di quel sito a `viewer.origins` nel file `lunascape-docs.json` del repository.

## Aprendo `index.html` non viene visualizzato nulla

Non funziona se aperto direttamente con `file://`. Aprirlo tramite un server HTTP oppure usare la versione per VS Code.

## Nel sito esportato viene visualizzato «lunascape-docs-manifest.json non trovato»

Distribuire così com'è l'insieme completo dei file generati da `npm run export:web`, manifesto incluso.

## Non è possibile salvare la bozza

- «Impossibile aprire IndexedDB», «In uso in un'altra scheda»: la causa è la modalità di navigazione privata del browser oppure un'altra scheda che mostra lo stesso sito. Aprire il sito in una finestra normale e chiudere le altre schede.
- Le bozze vengono salvate per ciascun dispositivo e per ciascun browser. Non vengono trasferite a un altro dispositivo.

## Argomenti correlati

- [Aprire un repository GitHub](../06-web/open-repository.md)
- [Salvare una bozza](../06-web/drafts.md)
