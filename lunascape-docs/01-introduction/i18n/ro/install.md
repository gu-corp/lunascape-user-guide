# Instalarea extensiei

Extensia VS Code „Lunascape Docs Pro” este distribuită ca fișier VSIX. Este gratuită; „Pro” indică ediția care predă lucrul unui AI și se actualizează singură.

## Cerințe

- VS Code 1.90 sau mai recent
- Funcțiile care scriu fișiere — crearea de documente, organizarea INDEX, salvarea setărilor de verificare, traducerea — funcționează numai într-un spațiu de lucru pe care l-ați marcat ca de încredere în VS Code.

## Instalarea

1. Obțineți fișierul VSIX. Această legătură indică întotdeauna versiunea curentă.

   [Descărcați lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Deschideți vizualizarea Extensii (`⇧⌘X` / `Ctrl+Shift+X`).
3. Alegeți [Instalare din VSIX…] din meniul `…` din colțul din dreapta sus și selectați fișierul descărcat.

### Din linia de comandă

Un singur rând, dacă preferați să nu părăsiți terminalul. Descarcă și instalează.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Notă**
> Dacă `code` nu este găsit, executați [Comandă shell: Instalează comanda „code” în PATH] din Paleta de comenzi (`⇧⌘P` / `Ctrl+Shift+P`).

## Actualizarea

Când este publicată o versiune mai nouă, extensia o descarcă și o instalează singură. VS Code vă propune să reîncărcați fereastra, iar atunci începeți să o folosiți. Setările și documentele rămân neschimbate.

Verifică o dată pe zi. Pentru a verifica imediat, executați [Lunascape Docs: Verifică actualizările] din Paleta de comenzi (`⇧⌘P` / `Ctrl+Shift+P`).

Setarea `lunascapeDocEditor.update.check` schimbă ce se întâmplă.

| Setare | Ce se întâmplă |
|---|---|
| Instalează o versiune mai nouă când este publicată | Implicit |
| Anunță-mă și lasă-mă să decid de fiecare dată | Apare o notificare și nimic nu se schimbă până nu apăsați [Actualizează] |
| Nu verifica niciodată | Nu se întâmplă nimic |

### Când nu se poate actualiza

„Actualizarea nu a putut fi descărcată: No Servers” înseamnă că versiunea instalată este 0.22.18 sau mai veche. Funcția ei de actualizare eșuează de fiecare dată la ultimul pas după descărcare, așa că nu se poate aduce singură la o versiune mai nouă. Reinstalați o singură dată manual, ca mai sus; de atunci înainte se actualizează singură.

## Verificarea versiunii

Deschideți „Lunascape Docs Pro” în vizualizarea Extensii pentru a vedea versiunea instalată. Veți avea nevoie de ea când raportați o problemă.

## Subiecte conexe

- [Crearea primelor documente](first-documents.md)
- [Raportarea unei probleme](../07-troubleshooting/report.md)
