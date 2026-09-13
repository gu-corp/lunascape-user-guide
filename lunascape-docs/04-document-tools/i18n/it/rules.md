# Modificare le regole di controllo

È possibile cambiare il livello di notifica di ogni controllo (errore, avviso, informazione) oppure disattivarlo. Le modifiche vengono salvate nel file `docs-lint.config.json` della radice della documentazione e condivise con il team.

## Modificare un livello di notifica

1. Nella barra degli strumenti premere [Strumenti documento] e aprire la scheda [Controllo].
2. Premere [Rivedi e modifica le regole].
   L'elenco dei controlli si espande all'interno della stessa scheda. Per ogni voce vengono indicati lo scopo e l'origine dell'impostazione attuale (Project, Profile, Pack o Default).
3. Scegliere il livello di notifica della voce da modificare.
4. Premere [Salva e ricontrolla].
   L'impostazione viene salvata e l'intera radice della documentazione viene controllata di nuovo con la nuova configurazione.

| Opzione | Significato |
|---|---|
| [Impostazione standard (…)] | Rimuove la personalizzazione e ripristina l'impostazione standard determinata dal profilo, dallo Standard Pack e dal valore predefinito, in quest'ordine |
| [Non usare] | Non esegue questo controllo |
| [Informazione] / [Avviso] / [Errore] | Segnala con questo livello di notifica |

> **Nota**
>
> - Per salvare è necessaria un'area di lavoro attendibile.
> - Viene salvato soltanto il livello di notifica di ogni voce. Le opzioni delle singole voci restano invariate. Lo Standard Pack e il profilo non si modificano da questa schermata.
> - Se il file `docs-lint.config.json` è stato modificato dall'esterno subito prima del salvataggio, il salvataggio viene annullato. Caricare lo stato più recente e riprovare.
> - Se il file `docs-lint.config.json` non esiste, viene creato al momento del salvataggio.

## Modificare direttamente i file di configurazione

- Premendo [Apri le impostazioni complete] si apre `docs-lint.config.json` in VS Code.
- Aprire [Origine delle regole e impostazioni del documento] e premere [Modifica le impostazioni del documento] per aprire `lunascape-docs.json` in VS Code. Lo Standard Pack e il profilo si scelgono qui.

Per entrambi i file sono attivi il completamento automatico e le descrizioni forniti dagli schemi JSON inclusi nell'estensione.

## Standard Pack e profili

Uno Standard Pack è uno standard di documentazione che riunisce i tipi di documento richiesti, la struttura dei capitoli, la terminologia e i modelli. Si sceglie con `documentStandards` in `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Il Pack incluso `builtin:gu-corp-software` offre i profili `base`, `web-application`, `api-service`, `regulated-financial-product` e `smart-contract`.

## Argomenti correlati

- [Controllare i documenti](check.md)
- [Impostazioni del progetto](project-configuration.md)
