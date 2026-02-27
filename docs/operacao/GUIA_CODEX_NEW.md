# Guia Operacional - codex-new

## Objetivo
Centralizar o fluxo de criacao de projetos com comando unico e comportamento previsivel.

## Comandos
- `C:\Github\codex-new.cmd <nome-projeto>`
- `C:\Github\codex-new.cmd <nome-projeto> local prod`
- `C:\Github\codex-new.cmd <nome-projeto> local incubacao -GitInit`
- `C:\Github\codex-new.cmd <nome-projeto> vps`

## Fluxo Local
1. Criar estrutura base do projeto.
2. Gerar arquivos de memoria (`codex.md`, `MEMORY.md`, `ERRORS.md`, `CODEX.local.md`).
3. Solicitar/configurar remoto GitHub.
4. Opcionalmente inicializar Git (`-GitInit`).

## Fluxo VPS
1. Solicitar dados de conexao e tipo de ambiente.
2. Executar hardening inicial (ufw, fail2ban, unattended-upgrades).
3. Ajustar SSH (porta final, bloqueio de root via SSH, firewall).
4. Criar usuarios administrativos e validar acesso.

## Validacoes Minimas
- Confirmar arquivos base criados.
- Confirmar status Git esperado.
- Confirmar servicos de seguranca ativos no modo VPS.
- Registrar resultado em memoria da sessao.

## Seguranca
- Nao registrar senha real em arquivo versionado.
- Qualquer credencial exposta deve ser rotacionada.
