# Templates de protocolos do LAM+

[English](README.md) | [Português](README.pt-BR.md)

Estes arquivos fornecem a estrutura mínima compartilhada pelos protocolos laboratoriais do LAM+. São modelos de conteúdo, não procedimentos concluídos.

## Criar um protocolo

1. Copie os dois templates para o diretório `protocols/` do equipamento correspondente.
2. Dê aos dois arquivos o mesmo nome-base:

```text
acquisition.md
acquisition.pt-BR.md
```

3. Substitua `LAM-XXX-000` somente depois de confirmar o escopo e o identificador.
4. Mantenha código, versão, data, autores, revisores e status sincronizados nos dois idiomas.
5. Substitua ou remova todos os comentários HTML de orientação antes da aprovação. Esses comentários não aparecem na renderização normal nem no PDF produzido pelo Pandoc.
6. Remova seções opcionais apenas quando não forem aplicáveis; não mantenha seções vazias sem explicação.

## Imagens

Em um protocolo dentro de `equipment/<system>/protocols/`, utilize caminhos relativos:

```markdown
![Legenda descritiva.](../assets/common/nome-da-imagem.png){#fig-nome-da-imagem width=85%}
```

Utilize:

- `assets/common/` para fotografias e figuras usadas nos dois idiomas;
- `assets/en/` para gráficos que contenham texto em inglês;
- `assets/pt-BR/` para gráficos que contenham texto em português.

Use nomes em minúsculas, separados por hífens, e registre origem e licença em `assets/IMAGE_CREDITS.md`.

## Geração de PDF

Quando as configurações Pandoc do repositório estiverem prontas, execute a partir da raiz:

```bash
pandoc --defaults templates/defaults-en.yaml \
  equipment/<system>/protocols/protocol-name.md \
  -o protocol-name-en.pdf
```

```bash
pandoc --defaults templates/defaults-pt-BR.yaml \
  equipment/<system>/protocols/protocol-name.pt-BR.md \
  -o protocol-name-pt-BR.pdf
```

Os PDFs gerados são artefatos de publicação e normalmente não devem ser versionados junto às fontes Markdown.

## Aprovação

Somente protocolos explicitamente identificados como `Approved` são procedimentos autorizados pelo LAM+. As revisões técnica, de segurança e bilíngue devem estar concluídas antes da alteração do status.

