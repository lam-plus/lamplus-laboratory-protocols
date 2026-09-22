<p align="center">
  <img src="assets/branding/logo-lamplus-transparent.png" alt="Logotipo do LAM+" width="280">
</p>

# Protocolos do Laboratório LAM+

[English](README.md) | [Português](README.pt-BR.md)

Este repositório reúne os protocolos operacionais públicos e versionados do **Laboratório Multiusuário LAM+** da **Universidade Federal Fluminense (UFF), Brasil**.

O projeto disponibiliza orientações claras, reprodutíveis e abertamente acessíveis para a operação dos sistemas analíticos do LAM+. Os protocolos são mantidos como documentos Markdown bilíngues, em inglês e português brasileiro, e preparados para gerar documentos PDF padronizados por meio do Pandoc.

## Escopo atual

O repositório contempla atualmente três sistemas laboratoriais:

| Sistema | Descrição | Situação do protocolo |
|---|---|---|
| [Sistema de escaneamento HSI](equipment/hsi-scanning-system/) | Sistema integrado de escaneamento hiperespectral, incluindo câmeras, iluminação, estágio de translação, alvos de referência, software de controle, calibração, aquisição e tratamento dos dados | Desenvolvimento ainda não iniciado |
| [Avaatech XRF Core Scanner](equipment/avaatech-xrf-core-scanner/) | Sistema de escaneamento de testemunhos por fluorescência de raios X | Protocolo existente em Word aguardando migração para Markdown |
| [MEV–EDS](equipment/mev-eds/) | Microscopia eletrônica de varredura com espectroscopia de raios X por dispersão em energia | Desenvolvimento ainda não iniciado |

Outros equipamentos poderão ser incorporados depois que seu escopo, suas necessidades documentais e suas responsabilidades técnicas estiverem definidos.

## Fluxo da documentação

Os arquivos Markdown são as fontes editáveis oficiais. O fluxo de publicação previsto é:

```text
Markdown → revisão técnica → PDF com Pandoc → GitHub Release → Zenodo
```

As versões em inglês e português do mesmo protocolo compartilham o mesmo identificador, versão, situação de aprovação e conteúdo técnico. Os PDFs são produtos gerados e não devem ser editados diretamente.

As versões publicadas serão arquivadas no **Zenodo**, proporcionando acesso permanente e registros citáveis. A primeira publicação no Zenodo ainda não foi realizada e será anunciada neste documento quando estiver disponível.

## Organização do repositório

```text
equipment/              Protocolos e imagens específicos dos equipamentos
templates/              Templates bilíngues para Markdown e Pandoc
assets/branding/        Identidade visual do LAM+ e institucional
TODO.md                 Roteiro de desenvolvimento e publicação
CHANGELOG.md            Alterações incorporadas às versões do repositório
AGENTS.md               Instruções do repositório para agentes de programação
```

As imagens específicas dos equipamentos ficam armazenadas junto ao respectivo sistema. Os elementos compartilhados de identidade visual ficam em `assets/branding/`.

## Protocolos e manuais dos fabricantes

Estes documentos são **protocolos operacionais do LAM+**, desenvolvidos para os sistemas instalados e utilizados no laboratório. Eles não são cópias nem substitutos dos manuais dos fabricantes.

A documentação dos fabricantes permanece como referência técnica importante. Os usuários devem consultar as instruções aplicáveis sempre que necessário, especialmente para limites de segurança, manutenção, atividades regulamentadas e procedimentos que não estejam contemplados em um protocolo do LAM+.

## Como contribuir

Sugestões, correções, traduções e aperfeiçoamentos técnicos são bem-vindos por meio de issues e pull requests no GitHub.

O acesso público não significa que as alterações propostas serão aceitas automaticamente. Mudanças que afetem procedimentos operacionais, calibração, segurança, configurações instrumentais ou critérios de controle de qualidade precisam ser avaliadas pelos responsáveis técnicos do LAM+ antes da aprovação.

Antes de contribuir:

1. consulte o diretório do equipamento e o arquivo `TODO.md`;
2. preserve a organização bilíngue;
3. utilize caminhos relativos para imagens e links internos;
4. informe a origem e a licença das imagens adicionadas;
5. não inclua manuais proprietários, informações confidenciais, credenciais, dados pessoais ou configurações instrumentais não verificadas.

As orientações detalhadas para contribuição serão mantidas em `CONTRIBUTING.md`.

## Situação documental e segurança

Os protocolos podem ser identificados como `Draft`, `Under review`, `Approved`, `Superseded` ou `Retired`. Somente documentos explicitamente identificados como **Approved** devem ser considerados procedimentos operacionais autorizados pelo LAM+.

Os usuários continuam responsáveis por cumprir os requisitos de treinamento do laboratório, as normas institucionais de segurança, os requisitos de proteção radiológica, as instruções dos fabricantes e a regulamentação aplicável. Um protocolo público não substitui a autorização específica para uso do equipamento nem o treinamento supervisionado.

## Licença e atribuição

Salvo indicação em contrário, a documentação original dos protocolos será disponibilizada sob a licença **Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)**.

Nomes institucionais, logotipos e marcas não estão automaticamente abrangidos pela licença da documentação. Materiais de terceiros permanecem sujeitos aos respectivos direitos e condições de licenciamento.

As informações para citação serão disponibilizadas por meio do arquivo `CITATION.cff` e do futuro registro no Zenodo.

## Contato

Dúvidas, sugestões e solicitações de informações adicionais podem ser encaminhadas por meio do sistema de issues deste repositório no GitHub ou diretamente para:

- **Igor Venancio:** [ivenancio@id.uff.br](mailto:ivenancio@id.uff.br)
- **André Belém:** [andrebelem@id.uff.br](mailto:andrebelem@id.uff.br)

