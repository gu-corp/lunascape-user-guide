# Weergave-instellingen wijzigen

Via [Weergave-instellingen] (tandwiel) op de werkbalk kan elke gebruiker wijzigen hoe de INDEX eruitziet en of de bewerkknop wordt getoond.

1. Druk op [Weergave-instellingen] op de werkbalk.
2. Schakel de gewenste items om. Wijzigingen worden meteen toegepast.
3. Druk nogmaals op [Weergave-instellingen] of klik buiten het paneel om het te sluiten.

## Instelbare items

| Categorie | Item | Werking |
|---|---|---|
| Documenttaal | (huidige status) | Toont de standaardtaal van het project en de weergegeven taal. Via [Projecttalen instellen…] opent u de taalinstellingen van het project |
| Inhoud | [Bestandsnamen] | Toont bestandsnamen in plaats van documenttitels |
| | [Documentpictogrammen] | Toont een pictogram bij elk document |
| | [Mappictogrammen] | Toont een pictogram bij elke map |
| | [Aantallen per map] | Toont het aantal documenten in elke map |
| | [Inspringhulplijnen] | Toont hulplijnen die de hiërarchie aangeven |
| | [Verbergen als er maar één document is] | Sluit de INDEX eenmalig, bij de eerste keer openen, in een documentatiehoofdmap met maar één document |
| | [Documentgegevens samenvouwen] | Vouwt de beheertabel boven aan een document samen tot de regel "Documentgegevens". Staat dit uit, dan wordt de tabel ongewijzigd getoond |
| | [Weergavedichtheid] | Kies de regelafstand van de INDEX uit [Normaal] / [Compact] |
| | [Bewerkknop] | Toont [Bewerken] rechtsonder in het document |
| Acties | [Terugzetten op projectstandaarden] | Verwijdert al uw eigen wijzigingen en keert terug naar de projectinstellingen |
| | [Extensie-instellingen openen] | Opent de instellingen van Lunascape Docs in het instellingenscherm van VS Code |

> **Tip**
>
> - Weergave-instellingen worden per gebruiker en per documentatiehoofdmap opgeslagen en nooit weggeschreven naar bestanden die in Git worden beheerd.
> - Instellingen gelden in de volgorde "weergave-instellingen van de gebruiker → VS Code-instellingen → `lunascape-docs.json` → productstandaarden". Teambrede standaardwaarden legt u vast in `tree` en `editor` in `lunascape-docs.json`.

## Het kleurenschema wisselen

Druk op de themaschakelaar (zon/maan) op de werkbalk om te wisselen tussen een witte achtergrond en het kleurenschema van VS Code. Het kleurenschema bij het openen wordt bepaald door de instelling `lunascapeDocEditor.appearance` (`light` of `auto`).

## Verwante onderwerpen

- [De INDEX gebruiken](index-panel.md)
- [Projectinstellingen](../04-document-tools/project-configuration.md)
- [Overzicht van VS Code-instellingen](../08-reference/settings.md)
