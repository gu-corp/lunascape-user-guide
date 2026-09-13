# Lire dans une autre langue

Lorsqu'un document possède des traductions, vous pouvez changer de langue depuis le menu des langues (globe) de la barre d'outils.

## Changer de langue

1. Appuyez sur le menu des langues de la barre d'outils.
   La langue de la page affichée s'affiche, ainsi que la façon dont elle a été déterminée (chemin de la traduction, détection automatique, langue par défaut du projet).
2. Choisissez la langue dans laquelle vous voulez lire.
   La traduction du même document s'ouvre. La langue choisie est mémorisée : le prochain document que vous ouvrirez s'affichera dans cette langue s'il en existe une traduction.

La liste des langues indique si le document possède une traduction dans chacune d'elles.

| Mention | Signification |
|---|---|
| Traduit | Une traduction existe et peut être ouverte |
| Non traduit | La langue est prise en charge par le projet, mais ce document n'a pas encore de traduction |
| À mettre à jour | Une traduction existe, mais le document d'origine a été modifié depuis |

> **Remarque**
>
> - Choisir une langue ne fait qu'ouvrir une traduction existante. Cela ne génère aucune traduction et ne crée aucun fichier. Pour créer une traduction, utilisez [Créer et gérer les traductions…] dans le même menu.
> - Lorsque la langue de la page affichée est considérée comme différente de la langue par défaut du projet, un avertissement s'affiche. La configuration n'est jamais modifiée.

## La langue affichée en premier

À l'ouverture d'un document, la première langue d'affichage est déterminée dans cet ordre.

1. La langue que vous avez choisie précédemment dans cette racine de documentation. Votre choix est enregistré (choisir la langue par défaut est également enregistré comme un choix).
2. La langue d'affichage de VS Code (dans la version navigateur Web, les paramètres de langue du navigateur). La langue prise en charge correspondante est sélectionnée automatiquement. Une langue régionale (comme `en-US`) correspond aussi à sa langue de base (`en`).
3. La langue de repli du projet (`fallbackLocale` dans `lunascape-docs.json`).
4. La langue par défaut du projet.

> **Conseil**
>
> - En cas de sélection automatique, la mention « sélection automatique » apparaît à côté de la langue actuelle dans le menu des langues. Placez le pointeur sur ce badge pour en connaître la raison.
> - `fallbackLocale` est la langue présentée aux lecteurs dont la langue d'environnement ne correspond à aucune des langues prises en charge. Dans un projet dont le document de référence est en japonais et qui possède une version anglaise, définir `"en"` ouvre la version anglaise pour un lecteur dont l'environnement est en espagnol, par exemple. Sans valeur définie, la langue par défaut est utilisée.

## Où sont rangées les traductions

Les documents dans la langue par défaut restent à leur emplacement ; les traductions sont placées dans **`i18n/<langue>/` du même dossier**, sous le même nom de fichier.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Remarque**
>
> - Reconstruire l'arborescence des dossiers sous `i18n/` (`i18n/en/guide/setup.md`) n'est pas reconnu. Le dossier `i18n/` se place toujours dans le même dossier que le document qu'il traduit.
> - Cet emplacement unique est le seul à partir duquel une traduction est résolue. Placer la traduction du même document dans le `i18n/` d'un dossier parent ne crée aucun conflit de priorité : cette copie devient simplement un fichier orphelin, absent du menu des langues comme du registre (et jamais supprimé automatiquement). Ne placez pas la même traduction à deux endroits.

## Lire dans la version navigateur Web

La version navigateur Web permet de changer de langue de la même manière lorsqu'une traduction existe. Pour lire dans une langue sans traduction, vous pouvez utiliser la fonction de traduction de page du navigateur. Le code, les formules et les figures sont exclus de la traduction.

## Voir aussi

- [Confier un travail à une IA](../05-ai/README.md)
- [Travaux disponibles](../05-ai/tasks.md)
- [Modifier les paramètres d'affichage](../02-reading/display-settings.md)
