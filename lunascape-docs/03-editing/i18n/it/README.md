# Modificare un documento

I documenti si possono modificare direttamente nel visualizzatore. La schermata di modifica offre una vista visiva, in cui si modifica ciò che si vede, e una vista del sorgente Markdown; un unico pulsante passa dall'una all'altra.

## Iniziare la modifica

Premere una delle opzioni seguenti. Tutte aprono la stessa schermata di modifica.

- [Modifica] in basso a destra nel testo
- [⋯] (Altre azioni) in alto a destra nel testo → [Modifica]
- Menu della voce in INDEX → [Modifica]

## Modificare

1. Modificare il testo direttamente.
   Nella barra degli strumenti in alto nella schermata di modifica sono disponibili il formato di paragrafo (corpo del testo, titoli da 1 a 4, citazione, codice), [Grassetto], [Corsivo], [Elenco puntato], [Elenco numerato], [Collegamento], [Inserisci una tabella], [Dimensione immagine], [Annulla] e [Ripristina].
2. Per modificare direttamente il sorgente Markdown, premere [Markdown].
   Premerlo di nuovo per tornare alla vista visiva. L'ultima vista utilizzata viene memorizzata e ripristinata alla successiva pressione di [Modifica].
3. Premere [Salva].
   Il file Markdown viene scritto e si torna alla visualizzazione di lettura. Per interrompere, premere [Annulla].

> **Nota**
>
> - Il salvataggio scrive soltanto sul file. Lo staging e il commit su Git non avvengono automaticamente.
> - Le formule e i diagrammi come Mermaid, TikZ e Vega-Lite vengono mostrati già elaborati nella vista visiva. Per modificarne il contenuto, passare a [Markdown].
> - I documenti che contengono sintassi propria di MDX (componenti, `import` e simili) si modificano solo nella vista Markdown, per preservare tale sintassi.
> - Il front matter (le impostazioni racchiuse tra le righe `---` all'inizio) viene mantenuto anche modificando il documento nella vista visiva.

> **Suggerimento**
>
> - Premendo [Apri in VS Code] il file si apre nel normale editor di testo. Salvando lì, anche la visualizzazione nel visualizzatore si aggiorna automaticamente.
> - Per non mostrare il pulsante [Modifica], disattivare [Pulsante di modifica] in [Impostazioni di visualizzazione]. Per nasconderlo nell'intero progetto, impostare `editor.showEditButton` su `false` in `lunascape-docs.json`.
> - La vista iniziale predefinita (visiva o Markdown) si modifica con l'impostazione `lunascapeDocEditor.editor.defaultMode` oppure con `editor.defaultMode` in `lunascape-docs.json`.

## Argomenti correlati

- [Creare e organizzare documenti e cartelle](organize.md)
- [Regolare la dimensione delle immagini](images.md)
- [Scrivere formule](math.md)
- [Creare diagrammi e grafici](diagrams.md)
