# Il registro e le sue registrazioni

Il registro nella parte superiore della scheda [AI] mostra lo stato della traduzione per ogni lingua supportata. Anche senza usare l'AI, permette di verificare che cosa manca.

| Indicazione | Significato |
|---|---|
| Traduzione mancante | Numero di documenti che non hanno ancora una versione tradotta |
| Da aggiornare | Numero di documenti la cui traduzione esiste, ma il cui documento canonico è più recente del momento registrato |
| Tradotto | Numero di traduzioni allineate al documento canonico |

Il registro viene calcolato percorrendo la radice della documentazione. Non interviene alcuna AI né alcun modello linguistico.

## Aggiornare le registrazioni delle traduzioni

Per determinare lo stato «da aggiornare» occorre aver registrato il documento canonico e la traduzione come erano al momento della traduzione. Un'AI di tipo sessione scrive i file direttamente, quindi la registrazione non viene creata automaticamente.

1. Quando la traduzione è terminata e ne hai verificato il contenuto, premi [Aggiorna le registrazioni delle traduzioni].
2. Le traduzioni prive di registrazione vengono registrate come corrispondenti al documento canonico attuale.

Le sessioni di Claude Code e i salvataggi dei fornitori di tipo API eseguono la registrazione automaticamente (alla sessione viene indicato di usare lo strumento MCP `record_translation_freshness`). Questo pulsante serve quando hai tradotto con Codex o con la chat di VS Code.

Da quel momento, se modifichi un documento canonico, la relativa traduzione viene mostrata come «da aggiornare».

> **Nota**
>
> - Le traduzioni che hanno già una registrazione non vengono sovrascritte, per non cancellare uno stato «da aggiornare» esistente.
> - Le registrazioni vengono salvate in `.lunascape-docs/translation-freshness.json`. Contengono soltanto percorsi relativi, lingue, hash del contenuto e data e ora, mai il testo del documento.

## Argomenti correlati

- [Il lavoro che puoi affidare](tasks.md)
- [Leggere in un'altra lingua](../02-reading/languages.md)
