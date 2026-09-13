# Le registre et les enregistrements

Le registre situé en haut de l'onglet [AI] indique l'état de la traduction pour chaque langue prise en charge. Même sans utiliser l'IA, il vous permet de voir ce qui manque.

| Affichage | Signification |
|---|---|
| Non traduit | Nombre de documents qui n'ont pas encore de traduction |
| À mettre à jour | Nombre de documents dont la traduction existe, mais dont le document de référence est plus récent que l'enregistrement |
| Traduit | Nombre de traductions qui suivent leur document de référence |

Le registre est calculé en parcourant la racine de documentation. Aucune IA ni aucun modèle de langage n'intervient.

## Mettre à jour les enregistrements de traduction

Pour déterminer l'état « à mettre à jour », il faut avoir enregistré le document de référence et sa traduction tels qu'ils étaient au moment de la traduction. Les IA de type session écrivent directement dans les fichiers : l'enregistrement n'est donc pas créé automatiquement.

1. Une fois la traduction terminée et son contenu vérifié, appuyez sur [Mettre à jour les enregistrements de traduction].
2. Les traductions sans enregistrement sont enregistrées comme correspondant au document de référence actuel.

Les sessions Claude Code et l'enregistrement de type API créent l'enregistrement automatiquement (la session reçoit l'instruction d'utiliser l'outil MCP `record_translation_freshness`). Ce bouton est nécessaire lorsque vous avez traduit avec Codex ou avec la conversation de VS Code.

Ensuite, si vous modifiez le document de référence, sa traduction s'affiche comme « à mettre à jour ».

> **Remarque**
>
> - Les traductions qui possèdent déjà un enregistrement ne sont pas écrasées, afin de ne pas effacer un état « à mettre à jour » existant.
> - Les enregistrements sont conservés dans `.lunascape-docs/translation-freshness.json`. Seuls y figurent le chemin relatif, la langue, une empreinte du contenu et la date : jamais le texte du document.

## Voir aussi

- [Travaux à confier](tasks.md)
- [Lire dans une autre langue](../02-reading/languages.md)
