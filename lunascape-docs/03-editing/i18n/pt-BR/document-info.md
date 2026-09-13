# Mostrar as informações do documento

A "tabela de controle de documento" colocada no início de um documento (uma tabela com ID do documento, versão, data de atualização, estado e assim por diante) é exibida durante a leitura como uma linha compacta de "Informações do documento". O próprio Markdown continua sendo uma tabela comum, portanto também pode ser lido normalmente no GitHub.

## Condições para a exibição

Coloque uma tabela de duas colunas como a seguir imediatamente após o título (H1).

```markdown
# Requisitos funcionais

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- A condição é que exista uma linha de ID do documento e vários campos de gerenciamento.
- Uma tabela colocada sob um título `## 文書管理` ou `## Document information` também é reconhecida.
- Tabelas no meio do texto e tabelas comuns de "item/valor" não são convertidas.

## Como é exibido

- Durante a leitura, apenas o estado e a data de atualização são exibidos em tamanho pequeno.
- Pressione a linha para exibir todos os campos.
- Ao imprimir, todos os campos são exibidos.
- Na tela de edição, a tabela aparece como uma tabela comum e pode ser editada assim mesmo.

> **Dica**
>
> Para sempre exibir a tabela em vez de recolhê-la, desative [Recolher as informações do documento] em [Configurações de exibição].

## Tópicos relacionados

- [Editar um documento](README.md)
- [Alterar as configurações de exibição](../02-reading/display-settings.md)
