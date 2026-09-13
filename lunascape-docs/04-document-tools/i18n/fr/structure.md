# Racines de documentation et conventions de fichiers

Les règles que suit Lunascape Docs pour trouver les documents et construire l'INDEX. Le système de fichiers est lui-même la source de vérité : aucun registre ni aucune configuration de build n'est nécessaire.

## Racine documentaire

- Le dossier `docs` le plus proche, ou un dossier contenant `lunascape-docs.json`, devient la racine documentaire.
- Avec un `lunascape-docs.json`, le dossier n'a pas besoin de s'appeler `docs`.
- Ouvrir un fichier Markdown situé hors de toute racine documentaire affiche son dossier comme racine documentaire temporaire.

## Fichiers affichés dans l'INDEX

- Les fichiers `.md`, `.markdown` et `.mdx` sont affichés. Les nouveaux fichiers apparaissent toujours, même sans front matter ni informations de navigation.
- Les dossiers commençant par `.`, `node_modules` et les dossiers indiqués dans `ignoredDirectories` (par défaut `99-archive`) ne sont pas affichés.
- Tout ce qui se trouve sous `i18n/` est traité comme des traductions et n'est pas listé séparément dans l'INDEX.

## Pages de couverture des dossiers

- Un `README.md` (ou `index.md` s'il n'y a pas de README) contenant du corps de texte est la page de couverture de son dossier. Appuyer sur le nom du dossier dans l'INDEX l'ouvre.
- Un `README.md` composé uniquement de front matter, sans corps de texte, est un « descripteur de configuration uniquement » et n'est pas affiché comme page. Utilisez-le lorsqu'un dossier n'a besoin que d'un titre ou d'un ordre.
- Lorsque `README.md` et `index.md` existent tous les deux, `README.md` est prioritaire.

## Langue par défaut et traductions

- Les documents en langue par défaut (documents de référence) restent à leur place.
- Une traduction est placée dans un dossier `i18n/<langue>/` à côté du document, sous le même nom de fichier. Reconstruire l'arborescence de dossiers sous `i18n/` n'est pas reconnu.
- C'est le seul emplacement à partir duquel une traduction est résolue. Le même fichier placé ailleurs est un fichier orphelin qu'aucun document ne revendique comme sa traduction.

```text
docs/
  lunascape-docs.json
  README.md                  ← page de couverture de la racine (page de départ)
  i18n/en/README.md          ← sa traduction anglaise
  01-product/
    README.md                ← page de couverture du dossier
    requirements.md
    i18n/en/README.md        ← les traductions anglaises des deux documents ci-dessus
    i18n/en/requirements.md
  99-archive/                ← exclu de l'INDEX par défaut
```

## À propos de `_meta.json`

Le `_meta.json` de Nextra n'est pas utilisé pour la navigation. Les fichiers existants ne sont ni modifiés ni supprimés. À l'avenir, seule une fonction explicite d'import/export les prendra en charge.

## Voir aussi

- [Configurer les informations de navigation](navigation-metadata.md)
- [Configuration du projet](project-configuration.md)
- [Changer de racine documentaire](../02-reading/roots.md)
