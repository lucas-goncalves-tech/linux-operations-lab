# Issue #22 — Executar teste integrado de recuperação operacional

**Labels:** `phase: reliability`, `priority: high`, `type: practical`
**Dependência:** #21

## Contexto
Uma sequência de exercícios isolados não prova que você consegue operar o servidor. Agora será feito um teste integrado, com falhas controladas e recuperação documentada.

## Objetivo
Demonstrar que o servidor pode ser diagnosticado e recuperado usando os runbooks criados.

## Tarefas
- [ ] Criar snapshot VMware antes do teste.
- [ ] Confirmar backup recente e validar checksum.
- [ ] Executar checklist de pré-teste: SSH, UFW, Docker, aplicação, timer, disco e logs.
- [ ] Cenário A: parar a aplicação e diagnosticar pelo alerta/log seguindo `runbooks/monitoring-alerts.md`.
- [ ] Cenário B: interromper o serviço de heartbeat e recuperar via systemd.
- [ ] Cenário C: restaurar `/srv/lab-data/app` a partir do backup recente da Issue #20 em um caminho isolado e validar a integridade sem sobrescrever os dados em uso.
- [ ] Cenário D: simular regra UFW incorreta apenas com console aberto; recuperar acesso sem reinstalar a VM.
- [ ] Registrar timeline, comandos, evidências, causa e resultado de cada cenário.
- [ ] Reverter todas as falhas induzidas e confirmar estado saudável.
- [ ] Criar relatório `docs/final-recovery-test.md`.

## Conceitos que você deve compreender
Recovery, rollback, snapshot, backup, integridade, MTTR, validação pós-recuperação e mudança controlada.

## Critérios de aceitação
- [ ] Todos os cenários foram resolvidos.
- [ ] Aplicação e SSH estão funcionais ao final.
- [ ] UFW e serviços estão no estado esperado.
- [ ] Dados restaurados foram verificados.
- [ ] Relatório permite reproduzir o teste.

## Não faça
Não apague discos, não corrompa o filesystem e não simule falha física do host.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
