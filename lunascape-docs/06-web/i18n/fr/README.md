# Ce que permet la version Web

La version Web de Lunascape Docs est publiée à l'adresse <https://docs.lunascape.org/>. Sans rien installer, vous pouvez lire les documents hébergés sur GitHub comme un site Web.

## Fonctions

| Fonction | Description |
|---|---|
| Consultation des dépôts publics | Ouvre les documents d'un dépôt public GitHub sans connexion |
| Consultation des dépôts privés | Après connexion à GitHub, ouvre les dépôts sur lesquels vous avez un accès en lecture |
| Consultation d'un dossier local | [Ouvrir des documents], puis [Ouvrir les documents d'un dossier local], ouvre un dossier de votre appareil (navigateurs compatibles uniquement) |
| Fonctions de lecture | INDEX, liens, historique, filtrage, sommaire de la page, changement de langue et changement de thème. Identiques à la version VS Code |
| Figures et formules | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, formules KaTeX |
| Brouillons | Modifiez les documents et conservez les changements comme brouillons sur votre appareil. Rien n'est écrit dans le dépôt |
| Liens directs vers une page | Une URL peut désigner le dépôt et la page, ce qui permet d'ouvrir directement une page précise |

## Différences avec la version VS Code

- La vérification des documents, la création à partir d'un modèle, la génération de propositions de traduction et l'organisation depuis l'INDEX ne sont pas disponibles dans la version Web.
- Les figures TikZ ne sont pas rendues.
- Les modifications ne sont pas écrites dans le dépôt : elles deviennent des brouillons sur votre appareil. La « demande de publication », qui envoie les brouillons sous forme de pull request, est implémentée mais n'est pas activée dans la visionneuse publique. Pour reporter les modifications dans le dépôt, modifiez avec la version VS Code ou dans un clone local.

## Rubriques associées

- [Ouvrir un dépôt GitHub](open-repository.md)
- [Consulter un dépôt privé](private-repository.md)
- [Enregistrer des brouillons](drafts.md)
