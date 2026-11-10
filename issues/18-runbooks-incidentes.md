# Issue #18 — Criar runbooks e resolver incidentes simulados

**Labels:** `phase: reliability`, `priority: high`, `type: practical`
**Dependência:** #17

## Contexto
Saber comandos isolados não basta. Um profissional de operações precisa diagnosticar sintomas de forma ordenada, registrar evidências e restaurar o serviço.

## Objetivo
Criar runbooks e resolver incidentes controlados no laboratório.

## Tarefas
- [ ] Criar modelo de incidente com: impacto, horário, sintomas, hipótese, evidências, causa raiz, mitigação, correção e prevenção.
- [ ] Criar runbook para SSH inacessível.
- [ ] Criar runbook para disco cheio.
- [ ] Criar runbook para serviço systemd falhando.
- [ ] Criar runbook para DNS ou rota indisponível.
- [ ] Simular serviço parado e recuperá-lo.
- [ ] Simular disco cheio de forma segura usando arquivo de teste limitado (não preencher o filesystem real).
- [ ] Simular falha de resolução DNS sem alterar permanentemente a configuração da rede; preferir teste isolado com `getent`/`resolvectl`.
- [ ] Resolver cada cenário seguindo o runbook, sem consultar um tutorial passo a passo.
- [ ] Registrar tempo até diagnóstico e recuperação, sem transformar isso em competição.

## Conceitos que você deve compreender
Incidente, sintoma, hipótese, causa raiz, mitigação, recuperação, runbook, impacto e pós-incidente.

## Critérios de aceitação
- [ ] Pelo menos três incidentes foram simulados e resolvidos.
- [ ] Cada incidente tem evidência antes/depois.
- [ ] Runbooks são executáveis por outra pessoa.
- [ ] Nenhuma simulação deixou o servidor indisponível.

## Evidências
`runbooks/` preenchido e relatórios em `evidence/incidents/`.

## Não faça
Não provoque indisponibilidade real de rede ou disco. Use somente cenários reversíveis e limitados.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
