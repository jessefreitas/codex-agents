# codex.md

## Objetivo
Padronizar como o Codex deve operar em projetos novos e existentes, com melhoria continua baseada em erros reais.

## Principios
- Clareza: explicar decisao, impacto e proximo passo.
- Rastreabilidade: toda mudanca relevante precisa ficar registrada em arquivo versionado.
- Entrega incremental: preferir lotes pequenos e verificaveis.
- Seguranca: nunca persistir segredo em repositorio.

## Regra de Aprendizado Continuo
Para cada erro, regressao ou retrabalho, executar este ciclo:
1. Registrar o erro em `ERRORS.md` (data, contexto, causa raiz, impacto).
2. Definir prevencao objetiva (teste, check, regra, automacao).
3. Atualizar `MEMORY.md` com a nova regra operacional.
4. Aplicar a correcao no processo (script, checklist ou template).
5. Validar com evidencia (saida de comando, teste, diff, PR).

## Estrutura de Memoria Recomendada
- `codex.md`: regra mestra de operacao.
- `MEMORY.md`: decisoes e aprendizados consolidados.
- `ERRORS.md`: incidentes e licoes aprendidas.
- `CODEX.local.md`: notas locais nao versionadas.

## Checklists Obrigatorios

### Antes de editar
- Confirmar escopo e arquivos alvo.
- Verificar estado Git (`git status -sb`).
- Identificar risco de quebrar comportamento existente.

### Antes de commit
- Revisar diff.
- Executar validacoes aplicaveis (lint/testes).
- Garantir ausencia de segredos.
- Atualizar docs afetadas.

### Antes de push
- Commit semantico e objetivo.
- Branch/PR com contexto, impacto e riscos.
- Confirmar que o estado local esta limpo apos commit.

## Padrao de Projeto Novo (Bootstrap)
Comando unico esperado:
- `C:\Github\codex-new.cmd <nome-projeto>`

Variantes:
- `C:\Github\codex-new.cmd <nome-projeto> local prod`
- `C:\Github\codex-new.cmd <nome-projeto> local incubacao -GitInit`
- `C:\Github\codex-new.cmd <nome-projeto> vps`

## Politica de Seguranca
- Credenciais, tokens e senhas nunca entram em Git.
- Se um segredo aparecer em conversa ou arquivo: considerar comprometido e rotacionar.
- Usar placeholders em documentacao (`<SECRET>`, `<TOKEN>`).

## Definicao de Pronto
Uma entrega so esta pronta quando:
- codigo/documentacao aplicados;
- validacao executada;
- aprendizado relevante registrado em memoria;
- commit e push concluidos.
