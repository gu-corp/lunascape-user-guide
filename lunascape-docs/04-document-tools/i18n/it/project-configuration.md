# Configurazione del progetto

Il file `lunascape-docs.json` posto direttamente sotto la radice della documentazione contiene le impostazioni della radice condivise dal team. È gestito con Git.

## Creare o modificare il file di configurazione

- Premi [Strumenti documento] nella barra degli strumenti → scheda [Controllo] → [Origine delle regole e impostazioni del documento] → [Modifica le impostazioni del documento] per aprire il file in VS Code. Se il file non esiste, in quel momento viene creato un file iniziale.
- Al nome di file `lunascape-docs.json` viene associato automaticamente il JSON Schema incluso, che fornisce il completamento automatico e la descrizione di ogni voce. Non è necessaria la voce `$schema`.

## Esempio di configurazione

```json
{
  "id": "product-docs",
  "title": "Documentazione del prodotto",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Descrizione delle voci

| Voce | Contenuto | Predefinito |
|---|---|---|
| `id` | La chiave con cui vengono salvate le impostazioni di visualizzazione di ciascun utente. Assegna un ID fisso quando vuoi conservare le impostazioni anche spostando la cartella | Il percorso della cartella |
| `title` | Il nome mostrato all'estrema sinistra della barra degli strumenti e nell'elenco delle radici della documentazione. Non cambia al cambiare della lingua dell'interfaccia | Il titolo del README/index della radice, altrimenti il nome della cartella |
| `indexTitle` | Il titolo dell'INDEX | `INDEX` |
| `startPage` | Il documento aperto per primo (percorso relativo alla radice della documentazione) | `README.md` |
| `appearance` | La combinazione di colori: `light` (sempre chiaro) o `auto` (segue il tema di VS Code) | `light` |
| `defaultLocale` | La lingua predefinita (la lingua del documento canonico). Si indica con un tag di lingua BCP 47 (`ja`, `en`, `zh-Hant` e simili). È l'origine delle traduzioni | Non impostato (dedotto dal testo e mostrato) |
| `fallbackLocale` | La lingua mostrata per prima ai lettori la cui lingua dell'ambiente non corrisponde ad alcuna delle lingue supportate. Indica una lingua contenuta in `locales` | Non impostato (si usa `defaultLocale`) |
| `locales` | L'elenco delle lingue supportate. Include `defaultLocale`. Diventano le voci del menu delle lingue e le destinazioni delle traduzioni | Solo `defaultLocale` |
| `ignoredDirectories` | I nomi delle cartelle escluse dall'INDEX, dalla ricerca e dai controlli. Se specificato, sostituisce il valore predefinito | `["99-archive"]` |
| `tree` | I valori predefiniti per la visualizzazione dell'INDEX. L'utente può sovrascriverli dalle impostazioni di visualizzazione | Come nell'esempio sopra |
| `editor.defaultMode` | La visualizzazione di modifica usata finché l'utente non la cambia: `visual` o `source` | `visual` |
| `editor.showEditButton` | Se mostrare [Modifica] in basso a destra nel documento | `true` |
| `documentStandards.pack` | Lo Standard Pack usato per il controllo dei documenti e i modelli: `builtin:<nome>` oppure un percorso relativo alla radice della documentazione | Nessuno |
| `documentStandards.profile` | Il nome del profilo definito dal Pack | Nessuno |
| `translation.enabled` | Abilita la creazione delle proposte di traduzione e la traduzione in blocco | `true` |
| `translation.contextFiles` | I file Markdown del documento canonico (percorso relativo alla radice della documentazione) passati durante la traduzione come riferimento per la terminologia e lo stile | `[]` |
| `translation.maxContextCharacters` | Il limite massimo del numero totale di caratteri dei documenti di riferimento (massimo 1048576) | `49152` |
| `description` | Una descrizione di una riga dell'insieme di documenti. Viene mostrata nella scheda della home del repository. Come `title`, si può scrivere come stringa o come oggetto per lingua | Nessuno |

## Indicare dove si trovano i documenti nel repository

Il file `lunascape-docs.json` posto direttamente sotto il repository può contenere non le impostazioni di quella cartella, ma una **mappa del repository**. Scrivendo una qualsiasi delle 3 voci seguenti diventa una mappa, e quella cartella stessa non è più una radice della documentazione.

| Voce | Contenuto | Predefinito |
|---|---|---|
| `defaultFolder` | In quale cartella si trovano i documenti (percorso relativo a questa cartella). La cartella indicata non richiede un proprio file di configurazione | Nessuno (si usa `docs`) |
| `roots` | L'elenco degli insiemi di documenti, quando ce ne sono più di uno (percorsi relativi a questa cartella, nell'ordine di visualizzazione). In questo caso, questa cartella diventa la home | Nessuno |
| `excludes` | Le cartelle da escludere dalla ricerca delle radici della documentazione (percorsi relativi a questa cartella). Si aggiungono alle esclusioni predefinite come `node_modules` | `[]` |
| `home.cards` | Se mostrare le schede degli insiemi di documenti sotto il README della home. Imposta `false` quando scrivi tu stesso i collegamenti nel README | `true` |

La radice della documentazione viene determinata in questo ordine. Si usa la prima trovata, procedendo dall'alto.

1. La cartella indicata da un'impostazione o da un comando
2. Ciò a cui puntano `defaultFolder` o `roots` nel `lunascape-docs.json` posto direttamente sotto il repository
3. La cartella che contiene un `lunascape-docs.json` (se sotto un genitore comune ce ne sono due o più, quel genitore diventa la home)
4. La cartella `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. La radice stessa del repository

> **Suggerimento**
>
> Se non scrivi nulla, entra in gioco il punto 4, quindi un normale repository con un solo `docs/` funziona come prima. Scrivi `defaultFolder` solo quando vuoi che la cartella si chiami `manual`.

### Esempio di mappa

```json
{
  "title": "Guida di Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Ordine di priorità delle impostazioni

Le voci relative alla visualizzazione hanno la priorità in questo ordine.

1. Le impostazioni di visualizzazione dell'utente (pannello [Impostazioni di visualizzazione])
2. Le impostazioni di VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. I valori predefiniti del prodotto

Solo le lingue (`defaultLocale`, `fallbackLocale`, `locales`) fanno eccezione: il `lunascape-docs.json` è la fonte autorevole. Non è possibile sovrascrivere le lingue del progetto con le impostazioni personali di VS Code.

> **Nota**
>
> Uno Standard Pack può essere indicato come `standard` anche in `docs-lint.config.json`. Quando è presente in entrambi, ha la priorità `docs-lint.config.json`.

## Argomenti correlati

- [Modificare le regole di controllo](rules.md)
- [Modificare le impostazioni di visualizzazione](../02-reading/display-settings.md)
- [Elenco delle impostazioni di VS Code](../08-reference/settings.md)
