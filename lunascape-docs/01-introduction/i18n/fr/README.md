# Qu'est-ce que Lunascape Docs

Lunascape Docs permet d'utiliser les documents Markdown placés dans un dépôt Git tels quels, comme un « site de spécifications ». Aucune étape de génération, aucun serveur de documentation ni base de données dédiée ne sont nécessaires.

## Ce que vous pouvez faire

| Objectif | Fonctions principales |
|---|---|
| Lire | INDEX (table des matières), liens dans le texte, fil d'Ariane, Précédent/Suivant, sommaire de la page, recherche par filtrage |
| Afficher | Tableaux, blocs de code, ajustement automatique des images, formules KaTeX, figures Mermaid, Vega-Lite, Markmap, WaveDrom et Svgbob, affichage replié des tableaux de gestion documentaire |
| Écrire | Basculer entre l'édition visuelle et l'édition de la source Markdown ; créer, dupliquer, renommer et réordonner depuis l'INDEX |
| Vérifier | Vérification des documents par docs-lint, contrôle des documents, chapitres et termes obligatoires selon le Standard Pack, création à partir de modèles |
| Traduire | Génération de propositions de traduction page par page ou en lot. Enregistrement après vérification <!-- ai-only --> |
| Utiliser depuis une IA | Un outil de spécification en lecture seule, consultable par les agents de VS Code <!-- ai-only --> |

## Environnements disponibles

| Environnement | Usage |
|---|---|
| Extension VS Code | Consultation, édition, vérification et traduction du dépôt local. C'est le cœur de cette aide |
| Version navigateur Web | Consultation des documents sur GitHub (publics ou privés), brouillons conservés sur l'appareil, consultation d'un dossier local |
| Extension Chromium | Ouvre la version navigateur Web dans un onglet du navigateur |
| Navigateur Lunascape | Intégrera le même modèle de document |

## Principes de base

- **Le Markdown est le document de référence.** Les documents restent les fichiers Markdown gérés par Git. Lunascape Docs ne les convertit jamais dans un autre format pour les conserver.
- **C'est vous qui enregistrez.** Les modifications ne sont écrites dans le fichier que lorsque vous appuyez sur [Enregistrer]. L'indexation et la validation Git ne sont jamais automatiques.
- **Les documents sont traités sur votre appareil.** Aucun document n'est envoyé à l'extérieur pour être lu ou modifié. Seule la traduction procède à un envoi, après affichage préalable du destinataire et du contenu, et uniquement après votre approbation.
- **Les traductions se placent dans `i18n/<langue>/`.** Les documents dans la langue par défaut restent à leur emplacement ; les traductions reprennent le même chemin relatif sous `i18n/en/`, par exemple.
- **L'IA se limite à proposer.** Les propositions de traduction sont enregistrées après vérification des différences. Aucun document n'est réécrit en silence. <!-- ai-only -->

## Voir aussi

- [Nom et rôle des différentes parties de l'écran](screen.md)
- [Installer l'extension](install.md)
- [Opérations de base](../02-reading/README.md)
