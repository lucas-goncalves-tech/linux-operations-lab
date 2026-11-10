# Issue #21 — Implementar monitoramento básico e alertas locais

**Labels:** `phase: reliability`, `priority: medium`, `type: practical`
**Dependência:** #20

## Contexto
Operar um servidor exige perceber falhas antes ou no momento em que afetam o serviço.

## Objetivo
Criar verificações periódicas para disponibilidade da aplicação e saúde básica do host.

## Tarefas
- [ ] Definir sinais mínimos: aplicação responde HTTP, serviço/container está ativo, disco abaixo de limite de alerta e memória disponível.
- [ ] Estender `server-health.sh` com verificações e códigos de saída claros.
- [ ] Criar verificação HTTP com `curl` e timeout.
- [ ] Criar limiar de disco configurável, por exemplo 80%, explicando que é um valor de laboratório.
- [ ] Registrar resultados com timestamp sem gravar dados sensíveis.
- [ ] Agendar a verificação com systemd timer.
- [ ] Simular aplicação parada e confirmar que a verificação detecta a falha.
- [ ] Definir como consultar histórico e diferenciar alerta de incidente.
- [ ] Criar `runbooks/monitoring-alerts.md` com o procedimento para investigar alertas de aplicação/contêiner, disco e memória, incluindo consulta ao histórico, evidências e critérios para considerar o serviço recuperado.
- [ ] Documentar limitações: isso é monitoramento local, não um sistema externo de alertas.

## Conceitos que você deve compreender
Métrica, disponibilidade, health check, threshold, observabilidade, monitoramento, alerta e falso positivo.

## Critérios de aceitação
- [ ] Verificação detecta aplicação saudável.
- [ ] Verificação detecta aplicação indisponível.
- [ ] Limite de disco é configurável.
- [ ] Timer executa automaticamente.
- [ ] Runbook explica como investigar cada alerta.
- [ ] `runbooks/monitoring-alerts.md` cobre os sinais definidos e os comandos para verificar o estado após a correção.

## Evidências
Saída de uma execução saudável e outra com falha controlada; logs do timer.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
