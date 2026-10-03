# Aprire un repository GitHub

Nella versione Web puoi aprire e leggere direttamente un repository GitHub, senza clonarlo. Per i repository pubblici non è necessario accedere.

## Aprire dalla schermata

1. Premi [Apri i documenti] (l'icona a forma di cartella) nella barra degli strumenti. Si apre la schermata «Apri i documenti».
2. Nella colonna a sinistra, scegli la posizione da aprire.

   | Posizione | Elementi elencati |
   |---|---|
   | Tutti | Tutti gli elementi seguenti. Quelli aperti di recente compaiono per primi |
   | Aperti di recente | I repository e le cartelle che hai aperto finora |
   | In evidenza | I manuali presentati dal sito |
   | Repository GitHub | Quando hai effettuato l'accesso con GitHub, i repository che puoi leggere |
   | Questo computer | Le cartelle di questo dispositivo |

3. Premi [Apri] sulla riga che vuoi aprire. Per restringere le righe, digita in [Filtra per nome del documento o del repository] in alto.

Per un repository che non compare nell'elenco, usa [Inserisci owner/repo e apri] nella colonna a sinistra.

> **Suggerimento**
>
> - I repository GitHub elencati sono quelli in cui è installata la GitHub App «Lunascape Docs» e per cui hai l'autorizzazione di lettura. Se un repository non compare, chiedi al suo proprietario di aggiungere l'App.

## Verificare dove si trova un documento

La piccola icona verso sinistra nella barra degli strumenti (il chip della posizione) indica dove si trova il documento che stai leggendo.

| Icona | Posizione |
|---|---|
| Il logo di GitHub | Stai leggendo da GitHub. Il documento non è salvato su questo dispositivo |
| Cartella | Una cartella di questo dispositivo |

Premi l'icona per visualizzare la posizione, lo stato e le operazioni disponibili da lì, come [Visualizza su GitHub] e [Copia il link].

## Aprire tramite URL

L'indirizzo riporta in sequenza il repository e la posizione del documento. Poiché il percorso indica la posizione all'interno del repository, l'ordine è lo stesso dell'URL di GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Cosa indicare | Forma |
|---|---|
| Solo il repository (ramo predefinito) | `/github/owner/repo` |
| Un documento nel repository | `/github/owner/repo/docs/01-product/vision.md` |
| Un ramo o un tag | Aggiungi `?ref=v1.2.0` alla fine |

Quando cambi pagina, cambia anche l'indirizzo. Premi [Condividi questo documento] nella barra degli strumenti per condividere il link della pagina che stai leggendo. Puoi usare anche [Indietro] e [Avanti] del browser.

Anche la forma precedente `?source=` si apre come prima. Dopo l'apertura, l'indirizzo viene riscritto nella nuova forma.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Senza accesso, si applica il limite di utilizzo dell'API di GitHub (60 richieste all'ora). Per i repository con molti documenti o per letture ripetute, usa [Accedi con GitHub].
> - I nomi di ramo che contengono `/` (come `feature/xxx`) possono essere indicati con `?ref=` nella forma di indirizzo descritta sopra. Non è possibile scriverli nella forma `?source=`.
> - I documenti vengono caricati con le autorizzazioni GitHub di chi legge. Chi non ha l'autorizzazione di lettura non li vede.

## Aprire i documenti da una cartella locale

Premi [Apri i documenti] nella barra degli strumenti, poi scegli una cartella del dispositivo da [Apri i documenti da una cartella locale] nella colonna a sinistra. I file vengono elaborati all'interno del browser e non vengono mai inviati all'esterno. Questa funzione è disponibile nei browser che supportano la selezione delle cartelle (Chrome, Edge e altri).

## Argomenti correlati

- [Consultare un repository privato](private-repository.md)
- [Impossibile aprire la versione Web o accedere](../07-troubleshooting/web.md)
