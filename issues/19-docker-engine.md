# Issue #19 — Instalar e operar Docker Engine

**Labels:** `phase: deployment`, `priority: high`, `type: practical`
**Dependência:** #18

## Contexto
Containers são uma ferramenta comum no fluxo DevOps. Antes de fazer deploy, você precisa compreender imagens, containers, volumes, redes e logs.

## Objetivo
Instalar Docker Engine pelo procedimento oficial compatível com Ubuntu 24.04 e executar containers de teste.

## Tarefas
- [ ] Consultar documentação oficial do Docker Engine para Ubuntu.
- [ ] Instalar Docker Engine e plugin Docker Compose pelo repositório oficial, seguindo o procedimento vigente.
- [ ] Validar `docker version`, `docker info` e `docker compose version`.
- [ ] Executar `hello-world`.
- [ ] Executar um container Nginx e mapear uma porta local alta para a porta 80 do container.
- [ ] Consultar `docker ps`, `docker ps -a`, `docker logs`, `docker inspect` e `docker stats`.
- [ ] Parar, iniciar e remover o container de teste.
- [ ] Criar uma rede Docker própria e conectar um container de teste.
- [ ] Entender o grupo `docker` e por que ele concede privilégios equivalentes a root; não adicionar usuários automaticamente.
- [ ] Documentar instalação, operação e remoção em `docs/docker-basics.md`.

## Conceitos que você deve compreender
Imagem, container, registry, daemon, volume, bind mount, port mapping, bridge network, Compose e privilégio do Docker socket.

## Critérios de aceitação
- [ ] Docker Engine e Compose funcionam.
- [ ] Container Nginx responde localmente.
- [ ] Você consegue inspecionar logs, estado e rede.
- [ ] Container de teste foi removido.
- [ ] Riscos do grupo docker estão documentados.

## Segurança
Não exponha o daemon Docker TCP. Não publique portas na LAN sem necessidade.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
