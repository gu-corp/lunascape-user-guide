# Spécifications principales

## Environnement requis

| Environnement | Configuration requise |
|---|---|
| Extension VS Code | VS Code 1.90 ou version ultérieure. Les fonctions qui écrivent des fichiers exigent un espace de travail approuvé |
| Version navigateur web | Chrome, Edge, Safari ou Firefox récents. La consultation d'un dossier local requiert un navigateur prenant en charge la sélection de dossier (File System Access API) |
| Extension Chromium | Manifest V3. Aucune autorisation d'hôte n'est demandée |

## Documents pris en charge

| Élément | Contenu |
|---|---|
| Fichiers | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tableaux, listes de tâches, blocs de code, texte barré), images locales, front matter YAML |
| MDX | Seuls les composants autorisés sont affichés. Aucun script arbitraire n'est exécuté |
| HTML | Affiché après nettoyage par DOMPurify 3.4.14 |

## Figures et formules

| Type | Nom de langage | Remarques |
|---|---|---|
| Formules | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Données intégrées uniquement. URL externes et marques d'image impossibles |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | JSON strict uniquement |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Source affichée repliée dans la version distribuée. Limites : 64 Kio en entrée, 15 secondes, SVG de 2 Mio |
| Penrose (expérimental) | `penrose` | Préréglage `set-theory` uniquement |

## Valeurs limites

| Élément | Valeur |
|---|---|
| Résultat du développement d'un modèle | 4 Mio |
| Contexte de référence de la traduction | 49 152 caractères par défaut, 1 048 576 caractères au maximum |
| Documents par exécution de traduction groupée | 1 000 documents |
| Largeur d'image personnalisée | 16 à 4096 px |

## Fichiers

| Fichier | Rôle | Suivi par Git |
|---|---|---|
| `lunascape-docs.json` | Configuration de la racine de documentation | Oui |
| `docs-lint.config.json` | Configuration des règles de vérification | Oui |
| `.lunascape-docs/translation-freshness.json` | Enregistrement de la fraîcheur des traductions (chemins, langues, empreintes et horodatages uniquement) | Oui |
| Paramètres VS Code et état de l'espace de travail | Paramètres d'affichage personnels, choix du fournisseur, état d'ouverture de l'INDEX | Non |

## Standard Pack inclus

`builtin:gu-corp-software` — profils : `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Rubriques associées

- [Liste des paramètres VS Code](settings.md)
- [Sécurité et limites d'enregistrement](security.md)
