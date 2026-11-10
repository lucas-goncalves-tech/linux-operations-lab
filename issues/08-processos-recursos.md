# Issue #08 — Inspecionar processos e consumo de recursos

**Labels:** `phase: operations`, `priority: medium`, `type: practical`
**Dependência:** #07

## Contexto
Um servidor pode ficar lento por consumo de CPU, memória, disco ou por processos travados.

## Objetivo
Identificar processos, sinais, consumo de recursos e limites básicos.

## Tarefas
- [ ] Inspecionar processos com `ps aux`, `ps -ef` e `pgrep`.
- [ ] Acompanhar consumo com `top` ou `htop`.
- [ ] Consultar memória com `free -h`.
- [ ] Consultar espaço e inodes com `df -h` e `df -i`.
- [ ] Inspecionar diretórios grandes com `du -xhd1 /var` e `du -xhd1 /home` (ajustar sintaxe se necessário).
- [ ] Iniciar um processo de teste inofensivo e encerrá-lo com `kill` usando seu PID.
- [ ] Diferenciar sinais SIGTERM e SIGKILL; usar SIGKILL apenas quando necessário.
- [ ] Consultar uptime e carga com `uptime`.
- [ ] Registrar um pequeno diagnóstico de saúde em `docs/resource-baseline.md`.

## Conceitos que você deve compreender
PID, PPID, processo, thread, sinal, CPU, RAM, swap, load average, filesystem e inode.

## Critérios de aceitação
- [ ] Você identifica o processo que mais consome CPU e memória.
- [ ] Consegue encerrar um processo de teste de forma controlada.
- [ ] Distingue falta de espaço de falta de inodes.
- [ ] Baseline de recursos documentado.

## Evidências
Saídas de `ps`, `free -h`, `df -h`, `df -i` e `uptime`.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
