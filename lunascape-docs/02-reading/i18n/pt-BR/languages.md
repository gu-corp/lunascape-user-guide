# Ler em outro idioma

Quando um documento tem traduções, você pode alternar o idioma no menu de idiomas (globo) da barra de ferramentas.

## Alternar o idioma

1. Pressione o menu de idiomas na barra de ferramentas.
   Ele mostra o idioma da página atual e como ele foi determinado (caminho da tradução, detecção automática ou idioma padrão do projeto).
2. Escolha o idioma que deseja ler.
   A tradução do mesmo documento é aberta. O idioma escolhido é memorizado e o próximo documento que você abrir será exibido nesse idioma, quando houver uma tradução.

A lista mostra se cada idioma tem uma tradução deste documento.

| Rótulo | Significado |
|---|---|
| Com tradução | A tradução existe e pode ser aberta |
| Sem tradução | O idioma é compatível com o projeto, mas este documento ainda não tem tradução |
| Desatualizado | Existe uma tradução, mas o documento original foi alterado depois de traduzido |

> **Nota**
>
> - Escolher um idioma apenas abre uma tradução já existente. Isso nunca gera uma tradução nem cria um arquivo. Para criar uma tradução, use [Criar ou gerenciar traduções…] no mesmo menu.
> - Quando o idioma da página atual é considerado diferente do idioma padrão do projeto, um aviso é exibido. As configurações nunca são alteradas.

## Idioma em que o documento é aberto

Ao abrir um documento, o primeiro idioma de exibição é decidido nesta ordem.

1. O idioma que você mesmo escolheu antes nesta raiz da documentação. Sua escolha é salva (escolher o idioma padrão também é salvo como uma escolha).
2. O idioma de exibição do VS Code (na versão para navegador Web, as configurações de idioma do navegador). Um idioma compatível correspondente é selecionado automaticamente; um idioma com região, como `en-US`, também corresponde ao idioma base `en`.
3. O idioma de fallback do projeto (`fallbackLocale` em `lunascape-docs.json`).
4. O idioma padrão do projeto.

> **Dica**
>
> - Quando o idioma é selecionado automaticamente, o idioma atual no menu de idiomas exibe "Seleção automática". Passe o ponteiro sobre o selo para ver o motivo.
> - `fallbackLocale` é o idioma mostrado aos leitores cujo idioma do ambiente não corresponde a nenhum dos idiomas compatíveis. Em um projeto cujo documento canônico é em japonês e que tem uma versão em inglês, definir `"en"` abre a versão em inglês para leitores em um ambiente em espanhol, por exemplo. Quando não está definido, o idioma padrão é usado.

## Onde as traduções ficam

Os documentos no idioma padrão permanecem em seu lugar; a tradução vai para uma **pasta `i18n/<idioma>/` ao lado do documento**, com o mesmo nome de arquivo.

```text
docs/
  README.md                  ← idioma padrão (por exemplo, japonês)
  i18n/en/README.md          ← sua versão em inglês
  guide/
    setup.md
    i18n/en/setup.md         ← sua versão em inglês
```

> **Nota**
>
> - Recriar a estrutura de pastas dentro de `i18n/` (`i18n/en/guide/setup.md`) não é reconhecido. A pasta `i18n/` sempre fica ao lado do documento que ela traduz.
> - Esse único local é o único de onde uma tradução é resolvida. Colocar a tradução do mesmo documento também no `i18n/` de uma pasta pai não cria disputa de precedência: a cópia na pasta pai simplesmente se torna um arquivo órfão que nem o menu de idiomas nem o registro veem (e que nunca é excluído automaticamente). Mantenha cada tradução em um só lugar.

## Ler na versão para navegador Web

Na versão para navegador Web também é possível alternar da mesma forma quando há traduções. Para ler em um idioma que não tem tradução, você pode usar o recurso de tradução de página do navegador. Código, fórmulas e diagramas ficam de fora da tradução.

## Tópicos relacionados

- [Entregar trabalho a uma IA](../05-ai/README.md)
- [Trabalho que pode ser entregue](../05-ai/tasks.md)
- [Alterar as configurações de exibição](../02-reading/display-settings.md)
