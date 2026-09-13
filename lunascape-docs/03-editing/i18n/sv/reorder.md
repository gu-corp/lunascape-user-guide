# Ändra dokumentens ordning

Ordningen som visas i INDEX kan ändras med dra och släpp eller från tangentbordet. Den ändrade ordningen sparas i dokumentets front matter som `navigation.order`.

## Ordna om med dra och släpp

1. Dra ett dokument eller en mapp i INDEX.
2. Släpp det före eller efter ett objekt på samma nivå, eller på en mapp.
   Inom samma nivå ändras ordningen. Om du släpper på en annan mapp flyttas objektet till den mappen.

## Ordna om med tangentbordet eller menyn

- Placera fokus på ett objekt i INDEX och tryck på `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Välj [Flytta upp ett steg] / [Flytta ned ett steg] i objektets meny.

## Detta sparas

- När du ordnar om inom samma nivå uppdateras `navigation.order` i originaldokumentets front matter. För en mapp skrivs värdet till mappens `README.md`. I en mapp som saknar `README.md` skapas en `README.md` med enbart front matter.
- När du flyttar till en annan mapp flyttas originaldokumentet och dess översättningar tillsammans. Före flytten visas en bekräftelse, eftersom relativa länkar kan påverkas.
- Git-staging och commit utförs aldrig.

> **Obs!**
>
> - Det går inte att ordna om medan du filtrerar, medan du redigerar ett dokument eller i en arbetsyta som inte är betrodd.
> - När meddelandet ”INDEX har uppdaterats” visas har en annan ändring just tillämpats. Utför åtgärden en gång till.
> - Startsidan kan inte flyttas till en annan mapp.

> **Tips**
>
> Om du anger `navigation.order` i steg om 100, till exempel 100, 200, 300, blir det enkelt att infoga dokument däremellan senare. Mer information finns i [Ange navigeringsinformation](../04-document-tools/navigation-metadata.md).

## Relaterade avsnitt

- [Skapa och organisera dokument och mappar](organize.md)
- [Ange navigeringsinformation](../04-document-tools/navigation-metadata.md)
