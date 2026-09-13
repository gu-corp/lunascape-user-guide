# Utilizzo da parte di agenti AI

L'estensione registra in VS Code il Language Model Tool di sola lettura `lunascape_getDocsSpecification`. Quando a un agente compatibile di VS Code vengono poste domande sulle funzionalità, sulla configurazione o sulle convenzioni dei documenti di Lunascape Docs, tramite questo strumento può recuperare il contenuto di questa guida (la specifica generale).

## Come si usa

Nella chat di VS Code, poni la domanda aggiungendo `#lunascapeDocs`, oppure chiedi semplicemente informazioni sulla configurazione o sulla struttura dei documenti di Lunascape Docs.

```text
#lunascapeDocs Come si abilitano le traduzioni in inglese in lunascape-docs.json?
```

## Argomenti dello strumento

| Argomento | Contenuto |
|---|---|
| `topic` | La sezione da recuperare: `all`, `usage` (Operazioni di base), `structure` (Radici della documentazione e convenzioni dei file), `editing` (Modifica di un documento), `configuration` (Configurazione del progetto), `security` (Sicurezza e limiti di scrittura) o `ai` (Utilizzo da parte di agenti AI) |
| `locale` | La lingua della guida (un tag di una lingua della guida inclusa, come `ja` o `en`). Se omesso, viene usata la lingua dell'interfaccia di VS Code e, in mancanza di questa, viene restituita la guida in giapponese |

> **Nota**
>
> - Lo strumento non invia mai il contenuto dei documenti all'esterno.
> - Lo strumento non restituisce mai nomi dell'area di lavoro né percorsi locali.
> - Lo strumento non modifica i file.
> - Funziona dagli agenti compatibili di VS Code anche senza un file `AGENTS.md`. Non viene condiviso automaticamente con altri client AI che non usano l'API dello strumento dell'estensione.

## Argomenti correlati

- [Visualizzare la guida](../02-reading/help.md)
- [Sicurezza e limiti di scrittura](security.md)
