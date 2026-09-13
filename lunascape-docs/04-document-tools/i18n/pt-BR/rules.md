# Alterar as regras de verificação

Você pode alterar o nível de notificação (erro, aviso, informação) de cada item de verificação ou deixar de usá-lo. As alterações são salvas em `docs-lint.config.json` na raiz da documentação e compartilhadas com a equipe.

## Alterar o nível de notificação

1. Na barra de ferramentas, pressione [Ferramentas de documento] e abra a guia [Verificação].
2. Pressione [Revisar e alterar as regras].
   A lista de itens de verificação se expande dentro do mesmo cartão. Cada item mostra sua finalidade e a origem da configuração atual (Project, Profile, Pack ou Default).
3. Escolha o nível de notificação do item que deseja alterar.
4. Pressione [Salvar e verificar de novo].
   A configuração é salva e toda a raiz da documentação é verificada novamente com a nova configuração.

| Opção | Significado |
|---|---|
| [Configuração padrão (…)] | Remove a substituição e volta à configuração padrão, definida na ordem perfil, Standard Pack e valor padrão |
| [Não usar] | Não verifica este item |
| [Informação] / [Aviso] / [Erro] | Relata neste nível de notificação |

> **Nota**
>
> - Para salvar, é necessário um espaço de trabalho confiável.
> - Só é salvo o nível de notificação de cada item. As opções de cada item são mantidas como estão. O Standard Pack e o perfil em si não são alterados nesta tela.
> - Se `docs-lint.config.json` tiver sido alterado externamente pouco antes de salvar, o salvamento é cancelado. Carregue o estado mais recente e tente de novo.
> - Se `docs-lint.config.json` não existir, ele é criado ao salvar.

## Editar os arquivos de configuração diretamente

- Pressione [Abrir as configurações completas] para abrir `docs-lint.config.json` no VS Code.
- Abra [De onde vêm as regras e as configurações do documento] e pressione [Editar as configurações do documento] para abrir `lunascape-docs.json` no VS Code. O Standard Pack e o perfil são escolhidos ali.

Nos dois arquivos, o preenchimento automático e as descrições dos JSON Schemas incluídos na extensão estão ativos.

## Standard Pack e perfis

O Standard Pack é um padrão de documentação que reúne os tipos de documento necessários, a estrutura de capítulos, a terminologia e os modelos. Ele é escolhido em `documentStandards`, em `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

O pacote incluído `builtin:gu-corp-software` tem os perfis `base`, `web-application`, `api-service`, `regulated-financial-product` e `smart-contract`.

## Tópicos relacionados

- [Verificar documentos](check.md)
- [Configurações do projeto](project-configuration.md)
