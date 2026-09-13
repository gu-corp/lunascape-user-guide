# Abrir um repositório do GitHub

Na versão Web, você abre documentos indicando um repositório do GitHub. Repositórios públicos não exigem login.

## Abrir pela tela

1. Abra <https://docs.lunascape.org/>.
2. Pressione [Abrir documentos] (o ícone de pasta) na barra de ferramentas.
3. Digite o repositório em [Informar um repositório] e pressione [Abrir].
   Quando você está conectado ao GitHub, também é possível escolher em uma lista por meio de [Escolher entre repositórios legíveis].

> **Dica**
>
> - O ícone do GitHub ao lado abre no github.com o documento que você está lendo. Ele não serve para abrir documentos.

## Abrir por URL

O endereço reúne, na mesma ordem, o repositório e a posição do documento. Como o caminho é a posição dentro do repositório, a sequência é a mesma da URL do GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Indicação | Como escrever |
|---|---|
| Somente o repositório (branch padrão) | `/github/owner/repo` |
| Um documento dentro do repositório | `/github/owner/repo/docs/01-product/vision.md` |
| Uma branch ou tag | acrescente `?ref=v1.2.0` ao final |

Ao mudar de página, o endereço também muda. Pressione [Compartilhar este documento] na barra de ferramentas para entregar a alguém o link da página que você está lendo. Os botões [Voltar] e [Avançar] do navegador também funcionam.

O formato anterior, com `?source=`, continua abrindo como sempre. Depois de aberto, ele é reescrito no novo formato.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Nota**
>
> - Sem fazer login, vale o limite de uso da API do GitHub (60 requisições por hora). Em repositórios com muitos documentos ou em leituras repetidas, use [Entrar com o GitHub].
> - Nomes de branch que contêm `/` (como `feature/xxx`) podem ser indicados com `?ref=` no formato de endereço acima. O formato `?source=` não permite escrevê-los.
> - Os documentos são carregados com as permissões do GitHub de quem lê. Quem não tem permissão de leitura não os vê.

## Abrir documentos de uma pasta local

Pressione [Abrir documentos] na barra de ferramentas e, em [Abrir documentos de uma pasta local], abaixo da lista, escolha uma pasta do seu dispositivo. Os arquivos são processados dentro do navegador e não são enviados para fora. Isso funciona em navegadores compatíveis com a seleção de pastas (Chrome, Edge e outros).

## Tópicos relacionados

- [Consultar um repositório privado](private-repository.md)
- [Não consigo abrir a versão Web ou fazer login](../07-troubleshooting/web.md)
