# Predavanje posla umjetnoj inteligenciji

Lunascape Docs ne poziva jezični model. Priprema **kontekst, alate i provjere**, a prevođenje, lekturu i pisanje prepušta umjetnoj inteligenciji koju već koristite.

## Zamisao

| Što proizvod priprema | Sadržaj |
|---|---|
| Kontekst | Pravila dokumentacije (gdje se nalaze prijevodi, front matter, standard dokumenta, pojmovnik) i položaj ciljanog dokumenta |
| Radni alati | Popis nedostajućih i zastarjelih prijevoda, čitanje i pisanje dokumenata, izrada iz predloška |
| Naknadne provjere | Provjera pomoću docs-lint te razlika u pokrivenosti i svježini |

Uputa ne sadrži tekst dokumenta. Umjetna inteligencija sama čita datoteke, sama piše i sama provjerava.

## Predajte posao

1. Na alatnoj traci pritisnite [Alati za dokumente] i otvorite karticu [AI].
2. Pod [Zadatak] odaberite posao koji želite predati.
3. Unesite potrebne podatke (ciljni jezik, temu).
4. Pritisnite [Predaj ovaj zadatak].
   Otvara se terminal u VS Code-u, a odabrana umjetna inteligencija prima uputu i započinje rad.

> **Savjet**
>
> Sesiju u Claude Code prate radni alati (MCP poslužitelj `lunascape-docs`). Sesija može sama dohvatiti popis nedostajućih i zastarjelih prijevoda, pokrenuti docs-lint i zabilježiti svježinu nakon prijevoda.

## Provjera rezultata

| Oblik pružatelja | Gdje rezultat završava |
|---|---|
| Sesijski (Claude Code, Codex) | Zapisuje izravno u radno stablo. **Provjerite ga u razlikama u Gitu** |
| API (jezični modeli u VS Code-u, Anthropic, kompatibilni s OpenAI) | Vraća prijedlog za jedan po jedan dokument. Provjerite ga pomoću [Otvori razlike] i zapišite pomoću [Spremi] |

### Provjera prijedloga kod API oblika

Kada pokrenete posao s API pružateljem, prijedlog stiže na karticu [AI].

1. Pritisnite [Otvori razlike] i usporedite ga s trenutačnim sadržajem.
2. Ako je u redu, pritisnite [Spremi]. Kod prijevoda bilježi se i svježina. Ako odustajete, pritisnite [Odbaci].
   Za prekid izrade u tijeku pritisnite [Prekini].

> **Napomena**
>
> - Lunascape Docs nikada ne obavlja pripremu (stage) ni urezivanje (commit) u Gitu. Izmjene obavezno provjerite u razlikama.
> - U radnom prostoru kojemu ne vjerujete, kao ni pri privremenom prikazu mape izvan korijena dokumentacije, posao se ne može predati.

## Povezane teme

- [Poslovi koje možete predati](tasks.md)
- [Postavke AI-ja](settings.md)
- [Popis i zapisi](ledger.md)
