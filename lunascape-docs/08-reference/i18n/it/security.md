# Sicurezza e limiti di salvataggio

I limiti che Lunascape Docs adotta per proteggere i documenti e il dispositivo.

## Visualizzazione

- L'HTML generato dal Markdown e l'SVG generato dai diagrammi vengono ripuliti con DOMPurify 3.4.14 prima della visualizzazione.
- Gli script arbitrari contenuti nell'MDX non vengono eseguiti.
- KaTeX viene eseguito con `trust: false`, `maxSize: 50` e `maxExpand: 1000`, e non considera attendibili né l'HTML esterno né i comandi arbitrari.
- Le librerie di disegno Markmap, WaveDrom, Svgbob, Vega-Lite e Penrose vengono caricate nel dispositivo, a versioni fissate, solo quando è presente il blocco corrispondente. Non sono consentiti riferimenti a risorse esterne, HTML grezzo e notazioni eseguibili; dall'SVG generato vengono rimossi script, immagini esterne, `link`, `style` e `foreignObject`.
- Il disegno TikZ non avvia il LaTeX del sistema: viene eseguito in sequenza in un worker TeX WebAssembly con un file system in memoria. Sono previsti limiti su input, coda, memoria, tempo di esecuzione (15 secondi) e output SVG, e le istruzioni di I/O su file vengono rifiutate.

## Accesso ai documenti e ai file

- I collegamenti dei documenti e le operazioni sui file non possono uscire dalla radice della documentazione.
- La creazione, la ridenominazione, lo spostamento e l'eliminazione dall'INDEX vengono applicati solo dopo che l'estensione ha verificato di nuovo la radice della documentazione, la versione dell'INDEX, il percorso del documento canonico, il tipo di destinazione, i limiti dei collegamenti simbolici e i documenti non salvati. Le richieste provenienti da un menu obsoleto o da un'altra radice della documentazione non vengono applicate.
- Durante la modifica di un documento o l'applicazione di un'altra operazione sull'INDEX, le operazioni di modifica dell'INDEX sono disattivate.
- La creazione da un modello verifica di nuovo, dopo l'anteprima, l'attendibilità dell'area di lavoro, l'identità della radice della documentazione, la versione dell'INDEX, lo Standard Pack e il contenuto generato, la destinazione di salvataggio e i limiti dei collegamenti simbolici. Non sovrascrive i file esistenti e non crea contenuti diversi dall'anteprima né risultati di espansione superiori a 4 MiB.
- Il salvataggio di un file di configurazione controlla la versione immediatamente prima del salvataggio e si interrompe se rileva una modifica esterna.

## Invio all'esterno

- I documenti non vengono inviati all'esterno per la consultazione, la modifica o il controllo. Il controllo dei documenti viene eseguito nel dispositivo in modo deterministico.
- Solo la traduzione (traduzione di questa pagina, traduzione in blocco) invia i documenti a un modello linguistico, dopo aver mostrato in anticipo la destinazione e l'ambito dell'invio e solo previa approvazione esplicita. <!-- ai-only -->
- Le proposte di traduzione vengono presentate come differenze e, dopo una nuova verifica delle versioni del documento canonico e della destinazione, vengono applicate solo se una persona le salva esplicitamente. <!-- ai-only -->
- Lo strumento di specifica destinato agli agenti AI non restituisce il testo dei documenti, i nomi delle aree di lavoro né i percorsi locali. <!-- ai-only -->

## Git

- Il salvataggio esegue soltanto la scrittura del file. Nessuna funzione esegue automaticamente lo staging o il commit in Git.
- I file esistenti come `_meta.json` non vengono mai eliminati o modificati in modo silenzioso. Anche le traduzioni orfane non vengono eliminate o spostate automaticamente.

## Argomenti correlati

- [Specifiche principali](README.md)
- [Utilizzo dall'AI](ai-agents.md)
