# Impostazioni di VS Code

Cercare «Lunascape Docs» nelle impostazioni di VS Code (`⌘,` / `Ctrl+,`) per modificare le voci seguenti. Sono tutte impostazioni personali e non vengono mai salvate nei documenti del progetto.

## Radice della documentazione

| Impostazione | Valori | Predefinito | Funzione |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` sceglie automaticamente la radice della documentazione più vicina al file Markdown aperto e, se il file non appartiene ad alcuna radice, apre temporaneamente la cartella superiore. `fixed` apre sempre la radice indicata in `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Matrice di stringhe | `["docs"]` | Nomi di cartella rilevati come radici della documentazione in modalità `auto`. Una cartella che contiene `lunascape-docs.json` viene rilevata indipendentemente dal nome. Se il file `lunascape-docs.json` nella directory principale del repository contiene `defaultFolder` o `roots`, hanno la precedenza |
| `lunascapeDocEditor.root` | Percorso | `docs` | Radice della documentazione relativa all'area di lavoro, usata in modalità `fixed` o all'apertura tramite comando |
| `lunascapeDocEditor.startPage` | Percorso | `README.md` | Pagina iniziale relativa alla radice della documentazione |
| `lunascapeDocEditor.title` | Stringa | `Lunascape Docs` | Sostituisce il titolo della scheda del documento. Non influisce sul nome mostrato nel selettore della radice della documentazione |
| `lunascapeDocEditor.ignoredDirectories` | Matrice di stringhe | `["99-archive"]` | Nomi di cartella esclusi dall'INDEX |

## Visualizzazione

| Impostazione | Valori | Predefinito | Funzione |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` usa uno sfondo bianco, `auto` segue i colori di VS Code |
| `lunascapeDocEditor.locale` | Tag di lingua | Nessuno | Lingua del documento personale, usata in via preferenziale quando è disponibile. Non modifica la lingua canonica del progetto |
| `lunascapeDocEditor.documentMetadata.compact` | Valore booleano | `true` | Riduce la tabella di gestione del documento posta dopo l'H1 a una riga «Informazioni sul documento» |
| `lunascapeDocEditor.tree.showFileNames` | Valore booleano | `false` | Mostra nell'INDEX i nomi dei file al posto dei titoli dei documenti |
| `lunascapeDocEditor.tree.showDocumentIcons` | Valore booleano | `false` | Mostra le icone dei documenti nell'INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Valore booleano | `false` | Mostra le icone delle cartelle nell'INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Valore booleano | `false` | Mostra nell'INDEX il numero di elementi contenuti direttamente in ogni cartella |
| `lunascapeDocEditor.tree.showGuides` | Valore booleano | `true` | Mostra nell'INDEX le linee guida dei livelli |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Spaziatura delle righe dell'INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Valore booleano | `true` | Chiude l'INDEX la prima volta, quando è presente un solo documento |

## Modifica

| Impostazione | Valori | Predefinito | Funzione |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Vista di modifica usata finché non si cambia. La vista usata per ultima ha la precedenza |
| `lunascapeDocEditor.editor.showEditButton` | Valore booleano | `true` | Mostra [Modifica] in basso a destra nel documento |

## Diagrammi

| Impostazione | Valori | Predefinito | Funzione |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Runtime di disegno per TikZ. `bundled` usa il runtime approvato incluso (non presente nella versione distribuita attuale), `workspace` usa `node-tikzjax` 1.0.5 nella directory principale di un'area di lavoro attendibile (solo per sviluppo e valutazione), `disabled` non disegna nulla |

## Impostazioni deprecate

| Impostazione | Da usare al suo posto |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` in `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` in `lunascape-docs.json` |

Le impostazioni personali non possono sostituire le lingue del progetto.

## Argomenti correlati

- [Modificare le impostazioni di visualizzazione](../02-reading/display-settings.md)
- [Configurazione del progetto](../04-document-tools/project-configuration.md)
