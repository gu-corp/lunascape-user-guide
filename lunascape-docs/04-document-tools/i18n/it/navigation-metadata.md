# Impostare i metadati di navigazione

Il nome e l'ordine mostrati nell'INDEX si scrivono nel front matter YAML di ciascun documento. I documenti vengono visualizzati anche senza di esso, usando l'intestazione (H1) e l'ordine dei nomi dei file.

## Nome e ordine del documento

Scrivi quanto segue all'inizio del documento.

```yaml
---
navigation:
  title: Introduzione
  order: 200
---
```

| Campo | Significato |
|---|---|
| `navigation.title` | Il nome mostrato nell'INDEX. Se omesso, viene usato l'H1 e, in mancanza di questo, il nome del file |
| `navigation.order` | Un numero intero che determina l'ordine, crescente. Se omesso, si applica un ordine predefinito stabile (per nome del file) |

> **Suggerimento**
>
> - Assegna i valori di `order` a intervalli di 100, come 100, 200, 300, così da poter inserire in seguito 150 tra di essi.
> - Valori di `order` mancanti, non validi o duplicati non nascondono mai un documento.
> - Riordinando nell'INDEX, `navigation.order` viene scritto automaticamente; non è necessario scriverlo a mano.

## Nome e ordine della cartella

Il nome e l'ordine di una cartella appartengono al front matter del suo `README.md` (o `index.md` se non c'è un README). La pagina di copertina non ha bisogno di contenuto nel corpo.

```yaml
---
navigation:
  title: Pianificazione del prodotto
  order: 100
---
```

Una cartella senza pagina di copertina usa il nome della cartella e l'ordine predefinito. Quando una modifica del titolo o un riordino nell'INDEX lo richiede, viene creato un `README.md` contenente solo il front matter. La semplice consultazione non crea mai un file.

## Gestione nelle traduzioni

- L'ordine e il ruolo di una cartella (pagina di copertina o solo configurazione) sono decisi unicamente dal documento nella lingua predefinita.
- Una traduzione può sovrascrivere solo `navigation.title`. Quando il documento canonico ha contenuto nel corpo, anche l'H1 della traduzione viene usato come nome.
- Una traduzione da sola non aggiunge mai una pagina.

## Ordinamento e comprimibilità degli elementi figli

`navigation.children.sort` e `navigation.children.defaultCollapsed` nella pagina di copertina di una cartella sono definiti per controllare come vengono ordinati i suoi elementi figli diretti e se questi partono compressi. La lettura e la modifica in VS Code sono previste in futuro.

## Argomenti correlati

- [Modificare l'ordine dei documenti](../03-editing/reorder.md)
- [Radici della documentazione e convenzioni sui file](structure.md)
