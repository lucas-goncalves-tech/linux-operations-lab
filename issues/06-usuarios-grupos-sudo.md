# Issue #06 — Administrar usuários, grupos e privilégios sudo

**Labels:** `phase: operations`, `priority: high`, `type: practical`
**Dependência:** #05

## Contexto
Servidores não devem depender de uma única conta compartilhada. Acesso deve ser concedido por identidade e função.

## Objetivo
Criar usuários e grupos de laboratório e validar privilégios administrativos.

## Tarefas
- [ ] Inspecionar usuários e grupos com `id`, `getent passwd` e `getent group`.
- [ ] Criar grupos `developers` e `operators`.
- [ ] Criar usuários de teste `dev01` e `ops01`, com diretórios home.
- [ ] Adicionar cada usuário ao grupo correto usando `usermod -aG`.
- [ ] Verificar grupos com `id <usuario>` e `groups <usuario>`.
- [ ] Testar login local/SSH de cada usuário.
- [ ] Validar que o usuário administrativo consegue executar `sudo -v`.
- [ ] Validar que usuários comuns não têm sudo indevido.
- [ ] Documentar o processo de admissão, alteração e remoção de usuário em `docs/user-management.md`.

## Conceitos que você deve compreender
UID, GID, grupo primário e suplementar, `/etc/passwd`, `/etc/shadow`, `/etc/group`, sudo e princípio do menor privilégio.

## Critérios de aceitação
- [ ] Grupos e usuários existem.
- [ ] Cada usuário pertence ao grupo esperado.
- [ ] `dev01` e `ops01` não têm privilégio administrativo.
- [ ] O usuário administrativo mantém acesso sudo.
- [ ] Procedimento de gestão de contas documentado.

## Evidências
Saídas de `id dev01`, `id ops01`, `getent group developers` e teste de sudo.

## Segurança
Use senhas de teste fortes e únicas. Não publique hashes, senhas ou conteúdo de `/etc/shadow`.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
