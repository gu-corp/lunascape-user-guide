# Modifier un document

Les documents se modifient directement dans le visualiseur. L'écran de modification propose un « affichage visuel », où vous modifiez ce que vous voyez, et un « affichage de la source Markdown » ; un seul bouton permet de passer de l'un à l'autre.

## Commencer la modification

Appuyez sur l'un des éléments suivants. Ils ouvrent tous le même écran de modification.

- [Modifier] en bas à droite du document
- [⋯] (Autres actions) en haut à droite du document → [Modifier]
- Menu d'un élément de l'INDEX → [Modifier]

## Modifier

1. Modifiez le texte directement.
   Dans la barre d'outils située en haut de l'écran de modification, vous disposez du format de paragraphe (corps de texte, titres 1 à 4, citation, code), de [Gras], [Italique], [Liste à puces], [Liste numérotée], [Lien], [Insérer un tableau], [Taille de l'image], [Annuler] et [Rétablir].
2. Pour modifier directement la source Markdown, appuyez sur [Markdown].
   Appuyez de nouveau dessus pour revenir à l'affichage visuel. Le dernier affichage utilisé est mémorisé et rétabli la prochaine fois que vous appuyez sur [Modifier].
3. Appuyez sur [Enregistrer] (vous pouvez aussi enregistrer avec Ctrl+S / ⌘S).
   Le fichier Markdown est écrit et l'affichage revient en mode lecture. Pour arrêter la modification et revenir au dernier contenu enregistré, appuyez sur [Abandonner les modifications].

## Toujours commencer par l'écran de modification (mode édition)

Appuyez sur [Mode édition] dans la barre d'outils pour l'activer : chaque document s'ouvrira alors sur l'écran de modification. Utilisez ce mode lorsque vous écrivez en continu, comme dans un bloc-notes.

- Tant qu'il est activé, appuyer sur [Enregistrer] ne ferme pas l'écran de modification. [Abandonner les modifications] revient au dernier contenu enregistré et laisse l'écran de modification ouvert.
- Appuyez de nouveau dessus pour le désactiver et revenir en mode lecture. L'activation ou la désactivation est mémorisée pour chaque utilisateur.
- Il ne s'affiche pas pour une racine documentaire dans laquelle il est impossible d'écrire (par exemple une source GitHub en lecture seule).

## Modifications non enregistrées

Les modifications que vous n'avez pas enregistrées sont conservées automatiquement sur cet appareil. Elles ne sont pas perdues lorsque vous passez à un autre document, ni lorsque vous fermez l'onglet ou la fenêtre.

- [Non enregistré] dans l'écran de modification indique que le contenu diffère du dernier contenu enregistré.
- La prochaine fois que vous ouvrez le même document, la modification reprend à partir du contenu conservé et vous en êtes averti. Si le document d'origine a été mis à jour depuis, vous en êtes également averti. [Abandonner les modifications] permet de revenir au contenu le plus récent.
- Les modifications conservées disparaissent avec [Enregistrer] ou [Abandonner les modifications]. Comme rien n'est enregistré, elles n'apparaissent pas dans Git ni parmi les brouillons.

> **Note**
>
> - L'enregistrement se contente d'écrire le fichier. La préparation (staging) et la validation (commit) Git ne sont jamais automatiques.
> - Les formules et les schémas tels que Mermaid, TikZ et Vega-Lite s'affichent sous leur forme rendue dans l'affichage visuel. Passez à [Markdown] pour en modifier le contenu.
> - Les documents contenant une syntaxe propre à MDX (composants, `import`, etc.) se modifient uniquement dans l'affichage Markdown, afin d'en préserver la syntaxe.
> - Le front matter (les paramètres encadrés par `---` en début de fichier) est préservé même lorsque vous le modifiez dans l'affichage visuel.

> **Astuce**
>
> - [Ouvrir dans VS Code] ouvre le fichier dans l'éditeur de texte habituel. Lorsque vous y enregistrez, l'affichage du visualiseur se met à jour automatiquement.
> - Pour masquer le bouton [Modifier], désactivez [Bouton de modification] dans les [Paramètres d'affichage]. Pour le masquer dans l'ensemble du projet, définissez `editor.showEditButton` sur `false` dans `lunascape-docs.json`.
> - L'affichage initial par défaut (visuel ou Markdown) se modifie via le paramètre `lunascapeDocEditor.editor.defaultMode` ou via `editor.defaultMode` dans `lunascape-docs.json`.

## Voir aussi

- [Créer et organiser des documents et des dossiers](organize.md)
- [Ajuster la taille des images](images.md)
- [Écrire des formules](math.md)
- [Créer des schémas et des graphiques](diagrams.md)
