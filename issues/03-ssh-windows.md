# Issue #03 — Acessar o Ubuntu pelo Windows usando SSH

**Labels:** `phase: foundation`, `priority: high`, `type: practical`
**Dependência:** #02

## Contexto
Uma VPS é administrada remotamente. A partir daqui, use o Windows como estação de administração e o Ubuntu como servidor.

## Objetivo
Estabelecer conexão SSH do Windows PowerShell para a VM Ubuntu.

## Tarefas
- [ ] No Ubuntu, verificar `systemctl status ssh`; se necessário, instalar `openssh-server` com `sudo apt install openssh-server`.
- [ ] Confirmar que o serviço está ativo com `sudo systemctl enable --now ssh`.
- [ ] No Windows PowerShell, verificar `ssh -V`.
- [ ] Conectar com `ssh <usuario>@<IP_DA_VM>`.
- [ ] Confirmar a identidade do host na primeira conexão e entender o arquivo `known_hosts`.
- [ ] Abrir uma segunda sessão SSH para provar que múltiplas sessões funcionam.
- [ ] Executar remotamente `hostname`, `whoami`, `uptime` e `ip -brief address`.
- [ ] Registrar como reconectar após reiniciar a VM.

## Conceitos que você deve compreender
Cliente/servidor SSH, porta TCP 22, autenticação, host key, `known_hosts`, daemon e sessão remota.

## Critérios de aceitação
- [ ] Conexão SSH funciona a partir do Windows.
- [ ] O usuário remoto é o usuário pessoal, não `root`.
- [ ] Duas sessões SSH simultâneas funcionam.
- [ ] Após reiniciar a VM, SSH volta a funcionar.
- [ ] `docs/ssh-access.md` explica como conectar e como encontrar o IP.

## Evidências
Captura do PowerShell conectado (sem expor dados pessoais) e saída de `systemctl status ssh`.

## Não faça
Ainda não desabilite autenticação por senha. Ainda não habilite firewall. Mantenha o console VMware disponível.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
