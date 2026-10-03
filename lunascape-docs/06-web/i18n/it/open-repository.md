# Aprire un repository GitHub

Nella versione Web e in Lunascape puoi aprire un repository GitHub e leggerlo così com'è, senza clonarlo. Per i repository pubblici non è necessario accedere.

## Aprire dalla schermata

1. Premi [Apri i documenti] (l'icona della cartella) nella barra degli strumenti. Si apre la schermata «Apri i documenti».
2. Nella colonna di sinistra, scegli dove cercare.

   | Posizione | Cosa elenca |
   |---|---|
   | Tutti | Tutto ciò che segue. Gli elementi aperti di recente compaiono per primi |
   | Aperti di recente | I repository e le cartelle che hai aperto finora |
   | In evidenza | I manuali presentati dal sito |
   | Repository GitHub | Quando hai effettuato l'accesso con GitHub, i repository che puoi leggere |
   | Questo computer | Le cartelle di questo dispositivo. In Lunascape compaiono qui anche i repository clonati |

3. Premi [Apri] nella riga che vuoi aprire. Per restringere l'elenco, digita nel campo [Filtra per nome del documento o del repository] in alto.

Se un repository non compare nell'elenco, indicalo con [Inserisci owner/repo e apri] nella colonna di sinistra.

> **Suggerimento**
>
> - L'elenco mostra i repository GitHub su cui è installata la GitHub App «Lunascape Docs» e per cui hai il permesso di lettura. Se un repository non compare, chiedi al suo proprietario di aggiungere l'App.

## Verificare la posizione di un documento

La piccola icona sul lato sinistro della barra degli strumenti (il chip della posizione) indica dove si trova il documento che stai leggendo.

| Icona | Posizione |
|---|---|
| Il logo di GitHub | Il documento viene letto da GitHub e non è salvato su questo dispositivo |
| Un computer | Una cartella di questo dispositivo gestita da Lunascape. Compaiono anche il nome del ramo Git e il numero di file modificati |
| Una cartella | Una cartella di questo dispositivo |

Premi l'icona per vedere la posizione, lo stato e le operazioni disponibili da lì, ad esempio [Visualizza su GitHub] e [Copia il link].

## Clonare un repository in Lunascape

In Lunascape puoi clonare un repository GitHub su questo dispositivo, quindi modificarlo ed eseguire commit con Git.

- Nella schermata «Apri i documenti», premi [Duplica] nella riga del repository.
- Se stai leggendo un repository aperto da GitHub, premi il chip della posizione e poi [Duplica su questo computer]. Al termine della clonazione, lo stesso documento si apre dalla copia su questo dispositivo.

Nell'elenco, un repository clonato è contrassegnato con «Su questo computer» e [Apri su questo computer] compare per primo.

## Aprire tramite URL

L'indirizzo riporta il repository e la posizione del documento nello stesso ordine in cui compaiono nel repository. Il percorso è la posizione all'interno del repository, quindi l'ordine è lo stesso dell'URL di GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Cosa specificare | Come scriverlo |
|---|---|
| Solo il repository (ramo predefinito) | `/github/owner/repo` |
| Un documento all'interno del repository | `/github/owner/repo/docs/01-product/vision.md` |
| Un ramo o un tag | Aggiungi `?ref=v1.2.0` alla fine |

L'indirizzo cambia quando passi da una pagina all'altra. Premi [Condividi questo documento] nella barra degli strumenti per inviare il link alla pagina che stai leggendo. Puoi usare anche i pulsanti [Indietro] e [Avanti] del browser.

Gli indirizzi nella vecchia forma `?source=` si aprono ancora. Dopo l'apertura, l'indirizzo viene riscritto nella nuova forma.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Se non hai effettuato l'accesso, si applica il limite di utilizzo dell'API di GitHub (60 richieste all'ora). Per i repository con molti documenti o se li consulti spesso, usa [Accedi con GitHub].
> - I nomi di ramo che contengono `/` (ad esempio `feature/xxx`) si possono indicare con `?ref=` nella forma dell'indirizzo descritta sopra. La forma `?source=` non permette di scriverli.
> - I documenti vengono caricati con i permessi GitHub di chi li legge. Chi non ha il permesso di lettura non li vede.

## Aprire i documenti da una cartella locale

Premi [Apri i documenti] nella barra degli strumenti, poi premi [Apri i documenti da una cartella locale] nella colonna di sinistra e scegli una cartella del dispositivo. I file vengono elaborati all'interno del browser e non vengono mai inviati all'esterno. Questa funzione è disponibile nei browser che supportano la selezione delle cartelle (Chrome, Edge e altri).

## Argomenti correlati

- [Consultare un repository privato](private-repository.md)
- [Impossibile aprire la versione Web o accedere](../07-troubleshooting/web.md)
