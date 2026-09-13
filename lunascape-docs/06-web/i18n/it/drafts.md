# Salvare le bozze

Quando modifichi un documento nel visualizzatore Web, le modifiche non vengono scritte nel repository, ma salvate nel browser come «bozza».

## Creare una bozza

1. Apri un documento e premi [Modifica] in basso a destra.
2. Modifica il testo e premi [Salva].
   Compare «Salvato come bozza» e la modifica viene memorizzata nel browser.

- I documenti con una bozza hanno un contrassegno nell'INDEX. Sopra il testo compare «Questo documento è una bozza salvata sul dispositivo (non pubblicata)».
- [Bozze] nella barra degli strumenti mostra il numero di bozze; premendolo si apre l'elenco delle bozze.

## Eliminare una bozza

- Per eliminare la bozza di un singolo documento, premi [Elimina la bozza] sopra il testo.
- Per eliminarle tutte, usa l'elenco delle bozze.

## Applicare le bozze al repository

La «richiesta di pubblicazione», che invia le bozze come pull request, è implementata ma non è attiva nel visualizzatore pubblico. Per modificare il repository, lavora con l'estensione per VS Code o su un clone locale.

> **Nota**
>
> - Le bozze sono salvate nel browser (IndexedDB). Non vengono trasferite a un altro browser o a un altro dispositivo e, se cancelli i dati del sito nel browser, spariscono.
> - Se il documento nel repository viene aggiornato dopo che hai creato la bozza, compare «Il documento di origine è stato aggiornato». Controlla il contenuto e decidi se eliminare la bozza o mantenerla.
> - Se apri una cartella locale da [Apri i documenti] e la modifichi, le modifiche vengono salvate direttamente nel file, se il browser lo supporta. Con i browser che non lo supportano, restano solo per la sessione corrente.

## Argomenti correlati

- [Che cosa puoi fare nel visualizzatore Web](README.md)
- [Modificare un documento](../03-editing/README.md)
