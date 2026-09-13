# Lavori che si possono affidare

Si scelgono da [Lavoro] nella scheda [AI]. Per ogni lavoro cambiano le istruzioni trasmesse e il controllo successivo.

| Lavoro | Contenuto | Requisiti | Tipo di API |
|---|---|---|---|
| Traduci questa pagina | Traduce il documento visualizzato nella lingua scelta | Il documento di destinazione aperto, la lingua di destinazione | ○ |
| Traduci tutto ciò che manca | Traduce in ordine i documenti con traduzione mancante e da aggiornare della lingua scelta | La lingua di destinazione | Solo con sessione |
| Correggi questa pagina | Verifica e corregge la terminologia, lo stile e la struttura dei capitoli richiesta dallo standard dei documenti | Il documento di destinazione aperto | ○ |
| Crea un nuovo documento | Crea un nuovo documento seguendo lo standard dei documenti e i modelli | L'argomento (facoltativo) | Solo con sessione |

## Che cosa contengono le istruzioni

| N. | Contenuto |
|---|---|
| 1 | La posizione della radice della documentazione, con l'indicazione di non modificare nulla al di fuori di essa |
| 2 | La lingua predefinita (documento canonico) e la collocazione delle traduzioni (la cartella `i18n/<lingua>/` accanto al documento) |
| 3 | Che `navigation.order` appartiene solo al documento canonico e che una traduzione può sovrascrivere soltanto `navigation.title` |
| 4 | Che non si devono modificare gli ID dei requisiti, i collegamenti, il codice, Mermaid, TeX e la struttura del front matter |
| 5 | Lo standard dei documenti e il glossario (`terminology` in `docs-lint.config.json`) |
| 6 | Di eseguire al termine il controllo dei documenti, di segnalare i file modificati e di non eseguire operazioni Git |

> **Suggerimento**
>
> I documenti di «Traduci tutto ciò che manca» vengono ricavati dal registro, fino a 200 documenti per esecuzione. Se sono di più, ripetere l'operazione.

## Argomenti correlati

- [Affidare un lavoro all'AI](README.md)
- [Il registro e le sue voci](ledger.md)
