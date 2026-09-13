# Vérifier les documents

docs-lint permet de contrôler la structure des titres, les liens rompus, l'absence de documents ou de sections obligatoires, les variations de terminologie, la cohérence des identifiants d'exigence, etc. La vérification porte toujours sur l'ensemble de la racine de documentation.

## Lancer une vérification

1. Dans la barre d'outils, appuyez sur [Outils de document], puis ouvrez l'onglet [Vérification].
2. Appuyez sur [Vérifier la racine documentaire].
   Vous pouvez aussi lancer « Lunascape Docs: Vérifier la racine documentaire » depuis la palette de commandes.
3. Consultez la liste des résultats.

## Lire les résultats

- Au-dessus de la liste, [Ce document] / [Tout] permettent de changer l'étendue affichée. L'étendue de la vérification elle-même reste toujours la racine de documentation entière.
- Les signalements comportent quatre niveaux : « erreur », « avertissement », « information » et « suggestion ». Dans la barre d'outils, [Outils de document] affiche le nombre d'erreurs et d'avertissements.
- Appuyez sur un signalement pour ouvrir l'emplacement correspondant dans la source Markdown, dans l'éditeur de VS Code.
- Les signalements qui concernent l'ensemble de la racine de documentation (l'absence d'un document de test, par exemple) apparaissent sous l'entrée « Racine de documentation entière » et n'ont pas d'emplacement.
- Ces mêmes signalements apparaissent également dans le panneau « Problèmes » de VS Code.

## Éléments vérifiés

Appuyez sur [Consulter et modifier les règles] pour afficher la liste des vérifications actives et l'objectif de chacune. Les principales sont les suivantes.

| Élément | Contenu |
|---|---|
| Structure des titres | Il existe un seul H1 et les niveaux de titre ne sautent pas d'étape |
| Liens internes | Les documents ciblés existent et ne sortent pas de la racine de documentation |
| Langage des blocs de code | Les blocs de code indiquent un nom de langage |
| Dossiers et documents requis | Les dossiers et documents exigés par le profil du Standard Pack sont présents |
| Sections requises dans un document | Chaque type de document comporte les sections requises |
| Uniformité de la terminologie | Les expressions à éviter sont détectées et les termes recommandés proposés |
| Nommage et doublons des identifiants d'exigence | Les identifiants d'exigence respectent la règle de nommage et ne sont pas définis deux fois |
| Cohérence des références aux identifiants d'exigence | Les identifiants d'exigence cités par la conception, les tests ou les tableaux de suivi existent bien |
| Correspondance entre exigences et tests | Les identifiants d'exigence sont référencés depuis les documents de test |

Les éléments actifs dépendent du Standard Pack et du profil choisis dans `lunascape-docs.json`, ainsi que de `docs-lint.config.json`.

> **Remarque**
>
> - Dès que vous modifiez un document ou un réglage, le résultat précédent passe à « nouvelle vérification nécessaire ». Rien n'est validé automatiquement : appuyez de nouveau sur [Vérifier la racine documentaire].
> - Les modifications non enregistrées ne sont pas prises en compte par la vérification. Enregistrez-les au préalable.
> - La vérification s'exécute localement et de façon déterministe. Les évaluations réalisées par l'IA et les résultats de traduction ne se mêlent jamais aux résultats de la vérification.

## Voir aussi

- [Modifier les règles de vérification](rules.md)
- [Configuration du projet](project-configuration.md)
- [La vérification, la création ou la traduction ne fonctionne pas](../07-troubleshooting/tools.md)
