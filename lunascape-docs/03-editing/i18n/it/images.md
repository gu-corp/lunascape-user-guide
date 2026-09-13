# Ridimensionare le immagini

Le immagini inserite in un documento si adattano automaticamente alla larghezza del testo e all'altezza dello schermo. Per un'immagine che deve avere una dimensione specifica, puoi impostarne la larghezza.

## Come funziona l'adattamento automatico

- Un'immagine Markdown normale (`![descrizione](./images/screen.png)`) viene ridotta per rientrare nella larghezza del testo. Non viene mai ingrandita oltre la sua dimensione originale.
- Una schermata verticale viene limitata al 72% dell'altezza dello schermo oppure a 720px, a seconda di quale valore sia più piccolo.

## Impostare la larghezza nell'editor

1. Premi [Modifica] e seleziona l'immagine nella vista visuale.
2. Scegli una larghezza da [Dimensione immagine] nella barra degli strumenti.
3. Premi [Salva].

| Opzione | Larghezza |
|---|---|
| [Automatica] | Non specificata (adattamento automatico) |
| [Piccola (360px)] | 360px |
| [Media (560px)] | 560px |
| [Grande (760px)] | 760px |
| [Larghezza del testo (920px)] | 920px |
| [Personalizzata…] | Un numero intero qualsiasi da 16 a 4096px |

## Impostare la larghezza in Markdown

Assegna un valore numerico `width` al tag HTML `img`. Questa forma viene visualizzata come immagine anche su GitHub e in MDX.

```html
<img src="./images/screen.png" alt="Schermata delle impostazioni" width="360" />
```

> **Nota**
>
> - `width` accetta solo un numero, senza `px` o `%`. Un valore superiore alla larghezza del testo rientra comunque nella larghezza del testo quando viene visualizzato.
> - I percorsi delle immagini sono relativi al documento. Le immagini che si trovano al di fuori della radice della documentazione non vengono mostrate.

## Argomenti correlati

- [Modificare un documento](README.md)
- [I diagrammi, le formule o le immagini non vengono visualizzati](../07-troubleshooting/rendering.md)
