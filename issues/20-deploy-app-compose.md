# Issue #20 — Fazer deploy de uma aplicação com Docker Compose

**Labels:** `phase: deployment`, `priority: high`, `type: practical`
**Dependência:** #19

## Contexto
Agora o servidor receberá uma aplicação simples. O objetivo não é desenvolver um produto complexo, mas operar um workload com configuração, persistência e logs.

## Objetivo
Implantar uma aplicação HTTP simples via Docker Compose, acessível pela rede local, com dados persistentes.

## Tarefas
- [ ] Escolher uma aplicação de demonstração pequena e mantida (por exemplo, uma aplicação estática Nginx com página própria).
- [ ] Criar diretório `/opt/lab/app`.
- [ ] Criar `compose.yaml` versionado no repositório.
- [ ] Usar imagem oficial e tag explícita, evitando `latest` no deploy documentado.
- [ ] Configurar bind address/porta publicada de forma consciente.
- [ ] Criar volume ou bind mount para conteúdo persistente.
- [ ] Definir política de restart adequada.
- [ ] Iniciar com `docker compose up -d`.
- [ ] Validar localmente com `curl` e, se a regra UFW permitir, a partir do Windows.
- [ ] Consultar logs e estado com Docker Compose.
- [ ] Alterar conteúdo, recriar container e provar que dados persistentes permanecem.
- [ ] Reiniciar a VM e validar recuperação automática.
- [ ] Documentar deploy, atualização, rollback e remoção.

## Conceitos que você deve compreender
Compose, declarative configuration, port publishing, volume, restart policy, health check, image tag e rollback.

## Critérios de aceitação
- [ ] Aplicação responde por HTTP.
- [ ] Configuração está versionada sem segredos.
- [ ] Dados persistem após recriação do container.
- [ ] Serviço volta após reboot.
- [ ] Procedimento de atualização e rollback documentado.

## Segurança
Não coloque segredos no `compose.yaml`. Não publique a aplicação na internet nem abra portas no roteador.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
