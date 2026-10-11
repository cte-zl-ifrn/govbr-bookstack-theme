# Issue tracker: GitHub

## Destino

Especificações e tickets deste repositório são GitHub Issues em [cte-zl-ifrn/govbr-bookstack-theme](https://github.com/cte-zl-ifrn/govbr-bookstack-theme/issues). Use o CLI `gh` para consultar e publicar.

O projeto de acompanhamento é [Migração do portal de ajuda](https://github.com/orgs/cte-zl-ifrn/projects/11), da organização `cte-zl-ifrn`, número `11`. Uma issue pertence ao repositório; sua inclusão no Project é uma operação adicional.

## Operações

Execute os comandos dentro do clone deste repositório; o `gh` identifica o destino pelo remote. Fora dele, use `--repo cte-zl-ifrn/govbr-bookstack-theme`.

- Criar: `gh issue create --title "Título" --body-file /caminho/issue.md`.
- Ler: `gh issue view NUMERO --comments`.
- Listar: `gh issue list --state open --json number,title,body,labels,assignees`; filtre por label conforme a tarefa.
- Comentar: `gh issue comment NUMERO --body-file /caminho/comentario.md`.
- Aplicar ou remover labels: `gh issue edit NUMERO --add-label LABEL` ou `--remove-label LABEL`.
- Encerrar: `gh issue close NUMERO`, após registrar o resultado na issue.

Para textos com várias linhas, escreva o conteúdo em arquivo e use `--body-file`.

## Publicação de especificações e tickets

Quando uma skill pedir publicação no rastreador:

1. Publique uma issue neste repositório, com os labels definidos em [triage-labels.md](triage-labels.md). Siga a etapa de revisão prevista na skill utilizada.
2. Adicione a issue ao Project: `gh project item-add 11 --owner cte-zl-ifrn --url URL_DA_ISSUE`.
3. Registre os vínculos de dependência após criar as issues, quando seus identificadores estiverem disponíveis.

O acesso via `gh` ao Project exige permissões próprias de Projects: `read:project` para consulta e `project` para escrita em tokens clássicos. Se o acesso estiver indisponível, preserve a issue criada, informe o vínculo pendente e conclua a associação quando o acesso estiver disponível. Uma issue publicada e uma issue adicionada ao Project são resultados distintos.

## Pull requests como entrada de triagem

**PRs as a request surface: no.** Pull requests externas não entram automaticamente no fluxo de triagem de solicitações.

Issues e pull requests compartilham a numeração do repositório. Confira o tipo do item ao receber apenas um número.

## Wayfinding operations

Use estas convenções quando `wayfinder` for explicitamente invocada:

- O mapa é uma issue com label `wayfinder:map`.
- Tickets de decisão são sub-issues do mapa, com label `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling` ou `wayfinder:task`, conforme o tipo. Crie esses labels apenas quando o fluxo precisar deles.
- Use a API de sub-issues do GitHub para os vínculos. Se ela estiver indisponível, mantenha uma lista de tickets no mapa e um link para o mapa em cada ticket.
- Registre bloqueios usando as dependências nativas do GitHub. Obtenha o ID numérico do bloqueador com `gh api repos/OWNER/REPO/issues/NUMERO --jq .id` e adicione-o ao ticket com `gh api --method POST repos/OWNER/REPO/issues/TICKET/dependencies/blocked_by -F issue_id=ID_DO_BLOQUEADOR`. Esse ID é o ID de banco de dados, diferente do número da issue e de `node_id`.
- Se as dependências nativas estiverem indisponíveis, registre links em uma seção `Blocked by` do ticket.
- A fronteira contém tickets abertos, sem responsável e cujos bloqueadores estão encerrados. Use as sub-issues do mapa e os vínculos de dependência para encontrá-los.
- Reivindique um ticket com `gh issue edit NUMERO --add-assignee @me` antes de trabalhá-lo.
- Para resolver, comente o resultado, encerre o ticket e acrescente ao mapa um link com uma frase sobre a decisão.
