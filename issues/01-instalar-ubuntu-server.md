# Issue #01 — Criar e instalar a VM Ubuntu Server

**Labels:** `phase: foundation`, `priority: high`, `type: practical`
**Dependência:** #00

## Contexto
Você já tem o VMware Workstation Pro 17 e uma VM CentOS. Agora criará uma VM separada, que representará o servidor Linux principal.

## Objetivo
Instalar Ubuntu Server 24.04 LTS em uma VM limpa e garantir que ela inicialize corretamente.

## Pré-requisitos
Issue #00 concluída. ISO oficial do Ubuntu Server 24.04 LTS baixada do site ubuntu.com.

## Tarefas
- [ ] Criar uma VM nova no VMware; não reutilizar o disco da VM CentOS.
- [ ] Selecionar Linux / Ubuntu 64-bit.
- [ ] Configurar CPU, RAM e disco conforme o inventário; usar disco virtual único, expansível (thin).
- [ ] Nomear a VM `ubuntu-vps-lab`.
- [ ] Instalar Ubuntu Server com OpenSSH Server selecionado durante a instalação, se a opção estiver disponível.
- [ ] Criar um usuário administrativo pessoal; não usar `root` como conta de trabalho.
- [ ] Definir hostname `ubuntu-vps-lab`.
- [ ] Usar particionamento guiado no disco virtual vazio da VM.
- [ ] Remover a ISO virtual após a instalação e reiniciar.
- [ ] Fazer login pelo console VMware e registrar versão do sistema com `cat /etc/os-release`.

## Conceitos que você deve compreender
ISO, boot, particionamento guiado, hostname, usuário inicial, LTS, console da VM e snapshot.

## Critérios de aceitação
- [ ] A VM inicia sem depender da ISO.
- [ ] É possível entrar com o usuário criado.
- [ ] `hostnamectl` mostra `ubuntu-vps-lab`.
- [ ] `cat /etc/os-release` confirma Ubuntu 24.04 LTS.
- [ ] `ip -brief address` mostra as interfaces de rede, mesmo que a rede ainda não esteja validada.
- [ ] Snapshot VMware `01-clean-install` criado.

## Evidências
Salvar a saída dos comandos de identificação do sistema em `evidence/01-install.txt`.

## Não faça
Não instale interface gráfica. Não use o disco da VM CentOS. Não configure serviços adicionais.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
