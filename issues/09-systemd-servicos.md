# Issue #09 — Gerenciar serviços com systemd

**Labels:** `phase: operations`, `priority: high`, `type: practical`
**Dependência:** #08

## Contexto
Serviços de servidor precisam iniciar, parar, reiniciar e subir automaticamente após reboot.

## Objetivo
Administrar serviços existentes e criar um serviço systemd simples para um script próprio.

## Tarefas
- [ ] Inspecionar `systemctl status ssh`.
- [ ] Usar `systemctl is-enabled`, `start`, `stop`, `restart` e `reload` quando suportado.
- [ ] Diferenciar serviço ativo de serviço habilitado no boot.
- [ ] Criar um script simples `/opt/lab/scripts/heartbeat.sh` que grave data/hora em `/var/log/lab-heartbeat.log` ou em diretório de log controlado.
- [ ] Criar uma unit `lab-heartbeat.service` do tipo `oneshot` ou serviço apropriado, com usuário e caminhos explícitos.
- [ ] Executar `systemd-analyze verify` na unit.
- [ ] Habilitar e iniciar o serviço conforme o tipo escolhido.
- [ ] Reiniciar a VM e verificar o comportamento.
- [ ] Documentar unit, dependências e comandos de operação em `docs/systemd-services.md`.

## Conceitos que você deve compreender
systemd, unit, service, target, daemon, enable, start, restart, status, exit code e dependência de serviço.

## Critérios de aceitação
- [ ] Unit passa na validação.
- [ ] Serviço executa a tarefa esperada.
- [ ] Logs do serviço podem ser consultados.
- [ ] Comportamento após reboot está documentado e validado.
- [ ] SSH continua operacional.

## Evidências
Arquivo unit, saída de `systemctl status lab-heartbeat` e `systemctl is-enabled lab-heartbeat`.

## Segurança
Não execute o serviço como root se ele não precisar de privilégios. Restrinja permissões do script e dos arquivos de log.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
