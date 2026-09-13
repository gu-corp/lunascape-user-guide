# Afficher les informations du document

Un « tableau de gestion documentaire » placé en tête d'un document (identifiant du document, version, date de mise à jour, état, etc.) est regroupé, lors de la lecture, dans une ligne compacte « Informations du document ». Le Markdown lui-même reste un tableau ordinaire, il se lit donc tel quel sur GitHub.

## Conditions d'affichage

Placez un tableau à deux colonnes comme le suivant immédiatement après le titre (H1).

```markdown
# Exigences fonctionnelles

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Le tableau doit contenir une ligne « 文書ID » et plusieurs champs de gestion.
- Un tableau placé sous un titre `## 文書管理` ou `## Document information` est également reconnu.
- Les tableaux situés au milieu du texte et les tableaux ordinaires « intitulé/contenu » ne sont pas convertis.

## Affichage

- Lors de la lecture, seuls l'état et la date de mise à jour sont affichés en petits caractères.
- Appuyez sur la ligne pour afficher tous les champs.
- À l'impression, tous les champs sont affichés.
- Dans l'éditeur, le tableau s'affiche comme un tableau ordinaire et peut être modifié tel quel.

> **Astuce**
>
> Pour toujours afficher le tableau au lieu de le replier, désactivez [Replier les informations du document] dans [Paramètres d'affichage].

## Rubriques connexes

- [Modifier un document](README.md)
- [Modifier les paramètres d'affichage](../02-reading/display-settings.md)
