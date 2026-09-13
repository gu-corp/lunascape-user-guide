# Instalacija proširenja

VS Code proširenje „Lunascape Docs Pro” distribuira se kao VSIX datoteka. Besplatno je; „Pro” označava izdanje koje predaje posao umjetnoj inteligenciji i samo se ažurira.

## Zahtjevi

- VS Code 1.90 ili noviji
- Značajke koje zapisuju datoteke — stvaranje dokumenata, organiziranje INDEX-a, spremanje postavki provjere, prevođenje — rade samo u radnom prostoru koji ste u VS Code-u označili kao pouzdan.

## Instalacija

1. Nabavite VSIX datoteku. Ova poveznica uvijek pokazuje na trenutnu verziju.

   [Preuzmite lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Otvorite prikaz proširenja (`⇧⌘X` / `Ctrl+Shift+X`).
3. Iz izbornika `…` u gornjem desnom kutu odaberite [Instaliraj iz VSIX-a…] i odaberite datoteku koju ste preuzeli.

### Putem naredbenog retka

Jedan redak, ako radije ne biste napuštali terminal. Preuzima i instalira.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Napomena**
> Ako se `code` ne pronađe, pokrenite [Naredba ljuske: Instaliraj naredbu „code” u PATH] iz palete naredbi (`⇧⌘P` / `Ctrl+Shift+P`).

## Ažuriranje

Kada se objavi novija verzija, proširenje je samo preuzima i instalira. VS Code ponudi ponovno učitavanje prozora i tada je počinjete koristiti. Vaše postavke i dokumenti ostaju netaknuti.

Provjera se izvodi jednom dnevno. Da provjerite odmah, pokrenite [Lunascape Docs: Provjeri ima li novije verzije] iz palete naredbi (`⇧⌘P` / `Ctrl+Shift+P`).

Postavka `lunascapeDocEditor.update.check` mijenja što se događa.

| Postavka | Što se događa |
|---|---|
| Instaliraj noviju verziju kada se objavi | Zadano |
| Obavijesti me i pusti me da svaki put odlučim | Pojavi se obavijest i ništa se ne mijenja dok ne pritisnete [Ažuriraj] |
| Nikad ne provjeravaj | Ništa se ne događa |

### Kada se ne može ažurirati

Poruka „Ažuriranje nije moguće preuzeti: No Servers” znači da je instalirana verzija 0.22.18 ili starija. Njezin postupak ažuriranja svaki put zakaže u posljednjem koraku, pa se sam ne može dovesti na noviju verziju. Instalirajte jednom ručno, kao gore; od tada se ažurira sam.

## Provjera verzije

Otvorite „Lunascape Docs Pro” u prikazu proširenja da vidite instaliranu verziju. Trebat će vam kada prijavljujete problem.

## Povezane teme

- [Stvaranje prvih dokumenata](first-documents.md)
- [Prijava problema](../07-troubleshooting/report.md)
