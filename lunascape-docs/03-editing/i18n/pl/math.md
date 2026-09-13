# Pisanie wzorów matematycznych

Wzory matematyczne zapisuje się w notacji TeX i renderuje lokalnie na urządzeniu za pomocą KaTeX. Sieć nie jest używana.

## Notacja

| Rodzaj | Ograniczniki | Przykład |
|---|---|---|
| Wzór w tekście (w zdaniu) | `$...$` lub `\(...\)` | `Masę i energię wiąże zależność $E = mc^2$.` |
| Wzór blokowy (w osobnym wierszu) | `$$...$$` lub `\[...\]` | Patrz niżej |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Wokół ograniczników nie są potrzebne spacje. Wzór przylegający bezpośrednio do tekstu japońskiego, na przykład `値は$V=-H$である`, również zostanie rozpoznany.
- Znak `$` wewnątrz kodu w tekście lub bloku kodu pozostaje zwykłym tekstem.
- Zapisy przypominające kwoty, takie jak `$5 and $10`, nie są traktowane jako wzór.

## Edytowanie

W widoku wizualnym wzory są pokazywane w postaci wyrenderowanej. Aby zmienić treść, naciśnij [Markdown] w edytorze i edytuj źródło. Zapisanie z widoku wizualnego zachowuje źródło TeX oraz pierwotną postać ograniczników (`$` albo `\(`) bez zmian.

> **Uwaga**
>
> - Ze względów bezpieczeństwa KaTeX działa z ustawieniem `trust: false` oraz ogranicza rozmiar (`maxSize: 50`) i liczbę rozwinięć makr (`maxExpand: 1000`). Wzory przekraczające te limity nie są renderowane.
> - Element `tikzpicture` zapisany wewnątrz `$$...$$` lub `\[...\]` w istniejącym dokumencie jest rozpoznawany jako rysunek TikZ, a nie jako wzór.

## Tematy pokrewne

- [Pisanie diagramów i wykresów](diagrams.md)
- [Diagramy, wzory lub obrazy nie są wyświetlane](../07-troubleshooting/rendering.md)
