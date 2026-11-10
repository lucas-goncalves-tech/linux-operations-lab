# Issue #00 — Planejar o laboratório e inventariar o computador

**Labels:** `phase: foundation`, `priority: medium`, `type: practical`
**Dependência:** Nenhuma

## Contexto
Antes de criar a VM, registre os recursos disponíveis no computador host. O objetivo é dimensionar o laboratório sem comprometer o Windows nem as VMs existentes.

## Objetivo
Definir os limites do laboratório, criar o repositório e registrar as decisões iniciais.

## Tarefas
- [ ] Criar o repositório GitHub `linux-operations-lab` (público ou privado).
- [ ] Criar as pastas `docs/`, `scripts/`, `evidence/` e `runbooks/`.
- [ ] Registrar no `docs/host-inventory.md`: versão do Windows, CPU, RAM total, espaço livre em disco e versão do VMware Workstation.
- [ ] Registrar se a virtualização por hardware está habilitada.
- [ ] Definir recursos iniciais da VM: 2 vCPU, 4 GB RAM e 40 GB de disco virtual thin provisioned. Ajustar para baixo se o host não suportar.
- [ ] Registrar a finalidade: VM Ubuntu será o servidor principal; CentOS existente permanece como laboratório secundário.
- [ ] Criar as labels do projeto conforme o README.

## Conceitos que você deve compreender
Hipervisor tipo 2, máquina host, máquina guest, vCPU, RAM alocada, disco virtual thin provisioned, snapshot e rede virtual.

## Critérios de aceitação
- [ ] Repositório criado com estrutura de pastas.
- [ ] Inventário do host documentado sem publicar dados sensíveis.
- [ ] Recursos da VM definidos e compatíveis com o host.
- [ ] Nenhuma configuração da VM CentOS existente foi alterada.

## Evidências
Anexar `docs/host-inventory.md` e uma captura das configurações gerais do VMware (oculte informações pessoais).

## Não faça
Não instale Ubuntu ainda e não altere BIOS/UEFI sem necessidade.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
