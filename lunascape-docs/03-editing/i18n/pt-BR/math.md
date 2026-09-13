# Escrever fórmulas matemáticas

As fórmulas matemáticas são escritas na notação TeX e renderizadas no seu dispositivo com KaTeX. Nenhuma rede é usada.

## Como escrever

| Tipo | Delimitadores | Exemplo |
|---|---|---|
| Fórmula em linha (dentro de uma frase) | `$...$` ou `\(...\)` | `A relação entre massa e energia é $E = mc^2$.` |
| Fórmula em destaque (em uma linha própria) | `$$...$$` ou `\[...\]` | Veja abaixo |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Não é necessário espaço antes ou depois dos delimitadores. Fórmulas adjacentes a texto em japonês, como `値は$V=-H$である`, são reconhecidas.
- Um `$` dentro de código em linha ou de um bloco de código não é tratado como fórmula e aparece como está.
- Textos com aparência de valores monetários, como `$5 and $10`, não são tratados como fórmulas.

## Editar

Na exibição visual, as fórmulas aparecem renderizadas. Para alterar o conteúdo, pressione [Markdown] na tela de edição e edite o código-fonte. Ao salvar pela exibição visual, o código-fonte TeX e a forma original do delimitador (`$` ou `\(`) são mantidos.

> **Atenção**
>
> - Por segurança, o KaTeX é executado com `trust: false` e tem limites de tamanho (`maxSize: 50`) e de expansões de macro (`maxExpand: 1000`). Fórmulas que ultrapassam esses limites não são renderizadas.
> - Um `tikzpicture` escrito dentro de `$$...$$` ou `\[...\]` em um documento existente é reconhecido como diagrama TikZ, e não como fórmula matemática.

## Tópicos relacionados

- [Escrever diagramas e gráficos](diagrams.md)
- [Diagramas, fórmulas matemáticas ou imagens não aparecem](../07-troubleshooting/rendering.md)
