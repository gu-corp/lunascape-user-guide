# Formules schrijven

Formules schrijft u in TeX-notatie; ze worden met KaTeX op uw apparaat weergegeven. Er wordt geen netwerk gebruikt.

## Notatie

| Soort | Notatie | Voorbeeld |
|---|---|---|
| Formule in de tekst (inline) | `$...$` of `\(...\)` | `De relatie tussen massa en energie is $E = mc^2$.` |
| Formule op een eigen regel (display) | `$$...$$` of `\[...\]` | Zie hieronder |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Rond de scheidingstekens is geen spatie nodig. Ook een formule die direct tegen Japanse tekst aan staat, zoals `値は$V=-H$である`, wordt herkend.
- Een `$` binnen inlinecode of een codeblok wordt niet als formule behandeld, maar ongewijzigd weergegeven.
- Tekst die op een geldbedrag lijkt, zoals `$5 and $10`, wordt niet als formule behandeld.

## Bewerken

In de visuele weergave ziet u de formule als weergegeven resultaat. Druk op [Markdown] in het bewerkingsscherm en bewerk de bron om de inhoud te wijzigen. Ook bij opslaan vanuit de visuele weergave blijven de TeX-bron en de oorspronkelijke vorm van de scheidingstekens (`$` of `\(`) behouden.

> **Let op**
>
> - KaTeX werkt voor de veiligheid met `trust: false` en kent limieten voor de grootte (`maxSize: 50`) en het aantal macro-expansies (`maxExpand: 1000`). Formules die deze limieten overschrijden, worden niet weergegeven.
> - Een `tikzpicture` die in een bestaand document binnen `$$...$$` of `\[...\]` staat, wordt herkend als TikZ-diagram en niet als formule.

## Verwante onderwerpen

- [Diagrammen en grafieken schrijven](diagrams.md)
- [Diagrammen, formules of afbeeldingen worden niet weergegeven](../07-troubleshooting/rendering.md)
