# Tâches disponibles

Choisissez-la sous [Tâche], dans l'onglet [IA]. Chaque tâche modifie les instructions transmises et la vérification effectuée ensuite.

| Tâche | Contenu | Nécessaire | Type d'API |
|---|---|---|---|
| Traduire cette page | Traduit le document affiché dans la langue choisie | Le document ouvert, une langue cible | Oui |
| Traduire les pages non traduites | Traduit l'un après l'autre les documents non traduits et à mettre à jour de la langue choisie | Une langue cible | Session uniquement |
| Relire cette page | Vérifie et corrige la terminologie, le style et les sections exigées par le standard documentaire | Le document ouvert | Oui |
| Créer un document | Crée un document en suivant le standard documentaire et ses modèles | Un sujet (facultatif) | Session uniquement |

## Ce que contiennent les instructions

| N° | Contenu |
|---|---|
| 1 | L'emplacement de la racine de documentation, avec la consigne de ne rien modifier en dehors |
| 2 | La langue par défaut (document de référence) et l'emplacement des traductions : un dossier `i18n/<langue>/` à côté du document |
| 3 | Que `navigation.order` n'appartient qu'au document de référence et qu'une traduction ne peut remplacer que `navigation.title` |
| 4 | Que les identifiants d'exigence, les liens, le code, Mermaid, TeX et la structure du front matter ne doivent pas changer |
| 5 | Le standard documentaire et le glossaire (`terminology` dans `docs-lint.config.json`) |
| 6 | D'exécuter ensuite la vérification du document, de signaler les fichiers modifiés et de n'effectuer aucune opération Git |

> **Conseil**
>
> Les documents visés par « Traduire les pages non traduites » proviennent du registre, à raison de 200 documents par exécution. Relancez la tâche s'il en reste.

## Voir aussi

- [Confier une tâche à une IA](README.md)
- [Le registre et ses enregistrements](ledger.md)
