# Leggere in un'altra lingua

Quando un documento ha delle traduzioni, puoi cambiare lingua dal menu delle lingue (globo) nella barra degli strumenti.

## Cambiare lingua

1. Premi il menu delle lingue nella barra degli strumenti.
   Vengono mostrate la lingua della pagina visualizzata e il motivo della scelta (percorso della traduzione, rilevamento automatico, lingua predefinita del progetto).
2. Scegli la lingua in cui vuoi leggere.
   Si apre la traduzione dello stesso documento. La lingua scelta viene memorizzata e anche il documento che aprirai successivamente verrà mostrato in quella lingua, se ne esiste una traduzione.

L'elenco delle lingue indica se il documento ha una traduzione in ciascuna di esse.

| Indicazione | Significato |
|---|---|
| Tradotto | Esiste una traduzione e può essere aperta |
| Non tradotto | La lingua è supportata dal progetto, ma questo documento non ha ancora una traduzione |
| Da aggiornare | La traduzione esiste, ma il documento di origine è cambiato dopo la traduzione |

> **Nota**
>
> - Scegliere una lingua apre soltanto una traduzione già esistente: non genera traduzioni e non crea file. Per creare una traduzione, usa [Crea e gestisci traduzioni…] nello stesso menu.
> - Quando la lingua della pagina visualizzata risulta diversa dalla lingua predefinita del progetto, viene mostrato un avviso. La configurazione non viene mai modificata.

## La lingua con cui si apre un documento

Quando apri un documento, la prima lingua di visualizzazione viene decisa in quest'ordine.

1. La lingua che hai scelto in precedenza in questa radice della documentazione. La scelta viene salvata (anche la scelta della lingua predefinita viene salvata come tale).
2. La lingua dell'interfaccia di VS Code (nella versione per browser Web, le impostazioni di lingua del browser). Viene selezionata automaticamente la lingua supportata corrispondente; una lingua con indicazione regionale (come `en-US`) corrisponde anche alla lingua di base (`en`).
3. La lingua di ripiego del progetto (`fallbackLocale` in `lunascape-docs.json`).
4. La lingua predefinita del progetto.

> **Suggerimento**
>
> - Quando la lingua è stata selezionata automaticamente, accanto alla lingua corrente nel menu delle lingue compare l'indicazione «selezione automatica». Passa il puntatore sull'etichetta per vederne il motivo.
> - `fallbackLocale` è la lingua mostrata ai lettori il cui ambiente non corrisponde a nessuna delle lingue supportate. In un progetto il cui documento canonico è in giapponese e che dispone di una versione inglese, impostando `"en"` i lettori con un ambiente in spagnolo, ad esempio, vedranno la versione inglese. Se non è impostata, viene usata la lingua predefinita.

## Dove si trovano le traduzioni

I documenti nella lingua predefinita restano dove sono; la traduzione va nella cartella **`i18n/<lingua>/` accanto al documento**, con lo stesso nome di file.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Nota**
>
> - Ricostruire la struttura delle cartelle sotto `i18n/` (`i18n/en/guide/setup.md`) non viene riconosciuto. La cartella `i18n/` va sempre collocata accanto al documento che traduce.
> - Quell'unica posizione è l'unico punto da cui viene risolta una traduzione. Mettere la traduzione dello stesso documento anche nella cartella `i18n/` di una cartella superiore non crea alcun conflitto di precedenza: quella copia diventa semplicemente un file isolato che non compare né nel menu delle lingue né nel registro (e non viene eliminato automaticamente). Non mettere la stessa traduzione in due posti.

## Se leggi nella versione per browser Web

Anche nella versione per browser Web puoi cambiare lingua allo stesso modo, se esiste una traduzione. Per leggere in una lingua che non ha traduzione, puoi usare la funzione di traduzione della pagina del browser. Il codice, le formule e i diagrammi sono esclusi dalla traduzione.

## Argomenti correlati

- [Affidare un lavoro a un'AI](../05-ai/README.md)
- [Lavori che puoi affidare](../05-ai/tasks.md)
- [Modificare le impostazioni di visualizzazione](../02-reading/display-settings.md)
