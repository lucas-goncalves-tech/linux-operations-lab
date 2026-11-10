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
- [x] Criar uma VM nova no VMware; não reutilizar o disco da VM CentOS.
- [x] Selecionar Linux / Ubuntu 64-bit.
- [x] Configurar CPU, RAM e disco conforme o inventário; usar disco virtual único, expansível (thin).
- [x] Nomear a VM `ubuntu-vps-lab`.
- [x] Instalar Ubuntu Server com OpenSSH Server selecionado durante a instalação, se a opção estiver disponível.
- [x] Criar um usuário administrativo pessoal; não usar `root` como conta de trabalho.
- [x] Definir hostname `ubuntu-vps-lab`.
- [x] Usar particionamento guiado no disco virtual vazio da VM.
- [x] Remover a ISO virtual após a instalação e reiniciar.
- [x] Fazer login pelo console VMware e registrar versão do sistema com `cat /etc/os-release`.

## Conceitos que você deve compreender
ISO, boot, particionamento guiado, hostname, usuário inicial, LTS, console da VM e snapshot.

## Critérios de aceitação
- [x] A VM inicia sem depender da ISO.
- [x] É possível entrar com o usuário criado.
- [x] `hostnamectl` mostra `ubuntu-vps-lab`.
- [x] `cat /etc/os-release` confirma Ubuntu 24.04 LTS.
- [x] `ip -brief address` mostra as interfaces de rede, mesmo que a rede ainda não esteja validada.
- [x] Snapshot VMware `01-clean-install` criado.

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
