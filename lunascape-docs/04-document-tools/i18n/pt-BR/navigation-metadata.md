# Configurar metadados de navegação

O nome e a ordem exibidos no INDEX são escritos no YAML front matter de cada documento. Os documentos são exibidos mesmo sem isso, usando o título (H1) e a ordem por nome de arquivo.

## Nome e ordem do documento

Escreva o seguinte no início do documento.

```yaml
---
navigation:
  title: Introdução
  order: 200
---
```

| Campo | Significado |
|---|---|
| `navigation.title` | O nome exibido no INDEX. Quando omitido, usa-se o H1 e, na falta dele, o nome do arquivo |
| `navigation.order` | Um número inteiro que determina a ordem, de forma crescente. Quando omitido, aplica-se uma ordem padrão estável (por nome de arquivo) |

> **Dica**
>
> - Atribua valores de `order` em incrementos de 100, como 100, 200, 300, para poder inserir 150 entre eles mais tarde.
> - Valores de `order` ausentes, inválidos ou duplicados nunca ocultam um documento.
> - Reordenar no INDEX grava o `navigation.order` para você; não é preciso escrevê-lo à mão.

## Nome e ordem da pasta

O nome e a ordem de uma pasta pertencem ao front matter do seu `README.md` (ou `index.md`, quando não houver README). A página de capa não precisa de conteúdo no corpo.

```yaml
---
navigation:
  title: Planejamento de produto
  order: 100
---
```

Uma pasta sem página de capa usa o nome da pasta e a ordem padrão. Quando uma alteração de título ou uma reordenação no INDEX exigir, cria-se um `README.md` apenas com front matter. A simples leitura nunca cria um arquivo.

## Tradução

- A ordem e o papel de uma pasta (página de capa ou apenas configuração) são decididos exclusivamente pelo documento no idioma padrão.
- Uma tradução pode substituir somente o `navigation.title`. Quando o documento canônico tem conteúdo no corpo, o H1 da tradução também é usado como nome.
- Uma tradução por si só nunca adiciona uma página.

## Ordenação e recolhimento de itens filhos

O `navigation.children.sort` e o `navigation.children.defaultCollapsed` na página de capa de uma pasta estão definidos para controlar como seus itens filhos diretos são ordenados e se começam recolhidos. A leitura e a edição deles no VS Code estão planejadas.

## Tópicos relacionados

- [Alterar a ordem dos documentos](../03-editing/reorder.md)
- [Raízes da documentação e convenções de arquivos](structure.md)
