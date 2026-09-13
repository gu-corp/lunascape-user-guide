# Modificare l'ordine dei documenti

L'ordine mostrato nell'INDEX può essere modificato con il trascinamento della selezione o da tastiera. L'ordine modificato viene salvato nel front matter del documento come `navigation.order`.

## Riordinare con il trascinamento della selezione

1. Trascinare un documento o una cartella nell'INDEX.
2. Rilasciarlo prima o dopo un elemento dello stesso livello, oppure su una cartella.
   All'interno dello stesso livello cambia l'ordine. Rilasciandolo su un'altra cartella, l'elemento viene spostato in quella cartella.

## Riordinare con la tastiera o dal menu

- Portare il fuoco su una voce dell'INDEX e premere `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Scegliere [Sposta su di una posizione] / [Sposta giù di una posizione] nel menu della voce.

## Che cosa viene salvato

- Riordinando all'interno dello stesso livello, viene aggiornato `navigation.order` nel front matter del documento canonico. Per una cartella, il valore viene scritto nel `README.md` della cartella; se la cartella non ne ha uno, viene creato un `README.md` con il solo front matter.
- Spostando un elemento in un'altra cartella, il documento canonico viene spostato insieme alle relative traduzioni. Prima dello spostamento viene richiesta una conferma, perché i collegamenti relativi possono esserne interessati.
- Non viene eseguita alcuna operazione di staging o commit su Git.

> **Nota**
>
> - Non è possibile riordinare durante un filtro, durante la modifica di un documento e in un'area di lavoro non attendibile.
> - Il messaggio «L'INDEX è stato aggiornato» indica che è appena stata applicata un'altra modifica. Ripetere l'operazione.
> - La pagina iniziale non può essere spostata in un'altra cartella.

> **Suggerimento**
>
> Assegnando a `navigation.order` valori a intervalli di 100, come 100, 200, 300, sarà più facile inserire in seguito altri documenti negli spazi intermedi. Per i dettagli, vedere [Impostare i metadati di navigazione](../04-document-tools/navigation-metadata.md).

## Argomenti correlati

- [Creare e organizzare documenti e cartelle](organize.md)
- [Impostare i metadati di navigazione](../04-document-tools/navigation-metadata.md)
