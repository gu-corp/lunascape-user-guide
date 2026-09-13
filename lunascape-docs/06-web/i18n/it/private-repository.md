# Consultare un repository privato

I documenti dei repository privati possono essere consultati accedendo con GitHub, limitatamente a quelli per i quali si dispone dell'autorizzazione di lettura. Lunascape Docs non possiede account o autorizzazioni propri.

## Accedere e aprire

1. Aprire <https://docs.lunascape.org/>.
   Quando si indica un documento privato o non si è ancora effettuato l'accesso, viene visualizzata la schermata di accesso.
2. Premere [Accedi con GitHub].
   La schermata di autenticazione di GitHub si apre in una finestra pop-up.
3. Terminato l'accesso, premere [Apri i documenti] nella barra degli strumenti e scegliere il repository da aprire in [Scegli tra i repository leggibili].

> **Suggerimento**
>
> - Il nome dell'account con cui si è effettuato l'accesso è mostrato nella barra degli strumenti. Da qui è possibile anche [Esci] o [Accedi con un altro account].
> - Nell'elenco compaiono i repository, tra quelli per cui si dispone dell'autorizzazione di lettura, degli account (organizzazioni o singoli utenti) in cui è installata la GitHub App «Lunascape Docs».

## Configurazione a cura del proprietario del repository

Se il repository desiderato non compare nell'elenco, il proprietario del repository o l'amministratore dell'organizzazione deve installare la GitHub App «Lunascape Docs».

- Le autorizzazioni richieste sono Contents (lettura e scrittura) e Pull requests (lettura e scrittura). La lettura serve per la consultazione, la scrittura per la richiesta di pubblicazione dal Web (Pull Request). Lunascape Docs non memorizza il contenuto dei documenti.
- L'unità di installazione è l'account (organizzazione o singolo utente). Si sceglie se applicarla a «All repositories» (includendo automaticamente anche i repository creati in seguito) oppure solo ai repository selezionati.

| Situazione | Procedura |
|---|---|
| Introdurla in una nuova organizzazione o in un account personale | Procedere dalla [pagina di installazione](https://github.com/apps/lunascape-docs/installations/new) |
| Aggiungere repository in un'organizzazione in cui è già installata | Configurarla in Settings dell'organizzazione → GitHub Apps → Lunascape Docs → Configure → Repository access |

Anche installandola per l'intera organizzazione, ciascun membro può consultare solo i repository per cui possiede l'autorizzazione di lettura. Allo stesso modo, può inviare una richiesta di pubblicazione solo per i repository per cui possiede l'autorizzazione di scrittura.

> **Suggerimento**
> - In caso di nuova installazione, le autorizzazioni richieste vengono mostrate in un elenco nella schermata di installazione e si considerano approvate nel momento in cui si preme «Install». Non è necessaria alcuna operazione aggiuntiva.
> - Alle organizzazioni che avevano installato l'app prima dell'aggiunta di un'autorizzazione viene inviata un'email di conferma agli amministratori e compare un pulsante di approvazione nella parte superiore di Settings dell'organizzazione → GitHub Apps → Lunascape Docs → Configure. Fino all'approvazione, in quell'organizzazione è possibile solo la consultazione e, inviando una richiesta di pubblicazione, viene visualizzato «È necessaria la concessione dell'autorizzazione di scrittura».
> - Le autorizzazioni attualmente in vigore possono essere verificate nella stessa schermata Configure. Per un account personale si trova in Settings → Applications → Installed GitHub Apps.
> - Se un repository è stato escluso per errore o l'app è stata disinstallata, è possibile ripristinare lo stato precedente reinstallandola dalla [pagina di installazione](https://github.com/apps/lunascape-docs/installations/new). Il messaggio di rifiuto della richiesta di pubblicazione include un collegamento alla schermata per la correzione.
> - Se dal lato del repository non si desidera accettare richieste di pubblicazione, scrivere `"publish": { "enabled": false }` in `lunascape-docs.json`. La consultazione resta disponibile come sempre.

## Argomenti correlati

- [Aprire un repository di GitHub](open-repository.md)
- [Impossibile aprire o accedere nella versione Web](../07-troubleshooting/web.md)
