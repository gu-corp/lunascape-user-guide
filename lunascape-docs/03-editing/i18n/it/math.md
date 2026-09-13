# Scrivere formule

Le formule si scrivono con la notazione TeX e vengono visualizzate sul dispositivo con KaTeX. Non viene usata la rete.

## Come si scrivono

| Tipo | Notazione | Esempio |
|---|---|---|
| Formula in linea (all'interno del testo) | `$...$` oppure `\(...\)` | `La relazione tra massa ed energia si esprime con $E = mc^2$.` |
| Formula in blocco (su una riga a sé) | `$$...$$` oppure `\[...\]` | Vedi sotto |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Non servono spazi prima e dopo i delimitatori. La formula viene riconosciuta anche quando è adiacente a testo giapponese, come in `値は$V=-H$である`.
- Un `$` all'interno del codice in linea o di un blocco di codice non viene trattato come formula e resta visualizzato così com'è.
- Le scritture che sembrano importi, come `$5 and $10`, non vengono trattate come formule.

## Modificare

Nella visualizzazione visiva le formule sono mostrate già composte. Per modificarne il contenuto, premi [Markdown] nella schermata di modifica e modifica il sorgente. Anche salvando dalla visualizzazione visiva, il sorgente TeX e la forma originale dei delimitatori (`$` oppure `\(`) restano invariati.

> **Nota**
>
> - Per sicurezza KaTeX funziona con `trust: false` e ha limiti di dimensione (`maxSize: 50`) e di espansione delle macro (`maxExpand: 1000`). Le formule che superano questi limiti non vengono visualizzate.
> - In un documento esistente, un `tikzpicture` scritto dentro `$$...$$` o `\[...\]` viene riconosciuto come diagramma TikZ e non come formula.

## Argomenti correlati

- [Scrivere diagrammi e grafici](diagrams.md)
- [I diagrammi, le formule o le immagini non vengono visualizzati](../07-troubleshooting/rendering.md)
