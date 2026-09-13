# Não é possível abrir ou entrar na versão Web

## Entrei, mas o repositório não aparece na lista

O GitHub App "Lunascape Docs" não está instalado nessa conta ou o repositório não está incluído. Peça ao proprietário do repositório ou a um administrador da organização que faça a instalação seguindo o procedimento de [Consultar um repositório privado](../06-web/private-repository.md).

## Não consigo avançar da tela de entrada

- Você não tem permissão de leitura no repositório. Peça ao proprietário do repositório que conceda a permissão.
- "O login do GitHub não está configurado neste site": um visualizador instalado por você mesmo não tem serviço de login configurado. O administrador precisa configurar o serviço de login.

## A janela pop-up de entrada não abre

O navegador está bloqueando os pop-ups. Permita os pop-ups deste site e tente novamente.

## Aparece "Sua sessão expirou"

A sessão expirou. Pressione [Entrar com o GitHub] novamente.

## Um repositório público retorna 404

- Verifique a forma `owner/repo@ref/dir`.
- Não é possível indicar nomes de branch que contenham `/`.

## Depois de algum tempo, o carregamento para de funcionar

Sem entrar, aplica-se o limite de uso da API do GitHub (60 vezes por hora). Quando aparecer "Limite de solicitações atingido", aguarde um pouco ou use [Entrar com o GitHub].

## Aparece "Este site não pode exibir este repositório"

Para abrir o repositório a partir de um visualizador instalado por você mesmo, é necessário adicionar a URL desse site em `viewer.origins` no `lunascape-docs.json` do repositório.

## Abro o `index.html` e nada é exibido

Não funciona quando aberto diretamente por `file://`. Abra-o por meio de um servidor HTTP ou use a versão do VS Code.

## No site exportado aparece "lunascape-docs-manifest.json não encontrado"

Publique o conjunto completo de arquivos gerado por `npm run export:web` (incluindo o manifesto), tal como está.

## Não consigo salvar o rascunho

- "Não é possível abrir o IndexedDB" / "Em uso por outra aba": a causa é o modo privado do navegador ou outra aba com o mesmo site aberto. Abra em uma janela normal e feche as outras abas.
- Os rascunhos são salvos por dispositivo e por navegador. Eles não são transferidos para outro dispositivo.

## Itens relacionados

- [Abrir um repositório do GitHub](../06-web/open-repository.md)
- [Salvar um rascunho](../06-web/drafts.md)
