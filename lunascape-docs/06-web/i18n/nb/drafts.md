# Lagre et utkast

Når du redigerer et dokument i webversjonen, skrives ikke endringene til repositoriet. De lagres inne i nettleseren som et «utkast».

## Opprette et utkast

1. Åpne et dokument og trykk [Rediger] nederst til høyre.
2. Rediger og trykk [Lagre].
   «下書きとして保存しました» (Lagret som utkast) vises, og endringen lagres i nettleseren.

- Dokumenter med et utkast får et merke i INDEX. Over teksten vises «この文書は端末内の下書きです（未公開）» (Dette dokumentet er et utkast på enheten, ikke publisert).
- [Utkast] på verktøylinjen viser antallet, og når du trykker på den, åpnes listen over utkast.

## Forkaste et utkast

- For å forkaste utkastet til ett dokument trykker du [Forkast utkastet] over teksten.
- For å forkaste alle utkastene bruker du utkastlisten.

## Overføre til repositoriet

«Publiseringsforespørsel», som sender utkast som en Pull Request, er implementert, men er ikke aktivert i den offentlige visningen. For å overføre til repositoriet må du redigere med VS Code-versjonen eller i en lokal klone.

> **Merk**
>
> - Utkast lagres i nettleseren (IndexedDB). De overføres ikke til en annen nettleser eller en annen enhet, og hvis du sletter nettstedsdataene i nettleseren, forsvinner utkastene også.
> - Hvis dokumentet i repositoriet oppdateres etter at du har opprettet et utkast, vises «上流が更新されています» (Oppstrøms er oppdatert). Kontroller innholdet, og avgjør deretter om du vil forkaste utkastet eller bruke det som det er.
> - Hvis du åpner en lokal mappe fra [Åpne dokumenter] og redigerer, lagres endringene direkte til filen dersom nettleseren støtter det. I nettlesere som ikke støtter det, beholdes de bare så lenge økten varer.

## Relaterte emner

- [Hva du kan gjøre i webversjonen](README.md)
- [Redigere et dokument](../03-editing/README.md)
