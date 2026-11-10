# Issue #15 — Agendar tarefas com cron e systemd timers

**Labels:** `phase: automation`, `priority: medium`, `type: practical`
**Dependência:** #14

## Contexto
Rotinas de manutenção precisam executar automaticamente e deixar rastros de execução.

## Objetivo
Agendar uma verificação de saúde e entender as diferenças entre cron e systemd timers.

## Tarefas
- [ ] Criar uma rotina que execute `server-health.sh` e grave log com timestamp.
- [ ] Configurar um cron job de usuário para executar a cada 5 minutos durante o laboratório.
- [ ] Verificar execução e logs; não presumir que cron herda o PATH do terminal.
- [ ] Remover o cron job de teste ao terminar.
- [ ] Criar uma unit service + timer do systemd para executar a mesma verificação.
- [ ] Consultar timer com `systemctl list-timers`.
- [ ] Comparar cron e systemd timer: logs, dependências, estado e calendário.
- [ ] Escolher uma solução final e documentar a justificativa.
- [ ] Garantir que os logs não cresçam indefinidamente; definir retenção simples ou encaminhar para journald.

## Conceitos que você deve compreender
Cron, crontab, systemd timer, calendário, PATH, execução não interativa e retenção de logs.

## Critérios de aceitação
- [ ] A rotina executa automaticamente e produz log.
- [ ] O agendamento foi validado observando pelo menos duas execuções.
- [ ] A tarefa de teste temporária foi removida.
- [ ] Existe documentação da solução escolhida e como desabilitá-la.

## Evidências
Trecho de log com horários distintos, `crontab -l` (se aplicável) e `systemctl list-timers`.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
