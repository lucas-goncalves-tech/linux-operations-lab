# Issue #17 — Aplicar hardening básico no Ubuntu Server

**Labels:** `phase: security`, `priority: high`, `type: practical`
**Dependência:** #16

## Contexto
Um servidor deve reduzir superfície de ataque e manter acesso administrativo controlado.

## Objetivo
Aplicar medidas básicas de segurança sem bloquear o próprio acesso.

## Pré-requisitos
Snapshot VMware, console aberto e duas sessões SSH funcionais. Backup da configuração SSH atual.

## Tarefas
- [ ] Atualizar sistema e verificar atualizações de segurança pendentes.
- [ ] Confirmar que root não é necessário para login remoto.
- [ ] Criar chave SSH ed25519 no Windows, protegendo a chave privada com passphrase.
- [ ] Instalar apenas a chave pública no usuário administrativo usando `ssh-copy-id` se disponível, ou procedimento manual seguro.
- [ ] Testar login por chave em uma NOVA sessão SSH.
- [ ] Fazer backup de `/etc/ssh/sshd_config` e usar um arquivo em `/etc/ssh/sshd_config.d/` quando apropriado.
- [ ] Validar a configuração com `sudo sshd -t`.
- [ ] Somente após confirmar login por chave, desabilitar login SSH de root e autenticação por senha, conforme compatibilidade da configuração Ubuntu.
- [ ] Recarregar SSH e testar uma nova sessão antes de fechar a antiga.
- [ ] Revisar UFW, usuários, grupos, permissões de arquivos sensíveis e serviços habilitados.
- [ ] Verificar atualizações automáticas de segurança e documentar sua política.
- [ ] Criar checklist de hardening em `docs/hardening-checklist.md`.

## Conceitos que você deve compreender
Autenticação por chave pública, chave privada, passphrase, sshd, superfície de ataque, menor privilégio, patching e defesa em profundidade.

## Critérios de aceitação
- [ ] Login SSH por chave funciona.
- [ ] Login SSH como root é bloqueado.
- [ ] Autenticação por senha só é desabilitada depois do teste por chave.
- [ ] `sshd -t` não retorna erro.
- [ ] SSH continua acessível após recarregar/reiniciar.
- [ ] Procedimento de recuperação pelo console VMware está documentado.

## Segurança crítica
Nunca envie chave privada para GitHub, Anki, chat ou documentação. Não feche a sessão SSH original até validar outra. Se a configuração falhar, restaure o backup pelo console.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
