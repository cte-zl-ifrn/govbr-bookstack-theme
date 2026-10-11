# Tema gov.br para BookStack

Tema para aplicar o [Design System do governo federal](https://www.gov.br/ds/home) ao BookStack, destinado ao portal [Ajuda do IFRN](https://ajuda.ead.ifrn.edu.br/).

## Escopo

- Definir como aplicar o design system gov.br às telas do BookStack que forem incluídas na especificação.
- Implementar os templates, estilos e recursos necessários ao tema.
- Verificar acessibilidade, navegação por teclado e apresentação em diferentes tamanhos de tela.
- Documentar instalação do tema, versões compatíveis do BookStack e validação durante atualizações.

O tema é uma customização separada que utiliza o BookStack original. Consulte a [documentação de customização do BookStack](https://www.bookstackapp.com/docs/admin/hacking-bookstack/).

## Relação com a migração do Ajuda

O projeto [Migração do portal de ajuda](https://github.com/orgs/cte-zl-ifrn/projects/11) acompanha um trabalho mais amplo:

- Instalar e configurar o BookStack.
- Aplicar este tema.
- Migrar artigos, categorias e recursos do WordPress, com acesso ao banco de produção.
- Publicar o serviço em `ajuda.ead.ifrn.edu.br`.
- Encaminhar paths existentes para os artigos ou categorias correspondentes após a migração.

As issues deste repositório tratam do tema.

## Referência da POC

A [POC BookStack + H5P](https://github.com/cte-zl-ifrn/poc-bookstack-h5p) reúne experimentos e evidências que fundamentam este trabalho.

## Planejamento e contribuição

As [issues](https://github.com/cte-zl-ifrn/govbr-bookstack-theme/issues) são acompanhadas no projeto [Migração do portal de ajuda](https://github.com/orgs/cte-zl-ifrn/projects/11).

Para planejar entregas, use o fluxo `grill-with-docs` → `to-spec` → `to-tickets`: decisões, especificação e tickets de implementação.

- [AGENTS.md](AGENTS.md): instruções para agentes.
- [Rastreador e Project](docs/agents/issue-tracker.md): publicação e acompanhamento de issues.
- [Labels de triagem](docs/agents/triage-labels.md): vocabulário de classificação.
- [Documentação de domínio](docs/agents/domain.md): convenções para `CONTEXT.md` e ADRs.
