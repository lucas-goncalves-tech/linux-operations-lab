# Linux Operations Lab — Backlog completo

Projeto prático para transformar uma VM Ubuntu Server no VMware Workstation Pro 17 em uma VPS simulada, administrada remotamente pelo Windows.

## Objetivo final

Ao concluir o backlog, você deverá conseguir instalar, configurar, proteger, operar, diagnosticar, automatizar e documentar um servidor Linux; executar uma aplicação como serviço; realizar backup e recuperação; e demonstrar tudo por evidências reproduzíveis.

Este laboratório é deliberadamente local. **Não crie uma conta AWS nem provisiona recursos pagos para executar estas Issues.** AWS, LocalStack e Terraform entram em projetos posteriores.

## Ambiente-alvo

- Hipervisor: VMware Workstation Pro 17.
- VM principal: Ubuntu Server 24.04 LTS (64-bit).
- VM CentOS existente: mantenha-a como laboratório secundário; não é pré-requisito.
- Recursos iniciais sugeridos: 2 vCPU, 4 GB RAM e disco virtual de 40 GB (thin provisioned). Se o computador tiver poucos recursos, use 2 GB RAM e reduza serviços simultâneos.
- Rede inicial: Bridged, para a VM receber um IP da rede local e o Windows conseguir acessá-la. Não configure redirecionamento de portas no roteador nem exponha SSH à internet.
- Acesso administrativo: conta pessoal sem login SSH direto como root; `sudo` para tarefas administrativas.
- Ferramentas no Windows: PowerShell e um cliente SSH (o OpenSSH Client do Windows normalmente já atende).

## Como usar

1. Crie um repositório GitHub chamado `linux-operations-lab`.
2. Copie cada arquivo da pasta `issues/` para uma Issue separada, mantendo o título e o corpo.
3. Crie as labels listadas abaixo.
4. Execute as Issues na ordem numérica. Não pule uma Issue só porque já conhece o assunto: use-a para validar e documentar o procedimento.
5. Em cada Issue, registre comandos executados, decisões, saídas relevantes e evidências. Não publique senhas, chaves privadas, tokens, IP público ou dados pessoais.
6. Só marque uma Issue como concluída quando todos os critérios de aceitação forem verdadeiros.

## Regras de execução

- Tire um snapshot VMware antes de mudanças de rede, SSH, firewall, armazenamento ou hardening.
- Mantenha o console VMware aberto enquanto altera SSH/firewall. Teste uma segunda sessão SSH antes de encerrar a sessão original.
- Não execute comandos destrutivos de disco (`mkfs`, `fdisk`, `parted`, `wipefs`, `dd`) fora de um disco virtual descartável e sem conferir o dispositivo.
- Não use `chmod -R 777`.
- Não desabilite autenticação por senha no SSH até provar que a autenticação por chave funciona em uma segunda sessão.
- Não habilite acesso público no roteador. O objetivo é simular uma VPS na LAN, não publicar o servidor na internet.
- Se algo quebrar, use o console VMware e o snapshot anterior; documente a causa em vez de reinstalar imediatamente.

## Labels sugeridas

- `phase: foundation`
- `phase: operations`
- `phase: security`
- `phase: automation`
- `phase: reliability`
- `phase: deployment`
- `type: documentation`
- `type: practical`
- `type: troubleshooting`
- `priority: high`
- `priority: medium`

## Mapa de dependências

As Issues são uma trilha linear intencional: cada uma usa artefatos ou conhecimentos verificados na anterior.

| Issue | Entrega principal | Depende de |
|---|---|---|
| 00 | Planejamento e inventário do host | — |
| 01 | VM Ubuntu instalada | 00 |
| 02 | Rede da VM validada | 01 |
| 03 | SSH funcional Windows → Ubuntu | 02 |
| 04 | Sistema atualizado e pacotes administrados | 03 |
| 05 | Navegação e organização do filesystem | 04 |
| 06 | Usuários, grupos e sudo | 05 |
| 07 | Permissões e propriedade | 06 |
| 08 | Processos e consumo de recursos | 07 |
| 09 | Serviços com systemd | 08 |
| 10 | Logs e diagnóstico | 09 |
| 11 | Diagnóstico de rede | 10 |
| 12 | Firewall UFW sem perder acesso | 11 |
| 13 | Discos, espaço e montagem segura | 12 |
| 14 | Bash para tarefas operacionais | 13 |
| 15 | Agendamento de tarefas | 14 |
| 16 | Backup e restauração testada | 15 |
| 17 | Hardening básico do servidor | 16 |
| 18 | Runbooks e troubleshooting de incidentes | 17 |
| 19 | Docker Engine e operação de containers | 18 |
| 20 | Aplicação containerizada e persistência | 19 |
| 21 | Monitoramento e alertas locais | 20 |
| 22 | Teste final de recuperação operacional | 21 |
| 23 | Documentação final e demonstração | 22 |

## Definição de pronto global

O laboratório só está concluído quando:
- A VM pode ser acessada do Windows por SSH.
- As tarefas administrativas são feitas com `sudo`, sem login remoto como root.
- Usuários e permissões foram testados com contas distintas.
- Serviços, logs, rede, firewall e armazenamento foram diagnosticados.
- Scripts e tarefas agendadas têm tratamento de erro e logs.
- Um backup foi restaurado com sucesso.
- O servidor tem hardening básico e runbooks.
- Uma aplicação Docker funciona após reinicialização e mantém seus dados.
- Há evidências e documentação suficientes para outra pessoa reproduzir o laboratório.
