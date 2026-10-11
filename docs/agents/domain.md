# Documentação de domínio

## Leitura durante a exploração

Este repositório usa um único contexto de domínio: `CONTEXT.md` na raiz e ADRs em `docs/adr/`.

Antes de explorar o código, leia `CONTEXT.md`, quando existir, e os ADRs relacionados à área de trabalho. Use o vocabulário do contexto em especificações, issues e código.

Esses documentos são criados conforme termos e decisões forem resolvidos por `domain-modeling`, normalmente através de `grill-with-docs`. Se ainda não existirem, prossiga com os documentos disponíveis.

## Registros de decisões

Crie `docs/adr/` quando houver a primeira decisão a registrar. Numere os ADRs sequencialmente: `0001-nome-da-decisao.md`.

Registre o contexto, a decisão e o motivo. Reserve ADRs para decisões com custo relevante de reversão, alternativas reais e justificativa que um futuro leitor precisará conhecer.

Ao propor algo que contradiga um ADR, indique o conflito e a justificativa para revisitar a decisão.
