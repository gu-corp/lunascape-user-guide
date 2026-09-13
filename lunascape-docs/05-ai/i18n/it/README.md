# Affidare il lavoro a un'AI

Lunascape Docs non richiama alcun modello linguistico. Prepara **contesto, strumenti e verifiche** e lascia all'AI che già usi il compito di tradurre, rivedere e scrivere.

## L'idea

| Ciò che il prodotto fornisce | Contenuto |
|---|---|
| Contesto | Le convenzioni della documentazione (dove risiedono le traduzioni, il front matter, lo standard dei documenti, il glossario) e la posizione del documento di destinazione |
| Strumenti di lavoro | Il registro delle traduzioni mancanti e da aggiornare, la lettura e la scrittura dei documenti, la creazione da modelli |
| Verifiche successive | Il controllo con docs-lint, la differenza di copertura e di aggiornamento |

L'istruzione non contiene il testo del documento: l'AI legge i file, li scrive e li verifica da sé.

## Affidare un lavoro

1. Premi [Strumenti documento] nella barra degli strumenti e apri la scheda [AI].
2. In [Lavoro] scegli il lavoro da affidare.
3. Compila le voci necessarie (lingua di destinazione, argomento).
4. Premi [Affida questo lavoro].
   Si apre un terminale di VS Code e l'AI scelta riceve l'istruzione e inizia a lavorare.

> **Suggerimento**
>
> Una sessione di Claude Code porta con sé gli strumenti di lavoro (il server MCP `lunascape-docs`): può ottenere da sé l'elenco delle traduzioni mancanti e da aggiornare, eseguire docs-lint e registrare l'aggiornamento dopo la traduzione.

## Controllare il risultato

| Tipo di provider | Dove arriva il risultato |
|---|---|
| A sessione (Claude Code, Codex) | Scrive direttamente nell'albero di lavoro. **Controlla il risultato nella differenza di Git** |
| Ad API (modelli linguistici di VS Code, Anthropic, compatibili con OpenAI) | Restituisce una proposta per volta. Controllala con [Apri differenza] e scrivila con [Salva] |

### Controllare una proposta di tipo API

Con un provider ad API la proposta arriva nella scheda [AI].

1. Premi [Apri differenza] e confrontala con il contenuto attuale.
2. Se va bene, premi [Salva]: nel caso di una traduzione viene registrato anche l'aggiornamento. Per rinunciare, premi [Scarta].
   Per fermare la generazione a metà, premi [Interrompi].

> **Nota**
>
> - Lunascape Docs non esegue mai operazioni di stage o di commit in Git. Controlla sempre le modifiche nella differenza.
> - Non è possibile affidare un lavoro in un'area di lavoro non attendibile, né mentre si esplora una cartella esterna a qualsiasi radice della documentazione.

## Argomenti correlati

- [Lavori disponibili](tasks.md)
- [Impostazioni AI](settings.md)
- [Il registro e le sue voci](ledger.md)
