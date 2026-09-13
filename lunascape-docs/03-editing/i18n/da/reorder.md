# Ændre dokumenternes rækkefølge

Den rækkefølge, der vises i INDEX, kan ændres med træk og slip eller fra tastaturet. Den ændrede rækkefølge gemmes i dokumentets front matter som `navigation.order`.

## Sortér med træk og slip

1. Træk et dokument eller en mappe i INDEX.
2. Slip det før eller efter et element på samme niveau, eller oven på en mappe.
   Inden for samme niveau ændres rækkefølgen. Slipper du elementet på en anden mappe, flyttes det til den mappe.

## Sortér med tastaturet eller menuen

- Sæt fokus på et element i INDEX, og tryk på `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Vælg [Flyt en op] / [Flyt en ned] i elementets menu.

## Det, der gemmes

- Når du sorterer inden for samme niveau, opdateres `navigation.order` i originaldokumentets front matter. For en mappe skrives værdien i mappens `README.md`. Har mappen ingen `README.md`, oprettes en `README.md`, der kun indeholder front matter.
- Når du flytter til en anden mappe, flyttes originaldokumentet og de tilhørende oversættelser samlet. Før flytningen vises en bekræftelse, fordi relative links kan blive påvirket.
- Der foretages hverken staging eller commit i Git.

> **Bemærk**
>
> - Du kan ikke sortere, mens der filtreres, mens et dokument redigeres, eller i en browser, du ikke har tillid til.
> - Når der vises "INDEX er blevet opdateret", er en anden ændring netop blevet anvendt. Gentag handlingen.
> - Startsiden kan ikke flyttes til en anden mappe.

> **Tip**
>
> Hvis du giver `navigation.order` værdier i spring på 100, for eksempel 100, 200, 300, er det let at indsætte dokumenter imellem senere. Se [Angive navigationsoplysninger](../04-document-tools/navigation-metadata.md) for detaljer.

## Relaterede emner

- [Oprette og organisere dokumenter og mapper](organize.md)
- [Angive navigationsoplysninger](../04-document-tools/navigation-metadata.md)
