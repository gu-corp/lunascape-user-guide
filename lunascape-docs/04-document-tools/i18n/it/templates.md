# Creare un documento da un modello

Nella scheda [Crea] degli Strumenti documento puoi scegliere un modello, visualizzarne l'anteprima e creare un nuovo documento.

1. Premi [Strumenti documento] nella barra degli strumenti e apri la scheda [Crea].
2. Premi [Crea da un modello] e scegli un modello.
3. Compila i campi di immissione (titolo, riepilogo e così via). I campi obbligatori sono contrassegnati con «Obbligatorio».
4. Inserisci la destinazione come percorso relativo alla radice della documentazione (ad esempio `03-design/api.md`).
5. Premi [Anteprima] e controlla il Markdown generato.
6. Premi [Crea con questo contenuto].
   Il documento viene creato e mostrato nel visualizzatore. Subito dopo viene eseguito il controllo dell'intera radice della documentazione.

## Modelli disponibili

| Modello | Contenuto |
|---|---|
| Documento di una pagina | Crea in un unico file una breve specifica, degli appunti o un documento esplicativo autonomo |
| Specifica, manuale, guida | Crea un unico file con una struttura di capitoli generica, adatta a una specifica, a un manuale o a una guida |
| Modelli di Standard Pack | Se in `lunascape-docs.json` è selezionato Standard Pack, si aggiungono i tipi di documento previsti da quel profilo (documento dei requisiti, documento di progettazione e così via) |

> **Nota**
>
> - Per creare un documento è necessaria un'area di lavoro attendibile.
> - I file esistenti non vengono mai sovrascritti. Se nella destinazione esiste già un documento con lo stesso nome, la creazione non riesce.
> - La destinazione richiede l'estensione `.md` o `.mdx`. Non è possibile creare documenti sotto `i18n` (dove si trovano le traduzioni).
> - Dopo aver modificato i dati inseriti, premi di nuovo [Anteprima] prima di creare il documento.

> **Suggerimento**
>
> In un progetto che non ha ancora una cartella dei documenti, puoi creare il primo gruppo di documenti con «Lunascape Docs: Crea documenti da un modello» nella palette dei comandi. Consulta [Creare i primi documenti](../01-introduction/first-documents.md).

## Argomenti correlati

- [Usare gli Strumenti documento](README.md)
- [Modificare le regole di controllo](rules.md)
