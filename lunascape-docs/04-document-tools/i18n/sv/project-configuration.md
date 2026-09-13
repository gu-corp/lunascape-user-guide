# Projektinställningar

`lunascape-docs.json` direkt under dokumentroten är de inställningar för dokumentroten som teamet delar. Den hanteras i Git.

## Skapa eller redigera inställningsfilen

- Tryck på [Dokumentverktyg] i verktygsfältet → fliken [Kontroll] → [Var reglerna kommer ifrån och dokumentinställningarna] → [Redigera dokumentinställningarna], så öppnas filen i VS Code. Om filen inte finns skapas en startfil i det ögonblicket.
- Filnamnet `lunascape-docs.json` kopplas automatiskt till det medföljande JSON-schemat, som ger komplettering och en beskrivning av varje fält. Någon `$schema`-rad behövs inte.

## Exempel på inställningar

```json
{
  "id": "product-docs",
  "title": "Produktdokumentation",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Beskrivning av fälten

| Fält | Innebörd | Standard |
|---|---|---|
| `id` | Nyckeln som varje användares visningsinställningar sparas under. Ange ett fast ID när inställningarna ska följa med även om mappen flyttas | Mappens sökväg |
| `title` | Namnet som visas längst till vänster i verktygsfältet och i listan över dokumentrötter. Det ändras inte när visningsspråket byts | Rubriken i rotens README/index, annars mappens namn |
| `indexTitle` | Rubriken för INDEX | `INDEX` |
| `startPage` | Dokumentet som öppnas först (sökväg relativt dokumentroten) | `README.md` |
| `appearance` | Färgsättningen: `light` (alltid ljus) eller `auto` (följer temat i VS Code) | `light` |
| `defaultLocale` | Standardspråket (originaldokumentens språk). Anges som en BCP 47-språktagg (`ja`, `en`, `zh-Hant` med flera). Det är källan för översättning | Inte angivet (härleds ur texten för visning) |
| `fallbackLocale` | Språket som först visas för läsare vars miljöspråk inte stämmer med något av de språk som stöds. Ange ett språk som finns i `locales` | Inte angivet (`defaultLocale` används) |
| `locales` | Listan över språk som stöds. Inkludera `defaultLocale`. De blir alternativ i språkmenyn och mål för översättning | Endast `defaultLocale` |
| `ignoredDirectories` | Mappnamn som utesluts ur INDEX, sökning och kontroller. Anger du fältet ersätts standardvärdet | `["99-archive"]` |
| `tree` | Standardvärden för hur INDEX visas. Användaren kan åsidosätta dem i Visningsinställningar | Som i exemplet ovan |
| `editor.defaultMode` | Redigeringsvyn innan användaren har bytt: `visual` eller `source` | `visual` |
| `editor.showEditButton` | Om [Redigera] visas nedtill till höger i dokumentet | `true` |
| `documentStandards.pack` | Det Standard Pack som används för dokumentkontroller och mallar: `builtin:<namn>` eller en sökväg relativt dokumentroten | Inget |
| `documentStandards.profile` | Namnet på en profil som paketet definierar | Inget |
| `translation.enabled` | Aktiverar översättningsförslag och samlad översättning | `true` |
| `translation.contextFiles` | Originaldokument i Markdown (sökvägar relativt dokumentroten) som skickas med vid översättning som stöd för terminologi och stil | `[]` |
| `translation.maxContextCharacters` | Övre gräns för referensdokumentens sammanlagda antal tecken (högst 1048576) | `49152` |
| `description` | En rad om dokumentsamlingen. Visas på korten på lagringsplatsens startsida. Precis som `title` kan den skrivas som en sträng eller som ett objekt per språk | Inget |

## Tala om var i lagringsplatsen dokumenten finns

En `lunascape-docs.json` som ligger direkt i lagringsplatsens rot kan innehålla en **karta över lagringsplatsen** i stället för inställningar för den mappen. Skriver du något av de tre fälten nedan blir filen en karta, och mappen är då inte själv någon dokumentrot.

| Fält | Innebörd | Standard |
|---|---|---|
| `defaultFolder` | Vilken mapp som innehåller dokumenten (sökväg relativt denna mapp). Mappen den pekar på behöver ingen egen inställningsfil | Inget (`docs` används) |
| `roots` | Listan över dokumentsamlingar när de är flera (sökvägar relativt denna mapp, i visningsordning). Denna mapp blir då startsidan | Inget |
| `excludes` | Mappar som utesluts när dokumentrötter söks upp (sökvägar relativt denna mapp). Läggs till de inbyggda undantagen, till exempel `node_modules` | `[]` |
| `home.cards` | Om startsidan visar korten för sina samlingar under sin README. Sätt fältet till `false` när du skriver länkarna själv i README | `true` |

Dokumentroten bestäms i följande ordning. Den första träffen uppifrån och ned används.

1. Den mapp du anger med en inställning eller ett kommando
2. Det som `defaultFolder` eller `roots` pekar på i `lunascape-docs.json` i roten
3. En mapp som har en `lunascape-docs.json` (finns två eller fler under en gemensam överordnad mapp blir den mappen startsida)
4. Mappen `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Lagringsplatsens rot i sig

> **Tips**
>
> Skriver du ingenting gäller punkt 4, så en vanlig lagringsplats med en enda `docs/` fungerar precis som förut. Skriv `defaultFolder` bara när mappen ska heta något annat, till exempel `manual`.

### Exempel på en karta

```json
{
  "title": "Lunascape Hjälp",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Inställningarnas prioritetsordning

Fält som rör visningen gäller i följande ordning.

1. Användarens visningsinställningar (panelen [Visningsinställningar])
2. Inställningarna i VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Produktens standardvärden

Språken (`defaultLocale`, `fallbackLocale`, `locales`) är det enda undantaget: där gäller `lunascape-docs.json`. Projektets språk kan inte åsidosättas med personliga inställningar i VS Code.

> **Obs!**
>
> Ett Standard Pack kan också anges som `standard` i `docs-lint.config.json`. Finns det i båda gäller `docs-lint.config.json`.

## Relaterade avsnitt

- [Ändra kontrollregler](rules.md)
- [Ändra visningsinställningar](../02-reading/display-settings.md)
- [Lista över inställningar i VS Code](../08-reference/settings.md)
