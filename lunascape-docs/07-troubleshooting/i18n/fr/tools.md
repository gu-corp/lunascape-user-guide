# La vérification, la création ou la traduction ne fonctionne pas

## Vérification

### Le message « docs-lint n'est pas disponible » s'affiche

- L'environnement d'exécution de docs-lint n'est pas inclus dans l'extension, ou la configuration présente un problème. Réinstallez l'extension.
- « Pour charger le Pack local et la configuration en toute sécurité, approuvez cet espace de travail dans VS Code » : un espace de travail approuvé est nécessaire pour utiliser un Standard Pack local.

### Le résultat reste sur « Revalidation nécessaire »

Lorsque vous modifiez un document ou un paramètre, le résultat précédent devient caduc. Appuyez de nouveau sur [Vérifier la racine documentaire]. Les modifications non enregistrées ne sont pas prises en compte.

### Appuyer sur un signalement n'ouvre rien

Les éléments « Toute la racine de documentation » ne sont liés à aucun document précis : ils n'ont donc pas de position. Vérifiez le document concerné en suivant le contenu du signalement.

### Impossible d'enregistrer les règles

- Un espace de travail approuvé est nécessaire.
- « La configuration de lint a été modifiée par une autre opération » : `docs-lint.config.json` a été modifié depuis l'extérieur. Chargez l'état le plus récent, puis recommencez.
- Les liens symboliques et les fichiers de configuration situés hors de la racine de documentation ne peuvent pas être modifiés.

## Création à partir d'un modèle

- « L'aperçu du modèle a expiré » / « Les informations saisies ont changé » : appuyez de nouveau sur [Aperçu], puis créez le document.
- « Un document existe déjà à cet emplacement » : les fichiers existants ne sont jamais écrasés. Indiquez un autre emplacement d'enregistrement.
- L'emplacement d'enregistrement doit être un chemin relatif à la racine de documentation, avec l'extension `.md` ou `.mdx`. Aucune création n'est possible sous `i18n`.
- « Approuvez l'espace de travail pour créer des documents » : approuvez l'espace de travail dans VS Code.

<!-- ai-only:start -->
## Traduction

### Les boutons de traduction sont inactifs

- « La traduction par IA n'est pas activée pour cette racine de documentation » : définissez `translation.enabled` sur `true` dans `lunascape-docs.json`.
- « La langue par défaut du projet n'est pas définie » : enregistrez la langue par défaut dans [Modifier les paramètres d'affichage](../02-reading/display-settings.md).
- « Ajoutez la langue cible aux langues prises en charge » : ajoutez la langue de destination à `locales`.
- « Aucun document de référence à traduire » : vous avez ouvert une page traduite. Basculez vers la page en langue par défaut.
- La traduction groupée n'est pas disponible dans un affichage de dossier temporaire. Placez un fichier `lunascape-docs.json` dans ce dossier pour en faire une racine de documentation.

### La proposition de traduction est refusée ou doit être régénérée

- « Le document de référence a changé. Régénérez la proposition de traduction » : le document de référence ou la langue cible a changé après la création de la proposition. Traduisez de nouveau.
- Si la réponse du modèle de langue omet des identifiants ou du code à préserver, elle n'est pas acceptée. Le contenu de la réponse est consultable dans le panneau de sortie « Lunascape Docs Traduction ».
- « La traduction groupée est limitée à 1000 documents par exécution » : répartissez la portée par dossier ou par sélection explicite.
<!-- ai-only:end -->

## Rubriques connexes

- [Vérifier un document](../04-document-tools/check.md)
- [Créer un document à partir d'un modèle](../04-document-tools/templates.md)
- [Confier un travail à une IA](../05-ai/README.md)
