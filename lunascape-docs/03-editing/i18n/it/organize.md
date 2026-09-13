# Creare e organizzare documenti e cartelle

Dal menu degli elementi dell'INDEX puoi creare, duplicare, rinominare ed eliminare documenti e cartelle. L'immissione avviene in una piccola finestra di dialogo all'interno del visualizzatore, senza interrompere la lettura.

> **Nota**
>
> Queste operazioni sono disponibili solo se l'area di lavoro è attendibile in VS Code. Non possono essere eseguite mentre un documento è in modifica, mentre è in corso un'altra operazione o quando l'elemento ha modifiche non salvate.

## Creare un documento o una cartella

1. Apri il menu dell'elemento ([⋯] o clic con il pulsante destro) della cartella di destinazione.
   Per creare direttamente sotto la radice della documentazione, usa [⋯] all'estremità destra dell'intestazione dell'INDEX oppure fai clic con il pulsante destro su un punto vuoto dell'INDEX.
2. Scegli [Nuovo documento] o [Nuova cartella].
3. Inserisci un nome e premi [Crea].
   Il nome di un documento richiede un'estensione Markdown (`.md`, `.markdown`, `.mdx` e simili).

I nuovi documenti vengono creati come documenti nella lingua predefinita (documenti canonici).

## Duplicare un documento

1. Apri il menu dell'elemento del documento e scegli [Duplica].
2. Inserisci un nuovo nome e premi [Crea].

Viene duplicato solo il documento canonico; le sue traduzioni no.

## Modificare il titolo

Modifica l'intestazione del documento (H1). Il nome del file resta invariato.

1. Apri il menu dell'elemento di un documento o di una cartella e scegli [Rinomina il titolo].
2. Inserisci il nuovo titolo su una sola riga e premi [Modifica].

Per una cartella viene modificata l'intestazione del suo `README.md`. Se è visualizzata una traduzione, viene modificato il titolo del documento in quella lingua.

## Modificare il nome della documentazione

Modifica il nome della documentazione mostrato nella barra degli strumenti (il nome della radice della documentazione).

1. Fai clic con il pulsante destro sul nome della documentazione nella barra degli strumenti. Lo stesso menu si apre anche da [⋯] all'estremità destra dell'intestazione dell'INDEX.
2. Scegli [Rinomina il documento] e inserisci un nuovo nome.

Se non è stato configurato nulla, viene mostrato il nome della cartella così com'è.

Il nome modificato viene scritto **nel punto che attualmente fornisce il nome della documentazione**, così un'intestazione visibile non viene mai ignorata.

| Stato attuale | Destinazione della scrittura |
|---|---|
| `lunascape-docs.json` contiene un nome | Viene aggiornato `lunascape-docs.json` |
| Non c'è un nome, ma la radice della documentazione ha un README | Viene riscritta l'intestazione (H1) del README |
| Nessuno dei due | Viene creato `lunascape-docs.json` e il nome vi viene salvato |

Il messaggio mostrato dopo la modifica indica dove è stata effettuata la scrittura.

> **Suggerimento**
>
> Il nome della documentazione viene determinato in quest'ordine: il nome in `lunascape-docs.json`, poi l'intestazione del README della radice della documentazione, infine il nome della cartella.

## Modificare il nome di un file o di una cartella

1. Apri il menu dell'elemento e scegli [Rinomina file] o [Rinomina cartella].
2. Inserisci il nuovo nome e premi [Modifica].

Vengono rinominate anche le traduzioni corrispondenti (lo stesso percorso sotto `i18n/<lingua>/`).

## Eliminare

1. Apri il menu dell'elemento e scegli [Sposta nel cestino].
2. Controlla il messaggio di conferma e approva lo spostamento.

L'elemento viene spostato nel cestino del sistema operativo, quindi può essere ripristinato se necessario. Le traduzioni non vengono eliminate e restano al loro posto.

## Nomi che non si possono usare

- Nomi che iniziano con `.` (non comparirebbero nell'INDEX)
- `i18n` (riservato ai file di traduzione)
- Nomi riservati da Windows (`CON`, `PRN` e simili)
- Nomi che terminano con un punto o uno spazio
- Nomi con caratteri di controllo o caratteri non ammessi nei nomi di file
- Nomi già presenti nella stessa cartella (compresi i nomi che differiscono solo per maiuscole e minuscole)

> **Nota**
>
> La pagina iniziale (di norma il `README.md` nella radice) non può essere rinominata né spostata. Modifica prima `startPage` in `lunascape-docs.json`.

## Argomenti correlati

- [Modificare l'ordine dei documenti](reorder.md)
- [Usare l'INDEX](../02-reading/index-panel.md)
