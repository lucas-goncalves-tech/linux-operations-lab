# Issue #11 — Diagnosticar conectividade e portas de rede

**Labels:** `phase: operations`, `priority: high`, `type: practical`
**Dependência:** #10

## Contexto
A aplicação pode estar ativa e ainda assim inacessível por causa de DNS, rota, porta, bind address ou firewall.

## Objetivo
Construir um procedimento de diagnóstico de rede do host.

## Tarefas
- [ ] Inspecionar interfaces com `ip link` e `ip -brief address`.
- [ ] Inspecionar rotas com `ip route`.
- [ ] Consultar DNS com `resolvectl` e `getent hosts`.
- [ ] Inspecionar sockets com `ss -tulpn` (usar sudo quando necessário).
- [ ] Testar HTTP/HTTPS com `curl -I` contra um endereço conhecido.
- [ ] Diferenciar `localhost`, `127.0.0.1`, IP da interface e `0.0.0.0`.
- [ ] Identificar a porta SSH em escuta e o processo associado.
- [ ] Fazer um teste local com `python3 -m http.server` em porta alta e encerrá-lo depois.
- [ ] Diagnosticar por que o servidor de teste pode ou não ser alcançado a partir do Windows.
- [ ] Documentar fluxo de diagnóstico em `runbooks/network-troubleshooting.md`.

## Conceitos que você deve compreender
TCP/UDP, socket, porta, DNS, rota, loopback, bind address, ICMP e HTTP.

## Critérios de aceitação
- [ ] Você identifica IP, rota, DNS e portas em escuta.
- [ ] Consegue explicar por que um serviço escutando em `127.0.0.1` não é acessível pela LAN.
- [ ] O servidor HTTP temporário foi encerrado.
- [ ] Runbook cobre camadas de diagnóstico sem depender de uma única ferramenta.

## Evidências
Saídas de `ip route`, `ss -tulpn`, `getent hosts` e `curl`.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
