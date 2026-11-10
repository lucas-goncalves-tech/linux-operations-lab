# Issue #12 — Configurar UFW sem perder o acesso SSH

**Labels:** `phase: security`, `priority: high`, `type: practical`
**Dependência:** #11

## Contexto
O firewall limita conexões de entrada. Uma regra incorreta pode bloquear seu próprio acesso remoto.

## Objetivo
Aplicar política de entrada restritiva, preservando SSH a partir da rede local.

## Pré-requisitos críticos
Mantenha o console VMware aberto. Confirme o IP/sub-rede local e faça snapshot. Não prossiga se SSH ainda não estiver estável.

## Tarefas
- [ ] Verificar se UFW está instalado e consultar `sudo ufw status verbose`.
- [ ] Antes de habilitar UFW, permitir OpenSSH com `sudo ufw allow OpenSSH`.
- [ ] Definir política padrão de entrada como deny e saída como allow.
- [ ] Habilitar UFW.
- [ ] Abrir uma NOVA sessão SSH a partir do Windows.
- [ ] Consultar regras numeradas e explicar cada uma.
- [ ] Executar teste de porta com `ss` no servidor e `Test-NetConnection <IP> -Port 22` no Windows.
- [ ] Remover qualquer regra temporária desnecessária.
- [ ] Documentar como recuperar acesso pelo console VMware em `runbooks/firewall-recovery.md`.

## Conceitos que você deve compreender
Firewall stateful, tráfego de entrada/saída, política default, regra, porta e origem.

## Critérios de aceitação
- [ ] UFW está ativo.
- [ ] Política de entrada é restritiva.
- [ ] SSH continua acessível do Windows.
- [ ] Nenhuma porta desnecessária está aberta.
- [ ] Procedimento de recuperação está documentado.

## Evidências
`sudo ufw status numbered`, `sudo ufw status verbose` e teste de conexão do Windows.

## Segurança
Não permita SSH de qualquer origem se puder restringir à sua LAN. Não altere regras remotamente sem console/snapshot disponíveis.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
