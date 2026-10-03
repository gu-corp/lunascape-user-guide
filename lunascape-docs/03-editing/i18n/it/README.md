# Modificare un documento

I documenti si possono modificare direttamente nel visualizzatore. La schermata di modifica offre una «visualizzazione visiva», dove si modifica ciò che si vede, e una «visualizzazione del sorgente Markdown»; un unico pulsante alterna le due.

## Iniziare la modifica

Premere una delle opzioni seguenti. Aprono tutte la stessa schermata di modifica.

- [Modifica] in basso a destra nel documento
- [⋯] in alto a destra nel documento (Altre azioni) → [Modifica]
- Menu della voce nell'INDEX → [Modifica]

## Modificare

1. Modificare il testo direttamente.
   Nella barra degli strumenti in alto nella schermata di modifica sono disponibili il formato del paragrafo (corpo, titoli da 1 a 4, citazione, codice), [Grassetto], [Corsivo], [Elenco puntato], [Elenco numerato], [Collegamento], [Inserisci una tabella], [Dimensione immagine], [Annulla] e [Ripristina].
2. Per modificare direttamente il sorgente Markdown, premere [Markdown].
   Premerlo di nuovo per tornare alla visualizzazione visiva. L'ultima visualizzazione usata viene memorizzata e ripristinata alla successiva pressione di [Modifica].
3. Premere [Salva] (si può salvare anche con Ctrl+S / ⌘S).
   Il contenuto viene scritto nel file Markdown e si torna alla visualizzazione di lettura. Per interrompere la modifica e tornare all'ultimo contenuto salvato, premere [Annulla modifiche].

## Iniziare sempre dalla schermata di modifica (modalità di modifica)

Premendo [Modalità di modifica] nella barra degli strumenti per attivarla, ogni volta che si apre un documento si parte dalla schermata di modifica. Utile quando si scrive in continuazione, come su un blocco note.

- Mentre è attiva, premere [Salva] non chiude la schermata di modifica. [Annulla modifiche] riporta all'ultimo contenuto salvato lasciando aperta la schermata di modifica.
- Premendola di nuovo si disattiva e si torna alla visualizzazione di lettura. Lo stato attivo/disattivo viene memorizzato per ciascun utente.
- Non viene mostrata per una radice della documentazione su cui non è possibile scrivere (ad esempio una sorgente GitHub di sola lettura).

## Modifiche non salvate

Le modifiche non salvate vengono conservate automaticamente su questo dispositivo. Non si perdono passando a un altro documento né chiudendo la scheda o la finestra.

- [Non salvato] nella schermata di modifica indica che c'è una differenza rispetto all'ultimo contenuto salvato.
- Alla successiva apertura dello stesso documento, si riprende dalle modifiche conservate e viene segnalato. Se nel frattempo il documento originale è stato aggiornato, viene segnalato anche questo. Con [Annulla modifiche] si può tornare al contenuto più recente.
- Le modifiche conservate scompaiono con [Salva] o [Annulla modifiche]. Poiché non sono state salvate, non compaiono in Git né tra le bozze.

> **Nota**
>
> - Il salvataggio scrive soltanto il file. Lo staging e il commit in Git non avvengono mai automaticamente.
> - Le formule e i diagrammi come Mermaid, TikZ e Vega-Lite vengono mostrati con il risultato del rendering nella visualizzazione visiva. Per modificarne il contenuto, passare a [Markdown].
> - I documenti che contengono sintassi specifica di MDX (componenti, `import` e simili) si modificano solo nella visualizzazione Markdown, per preservarne la sintassi.
> - Il front matter (le impostazioni racchiuse tra le righe `---` all'inizio) viene conservato anche modificando nella visualizzazione visiva.

> **Suggerimento**
>
> - Premendo [Apri in VS Code] si apre il file nel normale editor di testo. Salvando nell'editor di testo, anche la visualizzazione nel visualizzatore si aggiorna automaticamente.
> - Per non mostrare il pulsante [Modifica], disattivare [Pulsante di modifica] in [Impostazioni di visualizzazione]. Per nasconderlo nell'intero progetto, impostare `editor.showEditButton` su `false` in `lunascape-docs.json`.
> - La visualizzazione iniziale predefinita (visiva o Markdown) si può cambiare con l'impostazione `lunascapeDocEditor.editor.defaultMode` oppure con `editor.defaultMode` in `lunascape-docs.json`.

## Argomenti correlati

- [Creare e organizzare documenti e cartelle](organize.md)
- [Regolare le dimensioni delle immagini](images.md)
- [Scrivere formule](math.md)
- [Scrivere diagrammi e grafici](diagrams.md)
