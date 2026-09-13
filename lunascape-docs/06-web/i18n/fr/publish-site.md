# Publier vos documents sur le Web

Vous pouvez publier les documents de votre propre dépôt sous forme de site web, sur GitHub Pages ou sur n'importe quel hébergement statique. Il existe deux méthodes. Cette procédure s'adresse aux développeurs qui peuvent cloner le dépôt de Lunascape Docs et utiliser `npm`.

## Méthode 1 : placer les deux fichiers de la visionneuse

Cette méthode consiste à déployer uniquement la visionneuse (`index.html` et `lsdoc.js`) et à laisser les documents être chargés depuis GitHub. Les documents eux-mêmes ne font pas partie du site : la méthode est donc sûre pour un dépôt privé (les lecteurs se connectent avec GitHub).

1. Exécutez la commande suivante dans le dépôt de Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` et `lsdoc.js` sont générés dans `dist/viewer/`.
2. Placez les deux fichiers dans le dossier `docs/` du dépôt que vous voulez publier.
3. Activez GitHub Pages.

La racine de documentation à afficher est déterminée dans l'ordre suivant.

1. Le paramètre `source` dans `index.html`
2. La valeur `repository` indiquée dans le fichier `lunascape-docs.json` du même dossier
3. La déduction à partir de l'URL `*.github.io` et de l'organisation des branches

## Méthode 2 : exporter un site statique contenant les documents

Cette méthode consiste à exporter la visionneuse et les fichiers de documents ensemble, puis à héberger le résultat tel quel.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

La sortie contient l'ensemble de la visionneuse, les documents situés sous `docs/`, le fichier de liste `lunascape-docs-manifest.json` et `.nojekyll`. Placez le dossier de sortie sur S3 ou sur GitHub Pages pour le publier. Pour un exemple de publication automatique avec GitHub Actions, reportez-vous au fichier `examples/workflows/publish-docs-pages.yml` du dépôt.

> **Remarque**
>
> - **N'exportez pas les documents d'un dépôt privé vers GitHub Pages.** En dehors d'Enterprise Cloud, GitHub Pages est consultable par tout le monde. Si vous avez besoin d'une publication restreinte, utilisez la méthode 1 et faites connecter les lecteurs avec GitHub.
> - Ouvrir `index.html` directement en `file://` ne fonctionne pas, car le navigateur interdit le chargement des fichiers voisins et l'exécution des modules ES. Pour une vérification en local, utilisez la version VS Code ou un serveur HTTP.
> - Les bibliothèques de rendu pour TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob et Penrose sont chargées au moment de l'affichage. Sur un site exporté, déployez également le dossier `vendor/`.

## Voir aussi

- [Ce que permet la version Web](README.md)
- [Consulter un dépôt privé](private-repository.md)
