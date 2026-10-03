# Öppna en lagringsplats på GitHub

I webbversionen och i Lunascape kan du öppna en lagringsplats på GitHub och läsa den direkt, utan att duplicera den. Offentliga lagringsplatser kräver ingen inloggning.

## Öppna från skärmen

1. Tryck på [Öppna dokument] (mappikonen) i verktygsfältet. Skärmen ”Öppna dokument” öppnas.
2. Välj i den vänstra kolumnen var du vill öppna från.

   | Plats | Vad som visas |
   |---|---|
   | Alla | Allt nedan. Det du har öppnat nyligen visas först |
   | Nyligen öppnade | Lagringsplatser och mappar som du har öppnat tidigare |
   | Utvalda | Handböcker som webbplatsen rekommenderar |
   | GitHub-lagringsplatser | När du är inloggad med GitHub: de lagringsplatser som du kan läsa |
   | Den här datorn | Mappar på den här enheten. I Lunascape visas även duplicerade lagringsplatser här |

3. Tryck på [Öppna] på raden som du vill öppna. Skriv i [Filtrera på dokument- eller lagringsplatsnamn] längst upp om du vill begränsa raderna.

Om en lagringsplats inte finns i listan anger du den med [Ange owner/repo och öppna] i den vänstra kolumnen.

> **Tips**
>
> - Listan visar de GitHub-lagringsplatser där GitHub-appen ”Lunascape Docs” är installerad och där du har läsbehörighet. Om en lagringsplats saknas ber du ägaren att lägga till appen.

## Kontrollera var dokumentet finns

Den lilla ikonen till vänster i verktygsfältet (platsetiketten) visar var dokumentet som du läser finns.

| Ikon | Plats |
|---|---|
| GitHub-märket | Dokumentet läses från GitHub. Inget sparas på den här enheten |
| En dator | En mapp på den här enheten som Lunascape hanterar. Git-grenens namn och antalet ändrade filer visas också |
| En mapp | En mapp på den här enheten |

Tryck på ikonen om du vill se platsen, statusen och vad du kan göra därifrån, till exempel [Visa på GitHub] och [Kopiera länk].

## Duplicera en lagringsplats i Lunascape

I Lunascape kan du duplicera en lagringsplats från GitHub till den här enheten. Därefter kan du redigera och checka in ändringar med Git.

- På skärmen ”Öppna dokument” trycker du på [Duplicera] på lagringsplatsens rad.
- Om du läser en lagringsplats som du har öppnat från GitHub trycker du på platsetiketten och sedan på [Duplicera till den här datorn]. När dupliceringen är klar öppnas samma dokument från kopian på den här enheten.

En duplicerad lagringsplats markeras med ”Finns på den här datorn” i listan, och [Öppna på den här datorn] visas först på raden.

## Öppna med en URL

Adressen består av lagringsplatsen följd av dokumentets plats. Platsen anges som den är i lagringsplatsen, så ordningen blir densamma som i GitHub-URL:en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Vad du anger | Skrivsätt |
|---|---|
| Endast lagringsplatsen (standardgren) | `/github/owner/repo` |
| Ett dokument i lagringsplatsen | `/github/owner/repo/docs/01-product/vision.md` |
| En gren eller tagg | Lägg till `?ref=v1.2.0` sist |

Adressen ändras när du byter sida. Tryck på [Dela det här dokumentet] i verktygsfältet om du vill skicka en länk till sidan som du läser. Webbläsarens [Tillbaka] och [Framåt] fungerar också.

Den äldre formen med `?source=` går fortfarande att öppna. När sidan har öppnats skrivs adressen om till den nya formen.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Observera**
>
> - Utan inloggning gäller användningsgränsen för GitHub API (60 anrop per timme). Använd [Logga in med GitHub] för lagringsplatser med många dokument eller om du läser upprepade gånger.
> - Grennamn som innehåller `/` (till exempel `feature/xxx`) kan anges med `?ref=` i adressformen ovan. De kan inte skrivas i formen med `?source=`.
> - Dokumenten läses in med läsarens egna GitHub-behörigheter. Den som saknar läsbehörighet ser dem inte.

## Öppna dokument från en lokal mapp

Tryck på [Öppna dokument] i verktygsfältet. Tryck sedan på [Öppna dokument från en lokal mapp] i den vänstra kolumnen och välj en mapp på enheten. Filerna bearbetas i webbläsaren och skickas aldrig någon annanstans. Funktionen fungerar i webbläsare som kan välja mappar (Chrome, Edge med flera).

## Relaterade avsnitt

- [Visa en privat lagringsplats](private-repository.md)
- [Det går inte att öppna eller logga in i webbversionen](../07-troubleshooting/web.md)
