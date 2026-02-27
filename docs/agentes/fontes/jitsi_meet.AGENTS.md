# AGENTS Guidelines - App `agents.md`

Este diretorio contem uma aplicacao Next.js. Para manter velocidade e previsibilidade no suporte por agente, siga estas regras.

## Objetivo
- Corrigir com o menor diff seguro.
- Manter HMR funcional durante desenvolvimento.
- Validar cada mudanca antes de concluir.

## Regras operacionais obrigatorias
1. Use `npm run dev` para iterar.
2. Nao rode `npm run build` durante sessao interativa de correcao.
3. Se dependencias mudarem, atualize lockfile e reinicie o dev server.
4. Nao misture refatoracao ampla em task de bugfix.

## Fluxo de trabalho (assertivo)
1. Diagnostico
- Reproduza o erro.
- Identifique arquivo e causa raiz antes de editar.

2. Correcao
- Patch minimo no ponto causal.
- Preserve comportamento existente fora do escopo.

3. Validacao
- Execute somente checks relevantes ao modulo alterado:
  - `npm run lint`
  - `npm run test` (se existir)
  - validacao manual da tela/fluxo afetado em `npm run dev`

4. Relatorio
- Liste arquivos alterados.
- Explique causa raiz e efeito do patch.
- Informe validacoes executadas.

## Definicao de pronto
- Causa raiz confirmada.
- Correcao aplicada.
- Validacao executada com resultado.
- Sem regressao obvia no fluxo alterado.

## Comandos de referencia
- `npm run dev`: desenvolvimento com HMR.
- `npm run lint`: analise estatica.
- `npm run test`: suite de testes.
- `npm run build`: somente fora da sessao interativa.
