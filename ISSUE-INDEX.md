# Índice de Issues

Publique cada arquivo como uma Issue separada no GitHub, na ordem abaixo.

- [Issue #00 — Planejar o laboratório e inventariar o computador](issues/00-planejar-laboratorio.md) — depende de Nenhuma; fase `foundation`.
- [Issue #01 — Criar e instalar a VM Ubuntu Server](issues/01-instalar-ubuntu-server.md) — depende de #00; fase `foundation`.
- [Issue #02 — Configurar e validar a rede da VM](issues/02-rede-vm.md) — depende de #01; fase `foundation`.
- [Issue #03 — Acessar o Ubuntu pelo Windows usando SSH](issues/03-ssh-windows.md) — depende de #02; fase `foundation`.
- [Issue #04 — Atualizar o sistema e administrar pacotes](issues/04-atualizacoes-pacotes.md) — depende de #03; fase `foundation`.
- [Issue #05 — Explorar e organizar o filesystem Linux](issues/05-filesystem.md) — depende de #04; fase `foundation`.
- [Issue #06 — Administrar usuários, grupos e privilégios sudo](issues/06-usuarios-grupos-sudo.md) — depende de #05; fase `operations`.
- [Issue #07 — Aplicar propriedade, permissões e umask](issues/07-permissoes.md) — depende de #06; fase `operations`.
- [Issue #08 — Inspecionar processos e consumo de recursos](issues/08-processos-recursos.md) — depende de #07; fase `operations`.
- [Issue #09 — Gerenciar serviços com systemd](issues/09-systemd-servicos.md) — depende de #08; fase `operations`.
- [Issue #10 — Consultar logs e diagnosticar falhas](issues/10-logs-diagnostico.md) — depende de #09; fase `operations`.
- [Issue #11 — Diagnosticar conectividade e portas de rede](issues/11-rede-diagnostico.md) — depende de #10; fase `operations`.
- [Issue #12 — Configurar UFW sem perder o acesso SSH](issues/12-firewall-ufw.md) — depende de #11; fase `security`.
- [Issue #13 — Inspecionar armazenamento, filesystems e montagem](issues/13-armazenamento-montagem.md) — depende de #12; fase `operations`.
- [Issue #14 — Criar scripts Bash operacionais](issues/14-bash-automacao.md) — depende de #13; fase `automation`.
- [Issue #15 — Agendar tarefas com cron e systemd timers](issues/15-agendamento.md) — depende de #14; fase `automation`.
- [Issue #16 — Implementar backup e testar restauração](issues/16-backup-restore.md) — depende de #15; fase `reliability`.
- [Issue #17 — Aplicar hardening básico no Ubuntu Server](issues/17-hardening.md) — depende de #16; fase `security`.
- [Issue #18 — Criar runbooks e resolver incidentes simulados](issues/18-runbooks-incidentes.md) — depende de #17; fase `reliability`.
- [Issue #19 — Instalar e operar Docker Engine](issues/19-docker-engine.md) — depende de #18; fase `deployment`.
- [Issue #20 — Fazer deploy de uma aplicação com Docker Compose](issues/20-deploy-app-compose.md) — depende de #19; fase `deployment`.
- [Issue #21 — Implementar monitoramento básico e alertas locais](issues/21-monitoramento.md) — depende de #20; fase `reliability`.
- [Issue #22 — Executar teste integrado de recuperação operacional](issues/22-recuperacao-final.md) — depende de #21; fase `reliability`.
- [Issue #23 — Consolidar documentação e demonstrar o laboratório](issues/23-documentacao-demonstracao.md) — depende de #22; fase `documentation`.
