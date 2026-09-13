# Aprire un repository di GitHub

Nella versione Web i documenti si aprono indicando un repository di GitHub. Per i repository pubblici non è necessario accedere.

## Aprire dalla schermata

1. Apri <https://docs.lunascape.org/>.
2. Premi [Apri i documenti] (l'icona della cartella) nella barra degli strumenti.
3. Inserisci il repository in [Indica un repository] e premi [Apri].
   Quando hai effettuato l'accesso a GitHub, puoi anche sceglierlo da un elenco in [Scegli tra i repository leggibili].

> **Suggerimento**
>
> - L'icona di GitHub accanto apre su github.com il documento che stai leggendo. Non serve ad aprire i documenti.

## Aprire con un URL

L'indirizzo riporta il repository e la posizione del documento nell'ordine in cui compaiono: poiché il percorso è la posizione all'interno del repository, la sequenza è la stessa dell'URL di GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Cosa indicare | Forma |
|---|---|
| Solo il repository (ramo predefinito) | `/github/owner/repo` |
| Un documento all'interno del repository | `/github/owner/repo/docs/01-product/vision.md` |
| Un ramo o un tag | aggiungi `?ref=v1.2.0` alla fine |

Quando cambi pagina, cambia anche l'indirizzo. Premi [Condividi questo documento] nella barra degli strumenti per passare a qualcuno il collegamento alla pagina che stai leggendo. Funzionano anche i pulsanti [Indietro] e [Avanti] del browser.

Anche la vecchia forma con `?source=` si apre come prima. Una volta aperta, viene riscritta nella nuova forma.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Senza aver effettuato l'accesso vale il limite d'uso dell'API di GitHub (60 richieste all'ora). Per repository con molti documenti o per consultazioni ripetute, usa [Accedi con GitHub].
> - I nomi di ramo che contengono `/` (come `feature/xxx`) si possono indicare con `?ref=` nella forma di indirizzo sopra. Nella forma con `?source=` non è possibile scriverli.
> - I documenti vengono caricati con i permessi GitHub di chi legge. Chi non ha il permesso di lettura non li vede.

## Aprire i documenti di una cartella locale

Premi [Apri i documenti] nella barra degli strumenti e, sotto l'elenco, scegli [Apri i documenti da una cartella locale], quindi seleziona una cartella sul tuo dispositivo. I file vengono elaborati all'interno del browser e non vengono inviati all'esterno. Questa funzione è disponibile nei browser che supportano la selezione di cartelle (Chrome, Edge e altri).

## Argomenti correlati

- [Consultare un repository privato](private-repository.md)
- [La versione Web non si apre o non consente l'accesso](../07-troubleshooting/web.md)
