# Non è possibile modificare, salvare o riordinare

## Il pulsante [Modifica] non è presente

- [Pulsante di modifica] in [Impostazioni di visualizzazione] è disattivato. Attivalo, oppure usa [⋯] → [Modifica] in alto a destra nel testo, o il menu della voce nell'INDEX → [Modifica].
- Lo stesso vale quando `editor.showEditButton` in `lunascape-docs.json` è `false`.
- Mentre è visualizzata la Guida non è possibile modificare. Chiudi la Guida.

## Non è possibile passare alla vista visuale

«この文書にはMDX構文があるため通常の編集画面へ切り替えられません» (Questo documento contiene sintassi MDX e non può essere aperto nell'editor visuale): i documenti che contengono sintassi propria di MDX (componenti, `import` e simili) si modificano solo nella vista Markdown, per preservare tale sintassi.

## Non è possibile modificare direttamente formule o diagrammi

La vista visuale mostra il risultato del rendering. Nella schermata di modifica premi [Markdown] e modifica il sorgente.

## Non è possibile riordinare o trascinare

- Il riordino non è disponibile durante un filtro, durante la modifica di un documento e mentre è in corso un'altra operazione sull'INDEX.
- Quando l'area di lavoro non è attendibile, le operazioni di creazione, organizzazione ed eliminazione non sono disponibili. Imposta l'area di lavoro come attendibile in VS Code.
- «INDEXが更新されています。もう一度ドラッグしてください» (L'INDEX è stato aggiornato; trascina di nuovo): è appena stata applicata un'altra modifica. Ripeti l'operazione.
- La pagina iniziale (il `README.md` della radice) non può essere spostata.

## Viene visualizzato «未保存の変更があります» (Sono presenti modifiche non salvate)

Il file interessato è aperto in modifica nell'editor di VS Code. Salva o annulla le modifiche, poi riprova.

## Non è possibile rinominare

I nomi seguenti non sono utilizzabili.

- Nomi che iniziano con `.`, `i18n` e i nomi riservati di Windows (`CON` e simili)
- Nomi che terminano con un punto o uno spazio e nomi che contengono caratteri di controllo o caratteri non consentiti nei nomi di file
- Nomi già presenti nella stessa cartella (compresi i nomi che differiscono solo per maiuscole e minuscole)
- Nomi di documento privi di un'estensione Markdown

## Ho salvato, ma in Git non compaiono modifiche o non vengono eseguiti commit

Lunascape Docs si limita a scrivere il file: non esegue lo staging né il commit in Git. Controlla nella vista Controllo del codice sorgente di VS Code ed esegui il commit se necessario.

## Argomenti correlati

- [Modificare un documento](../03-editing/README.md)
- [Creare e organizzare documenti e cartelle](../03-editing/organize.md)
- [Modificare l'ordine dei documenti](../03-editing/reorder.md)
