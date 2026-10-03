# Qu'est-ce que Lunascape Docs ?

Lunascape Docs permet d'utiliser tels quels les documents Markdown d'un dépôt Git comme un « site de spécifications ». Aucune compilation préalable, aucun serveur de documentation et aucune base de données dédiée ne sont nécessaires.

## Ce que vous pouvez faire

| Objectif | Fonctions principales |
|---|---|
| Lire | INDEX (table des matières), liens dans le texte, fil d'Ariane, Précédent/Suivant, table des matières de la page, recherche filtrée |
| Afficher | Tableaux, blocs de code, ajustement automatique des images, formules KaTeX, schémas Mermaid, Vega-Lite, Markmap, WaveDrom et Svgbob, affichage replié des tableaux de gestion documentaire |
| Écrire | Basculer entre l'édition visuelle et l'édition du source Markdown ; créer, dupliquer, renommer et réordonner depuis l'INDEX |
| Vérifier | Vérification des documents avec docs-lint, contrôle des documents, sections et termes obligatoires selon un Standard Pack, création à partir de modèles |
| Traduire | Génération de propositions de traduction page par page ou en lot, à relire avant l'enregistrement <!-- ai-only --> |
| Utiliser depuis une IA | Outil de spécification en lecture seule que les agents de VS Code peuvent consulter <!-- ai-only --> |

## Environnements disponibles

| Environnement | Usage |
|---|---|
| Extension VS Code | Consultation, modification, vérification et traduction d'un dépôt présent sur votre ordinateur. C'est le sujet principal de cette aide |
| Version web | Consultation des documents sur GitHub (publics ou privés), brouillons conservés sur l'appareil, consultation d'un dossier local |
| Extension Chromium | Ouvre la version web dans un onglet du navigateur |

## Principes de base

- **Le Markdown est la version de référence.** Les documents restent des fichiers Markdown gérés par Git. Lunascape Docs ne les convertit jamais dans un autre format pour les conserver.
- **C'est vous qui enregistrez.** Les modifications ne sont écrites dans le fichier que lorsque vous appuyez sur [Enregistrer]. Les opérations Git d'indexation et de commit ne sont jamais effectuées automatiquement.
- **Les documents sont traités sur votre appareil.** Aucun document n'est envoyé à l'extérieur pour être consulté ou modifié. Seule la traduction envoie des données : la destination et le contenu sont affichés au préalable, et l'envoi n'a lieu qu'après votre approbation.
- **Les traductions se trouvent dans `i18n/<langue>/`.** Les documents dans la langue par défaut restent à leur emplacement ; les traductions sont placées sous le même chemin relatif, dans `i18n/en/` et ainsi de suite.
- **L'IA se limite à proposer.** Les propositions de traduction ne sont enregistrées qu'après vérification des différences. Les documents ne sont jamais réécrits à votre insu. <!-- ai-only -->

## Voir aussi

- [Nom et rôle des éléments de l'écran](screen.md)
- [Installer l'extension](install.md)
- [Opérations de base](../02-reading/README.md)
