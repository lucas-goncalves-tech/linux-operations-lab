# Issue #10 — Consultar logs e diagnosticar falhas

**Labels:** `phase: operations`, `priority: high`, `type: practical`
**Dependência:** #09

## Contexto
Quando um serviço falha, a mensagem de erro costuma estar nos logs. Saber localizá-los é uma habilidade operacional central.

## Objetivo
Investigar logs do sistema e do serviço criado na Issue anterior.

## Tarefas
- [ ] Consultar logs de boot com `journalctl -b`.
- [ ] Consultar logs de um serviço com `journalctl -u ssh` e `journalctl -u lab-heartbeat`.
- [ ] Filtrar por período com `--since` e `--until`.
- [ ] Acompanhar logs em tempo real com `journalctl -f`.
- [ ] Explorar `/var/log/auth.log`, `/var/log/syslog` e logs disponíveis na distribuição.
- [ ] Usar `grep`, `less`, `tail`, `head`, `cut` e `sort` em logs.
- [ ] Provocar uma falha controlada no script de laboratório (por exemplo, apontar temporariamente para um caminho inválido), observar o erro e restaurar a configuração.
- [ ] Registrar horário, sintoma, evidência, causa e correção em `runbooks/log-investigation.md`.

## Conceitos que você deve compreender
journald, syslog, log level, timestamp, rotação de logs, stdout/stderr e exit status.

## Critérios de aceitação
- [ ] Você encontra logs de SSH e do serviço próprio.
- [ ] Consegue filtrar por unidade e período.
- [ ] Identifica uma falha induzida e restaura o serviço.
- [ ] Runbook contém comandos e sequência de diagnóstico.

## Evidências
Trechos curtos e não sensíveis dos logs e registro da falha controlada.

## Não faça
Não publique logs que contenham IPs públicos, nomes de usuário pessoais, tokens ou dados privados.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
