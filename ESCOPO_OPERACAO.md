# Escopo de Trabalho - Operacao do Repositorio `codex-agents`

## Objetivo
Definir como vamos operar neste GitHub para manter consistencia, rastreabilidade e qualidade nas entregas.

## Escopo
- Estruturar e evoluir agentes, skills e automacoes relacionadas ao projeto.
- Padronizar fluxo de desenvolvimento (branch, commit, PR e revisao).
- Garantir que cada mudanca tenha contexto tecnico e validacao minima.

## Estrutura Inicial Recomendada
- `README.md`: visao geral do projeto e onboarding.
- `docs/`: documentacao funcional e tecnica.
- `agents/`: implementacoes de agentes.
- `skills/`: definicoes e instrucoes de skills.
- `scripts/`: utilitarios de automacao e manutencao.
- `tests/`: testes automatizados.

## Fluxo de Trabalho (GitHub)
1. Criar branch a partir de `main`.
2. Implementar mudanca pequena e objetiva.
3. Rodar validacoes locais (lint/testes aplicaveis).
4. Commit com mensagem clara.
5. Abrir PR com contexto, impacto e evidencias.
6. Revisar, ajustar e realizar merge.

## Convencoes
- Branch: `feat/<tema>`, `fix/<tema>`, `chore/<tema>`, `docs/<tema>`.
- Commits: padrao semantico (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`).
- PR: incluir objetivo, mudancas principais, riscos e plano de rollback (quando necessario).

## Criterios Minimos de Qualidade
- Nao quebrar comportamento existente sem justificativa.
- Atualizar documentacao quando houver mudanca de fluxo.
- Incluir testes para regra critica ou bug corrigido.
- Evitar segredos no codigo e no historico Git.

## Operacao Diaria
- Sincronizar com `main` antes de iniciar tarefa.
- Trabalhar em lotes pequenos para facilitar revisao.
- Priorizar correcoes de alto impacto primeiro.
- Registrar decisoes tecnicas em `docs/decisoes/` (ADR) quando houver trade-off relevante.

## Backlog Inicial Sugerido
1. Criar `README.md` com visao do projeto e setup.
2. Criar estrutura de pastas base (`docs`, `agents`, `skills`, `tests`, `scripts`).
3. Definir pipeline CI (lint + testes).
4. Configurar templates de Issue e PR.
5. Definir politica de revisao e branch protection.

## Definicao de Pronto (DoD)
- Codigo implementado e revisado.
- Testes relevantes passando.
- Documentacao atualizada.
- PR aprovado e mergeado em `main`.

## Responsabilidade
Este documento e o ponto de referencia para o nosso modo de operacao neste repositorio. Ajustes devem ser versionados via PR.
