# Dostosowywanie rozmiaru obrazów

Obrazy wstawione do dokumentu automatycznie dopasowują się do szerokości treści i wysokości ekranu. Obrazowi, który ma mieć określony rozmiar, możesz ustawić szerokość.

## Jak działa automatyczne dopasowanie

- Zwykły obraz Markdown (`![opis](./images/screen.png)`) jest zmniejszany tak, aby zmieścił się w szerokości treści. Nigdy nie jest powiększany ponad swój oryginalny rozmiar.
- Wysoki zrzut ekranu jest ograniczony do 72% wysokości ekranu lub 720px, zależnie od tego, która wartość jest mniejsza.

## Ustawianie szerokości w edytorze

1. Naciśnij [Edytuj] i zaznacz obraz w widoku wizualnym.
2. Wybierz szerokość z [Rozmiar obrazu] na pasku narzędzi.
3. Naciśnij [Zapisz].

| Opcja | Szerokość |
|---|---|
| [Automatycznie] | Bez określenia (automatyczne dopasowanie) |
| [Mała (360px)] | 360px |
| [Średnia (560px)] | 560px |
| [Duża (760px)] | 760px |
| [Szerokość treści (920px)] | 920px |
| [Własna…] | Dowolna liczba całkowita od 16 do 4096px |

## Ustawianie szerokości w Markdown

Nadaj znacznikowi HTML `img` liczbową wartość `width`. Ten zapis wyświetla się jako obraz również na GitHub i w MDX.

```html
<img src="./images/screen.png" alt="Ekran ustawień" width="360" />
```

> **Uwaga**
>
> - `width` przyjmuje tylko liczbę, bez `px` ani `%`. Wartość większa niż szerokość treści i tak zostanie wyświetlona w szerokości treści.
> - Ścieżki obrazów są względne wobec dokumentu. Obrazy znajdujące się poza katalogiem głównym dokumentacji nie są wyświetlane.

## Powiązane tematy

- [Edytowanie dokumentu](README.md)
- [Diagramy, wzory matematyczne lub obrazy nie są wyświetlane](../07-troubleshooting/rendering.md)
