# Postavke AI-ja

Odaberite AI i model kojima predajete posao. Ovaj zaslon koristi vlastite padajuće izbornike, a ne brzi odabir u VS Codeu.

1. Pritisnite [Alati za dokumente] → karticu [AI] → [Postavke AI-ja…].
2. Odaberite [Davatelja usluge].
   Oni koji se u ovom okruženju ne mogu koristiti prikazuju se kao neodabirni, uz navedeni razlog.
3. Odaberite [Model]. Izbor se mijenja ovisno o davatelju usluge.
4. Zatvorite zaslon. Odabir se sprema za svakog korisnika i koristi se i sljedeći put.

## Davatelji usluge

| Davatelj usluge | Oblik | Način otkrivanja |
|---|---|---|
| Claude Code | Sesijski | Postojanje naredbe `claude` |
| Codex | Sesijski | Postojanje naredbe `codex` |
| Jezični modeli VS Codea | API | Modeli registrirani u VS Code Language Model API |
| Anthropic API | API | Registrirani ključ API-ja |
| API kompatibilan s OpenAI-jem | API | Registrirani ključ API-ja i krajnja točka |

**Sesijski** davatelj sam čita i piše datoteke te sam pokreće provjeru dokumenta. Rezultati se upisuju izravno u radno stablo i pregledavaju se u razlikama u Gitu.

**API** davatelj vraća Markdown jednog dokumenta, a proširenje prikazuje razlike prije spremanja.

## Registriranje ključa API-ja

Anthropic API i API kompatibilan s OpenAI-jem mogu se koristiti nakon što se registrira ključ API-ja.

1. U [Davatelju usluge] odaberite gdje registrirate ključ. Pojavljuje se polje za unos ključa API-ja.
2. Unesite [Ključ API-ja]. Za API kompatibilan s OpenAI-jem unesite i [Krajnju točku] (primjerice `https://api.openai.com/v1`).
3. Pritisnite [Spremi]. Prikazuje se „Ključ registriran”.

> **Napomena**
>
> - Ključ se sprema u SecretStorage VS Codea i više se ne prikazuje. Ne upisuje se ni u `settings.json` ni u dokumente. Možete ga ukloniti s [Izbriši ključ].
> - Popis modela dohvaća se od svake usluge pomoću registriranog ključa. Dok se ne dohvati, prikazuje se poznati popis.
> - API davatelj može izvesti samo „Prevedi ovu stranicu” i „Lektoriraj ovu stranicu”. Obilazak više dokumenata i izradu dokumenata izvedite sesijskim davateljem.

> **Savjet**
>
> Ako se ne pronađe nijedan davatelj usluge, instalirajte Claude Code ili Codex ili registrirajte ključ API-ja. Ponovno otvorite [Postavke AI-ja…] i bit će otkriven.

## Povezane teme

- [Predaja posla AI-ju](README.md)
- [Popis postavki VS Codea](../08-reference/settings.md)
