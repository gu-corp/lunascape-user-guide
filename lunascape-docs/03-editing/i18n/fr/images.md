# Ajuster la taille des images

Les images insérées dans un document s'adaptent automatiquement à la largeur du texte et à la hauteur de l'écran. Pour une image que vous voulez afficher à une taille précise, vous pouvez définir sa largeur.

## Fonctionnement de l'ajustement automatique

- Une image Markdown ordinaire (`![description](./images/screen.png)`) est réduite pour tenir dans la largeur du texte. Elle n'est jamais agrandie au-delà de sa taille d'origine.
- Une capture d'écran en hauteur est limitée à 72 % de la hauteur de l'écran ou à 720 px, selon la plus petite des deux valeurs.

## Définir la largeur dans l'éditeur

1. Appuyez sur [Modifier] et sélectionnez l'image dans l'affichage visuel.
2. Choisissez une largeur dans [Taille de l'image] de la barre d'outils.
3. Appuyez sur [Enregistrer].

| Option | Largeur |
|---|---|
| [Automatique] | Non définie (ajustement automatique) |
| [Petite (360 px)] | 360 px |
| [Moyenne (560 px)] | 560 px |
| [Grande (760 px)] | 760 px |
| [Largeur du texte (920 px)] | 920 px |
| [Personnalisée…] | Un entier quelconque de 16 à 4096 px |

## Définir la largeur en Markdown

Donnez à la balise HTML `img` un `width` numérique. Cette forme s'affiche aussi comme une image sur GitHub et dans MDX.

```html
<img src="./images/screen.png" alt="Écran des paramètres" width="360" />
```

> **Remarque**
>
> - `width` n'accepte qu'un nombre, sans `px` ni `%`. Une valeur supérieure à la largeur du texte reste tout de même limitée à la largeur du texte à l'affichage.
> - Les chemins des images sont relatifs au document. Les images situées en dehors de la racine documentaire ne sont pas affichées.

## Voir aussi

- [Modifier un document](README.md)
- [Les schémas, formules ou images ne s'affichent pas](../07-troubleshooting/rendering.md)
