# Impostazioni AI

Scegli l'AI e il modello a cui affidare il lavoro. Questa schermata usa i propri menu a discesa, non la selezione rapida di VS Code.

1. Premi [Strumenti documento] → scheda [AI] → [Impostazioni AI…].
2. Scegli un provider in [Provider].
   I provider non utilizzabili in questo ambiente compaiono non selezionabili, con il motivo.
3. Scegli un modello in [Modello]. Le opzioni cambiano a seconda del provider.
4. Chiudi la schermata. La scelta viene salvata per ciascun utente e riutilizzata la volta successiva.

## Provider

| Provider | Tipo | Rilevamento |
|---|---|---|
| Claude Code | A sessione | Presenza del comando `claude` |
| Codex | A sessione | Presenza del comando `codex` |
| Modelli linguistici di VS Code | API | Modelli registrati nella VS Code Language Model API |
| Anthropic API | API | Registrazione di una chiave API |
| API compatibile con OpenAI | API | Registrazione di una chiave API e di un endpoint |

Un provider **a sessione** legge e scrive i file da sé ed esegue da sé il controllo del documento. I risultati vengono scritti direttamente nell'albero di lavoro e si verificano nelle differenze di Git.

Un provider **API** restituisce il Markdown di un documento e l'estensione mostra le differenze prima di salvare.

## Registrare una chiave API

Anthropic API e le API compatibili con OpenAI diventano utilizzabili una volta registrata una chiave API.

1. Scegli il provider in [Provider]. Compare il campo per la chiave API.
2. Inserisci la [Chiave API]. Per un'API compatibile con OpenAI, inserisci anche l'[Endpoint] (ad esempio `https://api.openai.com/v1`).
3. Premi [Salva]. Viene visualizzato «Chiave registrata».

> **Nota**
>
> - Le chiavi sono conservate nel SecretStorage di VS Code e non vengono più mostrate. Non vengono scritte né in `settings.json` né in alcun documento. Puoi eliminarle con [Elimina chiave].
> - Gli elenchi dei modelli vengono richiesti a ciascun servizio con la chiave registrata. Finché non si ottiene una risposta, viene mostrato un elenco noto.
> - Con un provider API si possono eseguire solo «Traduci questa pagina» e «Correggi questa pagina». Per scorrere più documenti e per creare documenti, usa un provider a sessione.

> **Suggerimento**
>
> Se non viene trovato alcun provider, installa Claude Code o Codex, oppure registra una chiave API. Riapri [Impostazioni AI…] e verrà rilevato.

## Argomenti correlati

- [Affidare il lavoro a un'AI](README.md)
- [Elenco delle impostazioni di VS Code](../08-reference/settings.md)
