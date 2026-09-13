# Mostrare le informazioni del documento

Una «tabella di controllo del documento» posta all'inizio di un documento (ID documento, versione, data di aggiornamento, stato e simili) viene riunita, durante la lettura, in una piccola riga «Informazioni documento». Il Markdown in sé rimane una tabella normale, quindi si legge senza problemi anche su GitHub.

## Condizioni

Posiziona una tabella a due colonne come la seguente subito dopo il titolo (H1).

```markdown
# Definizione dei requisiti funzionali

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- La condizione è che siano presenti una riga «文書ID» e più campi di gestione.
- Viene riconosciuta anche una tabella posta sotto un titolo `## 文書管理` o `## Document information`.
- Le tabelle nel mezzo del testo e le comuni tabelle «voce/contenuto» non vengono convertite.

## Come viene mostrato

- Durante la lettura vengono mostrati in piccolo solo lo stato e la data di aggiornamento.
- Premendo la riga vengono mostrati tutti i campi.
- Durante la stampa vengono mostrati tutti i campi.
- Nella schermata di modifica la tabella appare come una tabella normale e può essere modificata come tale.

> **Suggerimento**
>
> Per mostrare sempre la tabella invece di comprimerla, disattiva [Comprimi i dettagli del documento] in [Impostazioni di visualizzazione].

## Argomenti correlati

- [Modificare un documento](README.md)
- [Modificare le impostazioni di visualizzazione](../02-reading/display-settings.md)
