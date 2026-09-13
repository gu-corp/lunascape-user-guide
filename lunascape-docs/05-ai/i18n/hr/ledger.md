# Evidencija i zapisi

Evidencija na vrhu kartice [AI] prikazuje stanje prijevoda za svaki podržani jezik. I bez upotrebe AI-ja možete provjeriti što nedostaje.

| Prikaz | Značenje |
|---|---|
| Nedostaje prijevod | Broj dokumenata koji još nemaju prijevod |
| Zastarjelo | Broj dokumenata čiji prijevod postoji, ali je izvornik noviji od trenutka zabilježenog u zapisu |
| Prevedeno | Broj prijevoda koji prate izvornik |

Evidencija se izračunava pretraživanjem korijena dokumentacije. U tome ne sudjeluju ni AI ni jezični model.

## Ažuriranje zapisa o prijevodu

Za utvrđivanje stanja „Zastarjelo” potrebno je zabilježiti izvornik i prijevod onakvima kakvi su bili u trenutku prevođenja. AI sesijskog tipa zapisuje datoteke izravno, pa se zapis ne stvara automatski.

1. Kada je prijevod gotov i sadržaj provjeren, pritisnite [Ažuriraj zapise o prijevodu].
2. Prijevodi bez zapisa bilježe se kao oni koji odgovaraju trenutačnom izvorniku.

Sesije programa Claude Code i spremanje putem pružatelja API-ja bilježe zapis automatski (sesija dobiva uputu da upotrijebi MCP alat `record_translation_freshness`). Ovaj je gumb potreban kada ste prijevod izradili u Codexu ili u VS Code chatu.

Nakon toga, promijenite li izvornik, njegov će se prijevod prikazivati kao „Zastarjelo”.

> **Napomena**
>
> - Prijevodi koji već imaju zapis ne prepisuju se, kako se postojeće stanje „Zastarjelo” ne bi izbrisalo.
> - Zapisi se spremaju u `.lunascape-docs/translation-freshness.json`. Spremaju se samo relativne putanje, jezici, hashevi sadržaja te datum i vrijeme, a tekst dokumenta nikada.

## Povezane teme

- [Poslovi koje možete predati](tasks.md)
- [Čitanje na drugom jeziku](../02-reading/languages.md)
