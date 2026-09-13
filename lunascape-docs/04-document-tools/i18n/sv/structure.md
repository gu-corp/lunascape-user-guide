# Dokumentrot och filkonventioner

Reglerna som Lunascape Docs följer för att hitta dokument och bygga upp INDEX. Filsystemet är i sig originalet, så det behövs varken register eller bygginställningar.

## Dokumentrot

- Närmaste `docs`-mapp, eller en mapp som innehåller `lunascape-docs.json`, blir dokumentrot.
- Med en `lunascape-docs.json` behöver mappen inte heta `docs`.
- Om du öppnar en Markdown-fil som inte hör till någon dokumentrot visas dess mapp som en tillfällig dokumentrot.

## Filer som visas i INDEX

- Filer med `.md`, `.markdown` och `.mdx` visas. Nya filer visas alltid, även utan front matter eller navigeringsinformation.
- Mappar som börjar med `.`, `node_modules` och de mappar som anges i `ignoredDirectories` (standard `99-archive`) visas inte.
- Allt under `i18n/` behandlas som översättningar och listas inte separat i INDEX.

## Mappens startsida

- En `README.md` (eller `index.md` om README saknas) som har brödtext blir mappens startsida. Tryck på mappnamnet i INDEX för att öppna den.
- En `README.md` som bara består av front matter, utan brödtext, behandlas som en "beskrivning enbart för inställningar" och visas inte som en sida. Använd den när en mapp bara behöver en titel eller en ordning.
- Om både `README.md` och `index.md` finns har `README.md` företräde.

## Standardspråk och översättningar

- Dokument på standardspråket (originaldokumenten) ligger kvar där de är.
- Översättningen läggs i `i18n/<språk>/` i samma mapp som originaldokumentet, under samma filnamn. Att bygga upp mappstrukturen på nytt under `i18n/` känns inte igen.
- Det är den enda plats en översättning hämtas från. Samma fil placerad någon annanstans blir en lös fil som inget dokument räknar som sin översättning.

```text
docs/
  lunascape-docs.json
  README.md                  ← dokumentrotens startsida (startsidan)
  i18n/en/README.md          ← dess engelska version
  01-product/
    README.md                ← mappens startsida
    requirements.md
    i18n/en/README.md        ← de engelska versionerna av de två ovan
    i18n/en/requirements.md
  99-archive/                ← utesluts från INDEX som standard
```

## Om `_meta.json`

Nextras `_meta.json` används inte för navigering. Befintliga filer varken ändras eller tas bort. I framtiden hanteras de bara av en uttrycklig funktion för import och export.

## Relaterade avsnitt

- [Ställa in navigeringsinformation](navigation-metadata.md)
- [Projektinställningar](project-configuration.md)
- [Byta dokumentrot](../02-reading/roots.md)
