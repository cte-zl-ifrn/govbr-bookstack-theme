# Tema gov.br para BookStack

Tema para aplicar o [Design System do governo federal](https://www.gov.br/ds/home) ao BookStack que substituirá o WordPress no portal [Ajuda do IFRN](https://ajuda.ead.ifrn.edu.br/).

## Estado atual

O repositório está na etapa inicial de planejamento. Contém o README e a configuração das skills de engenharia; o tema ainda será especificado e implementado.

A [POC BookStack + H5P](https://github.com/cte-zl-ifrn/poc-bookstack-h5p) é a referência de experimentação. Suas customizações e evidências servem de entrada para o trabalho; a adoção do design system gov.br faz parte desta nova etapa.

## Escopo

- Definir como aplicar o design system gov.br às telas do BookStack que forem incluídas na especificação.
- Implementar os templates, estilos e recursos necessários ao tema.
- Verificar acessibilidade, navegação por teclado e apresentação em diferentes tamanhos de tela.
- Documentar instalação do tema, versões compatíveis do BookStack e validação durante atualizações.

O tema será desenvolvido como uma customização separada, consumindo o BookStack original. O mecanismo e a extensão dos overrides serão definidos durante a especificação. Consulte a [documentação de customização do BookStack](https://www.bookstackapp.com/docs/admin/hacking-bookstack/).

## Relação com a migração do Ajuda

O projeto [Migração do portal de ajuda](https://github.com/orgs/cte-zl-ifrn/projects/11) acompanha um trabalho mais amplo:

- Instalar e configurar o BookStack na VM já disponível.
- Aplicar este tema.
- Migrar artigos, categorias e recursos do WordPress, com acesso ao banco de produção.
- Publicar o serviço em `ajuda.ead.ifrn.edu.br`.
- Encaminhar paths existentes para os artigos ou categorias correspondentes após a migração.

As issues deste repositório tratam do tema. A organização dos artefatos de migração e operação será definida conforme a necessidade. A criação de um repositório `ajuda-bookstack` foi adiada até que sua necessidade seja demonstrada.

## Planejamento e contribuição

As [issues](https://github.com/cte-zl-ifrn/govbr-bookstack-theme/issues) são acompanhadas no projeto [Migração do portal de ajuda](https://github.com/orgs/cte-zl-ifrn/projects/11).

O fluxo previsto é `grill-with-docs` → `to-spec` → `to-tickets`. Ele deve definir as decisões, a especificação e as entregas antes da implementação.

- [AGENTS.md](AGENTS.md): instruções para agentes.
- [Rastreador e Project](docs/agents/issue-tracker.md): publicação e acompanhamento de issues.
- [Labels de triagem](docs/agents/triage-labels.md): vocabulário de classificação.
- [Documentação de domínio](docs/agents/domain.md): convenções para `CONTEXT.md` e ADRs.

As instruções de desenvolvimento, instalação e testes serão acrescentadas junto da primeira implementação.
