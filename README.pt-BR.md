# LAM+ — Protocolos laboratoriais

[English](README.md)

Repositório público e aberto dos protocolos operacionais do Laboratório Multiusuário LAM+, Universidade Federal Fluminense (UFF). O Markdown é a fonte editável e versionada. Estes são protocolos do LAM+, não cópias de manuais de fabricantes.

Este repositório inicial contém a estrutura documental; ainda não há protocolos operacionais aprovados.

## Sistemas

- [Sistema de varredura hiperespectral (HSI)](equipment/hsi-scanning-system/README.pt-BR.md)
- [Avaatech XRF Core Scanner](equipment/avaatech-xrf-core-scanner/README.pt-BR.md)
- [MEV–EDS](equipment/mev-eds/README.pt-BR.md)

## Fluxo de publicação

Markdown → Pandoc → PDF → GitHub Release → Zenodo. Antes de uma publicação formal: concluir a revisão técnica, sincronizar os idiomas, validar links e imagens, gerar e inspecionar ambos os PDFs, atualizar históricos e confirmar metadados de citação e arquivamento. PDFs são artefatos de publicação; não devem ser adicionados às pastas de fontes.

As versões em inglês e português brasileiro têm igual status documental e compartilham identificador, versão, data e conteúdo técnico.

## Modelos e geração de PDF

[Modelo de protocolo](templates/protocol-template.pt-BR.md) · [AGENTS.md](AGENTS.md)

Execute na raiz do repositório. Testado com Pandoc 3.9 e XeLaTeX. Dependências: Pandoc 3.9 ou posterior e XeLaTeX, com os pacotes TeX fontspec, polyglossia (inglês e português), geometry, graphicx, longtable, booktabs, array, calc, etoolbox, amsmath, amssymb, xcolor e hyperref. Não é necessário pandoc-crossref. O realce de sintaxe está desativado. Figuras com legendas e tabelas usam os recursos nativos do Pandoc; referências automáticas cruzadas não estão configuradas.

```sh
pandoc --defaults=templates/defaults-en.yaml templates/protocol-template.md -o /tmp/lam-template-en.pdf
pandoc --defaults=templates/defaults-pt-BR.yaml templates/protocol-template.pt-BR.md -o /tmp/lam-template-pt-BR.pdf
```

Para protocolos reais, acrescente `--resource-path=.:equipment/<system>/protocols` ao comando para resolver imagens relativas ao protocolo. Substitua os marcadores antes da revisão; a data do modelo é apenas a data de criação da estrutura, não uma data de publicação.

## Licença e metadados

A documentação e as figuras originais de protocolos usam CC BY 4.0; a licença de software, automação e modelos LaTeX permanece a definir. Marcas institucionais e materiais de terceiros exigem autorização própria. Consulte [LICENSE](LICENSE).

[CITATION.cff](CITATION.cff) · [.zenodo.json](.zenodo.json) · [CHANGELOG.md](CHANGELOG.md)

TODO: confirmar responsáveis pela autoria/citação, revisores, metadados da publicação e licença de software. Nenhum DOI ou data de publicação foi atribuído. Não publicar os metadados provisórios no Zenodo.
