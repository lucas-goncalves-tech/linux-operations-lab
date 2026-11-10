# Issue #04 — Atualizar o sistema e administrar pacotes

**Labels:** `phase: foundation`, `priority: high`, `type: practical`
**Dependência:** #03

## Contexto
Um servidor precisa receber atualizações de segurança e instalar software de forma controlada.

## Objetivo
Aprender o fluxo de atualização e gerenciamento de pacotes no Ubuntu.

## Tarefas
- [ ] Atualizar índices com `sudo apt update`.
- [ ] Verificar pacotes atualizáveis com `apt list --upgradable`.
- [ ] Aplicar atualizações com `sudo apt upgrade`.
- [ ] Verificar se há reinicialização pendente, quando aplicável.
- [ ] Instalar ferramentas úteis: `curl`, `wget`, `vim-tiny` ou `nano`, `tree`, `unzip`, `htop`, `jq`.
- [ ] Consultar detalhes de um pacote com `apt show`.
- [ ] Localizar arquivos instalados por um pacote com `dpkg -L`.
- [ ] Verificar versão de ferramentas instaladas.
- [ ] Remover um pacote de teste que não seja essencial e confirmar a remoção.
- [ ] Registrar comandos e política de atualização em `docs/package-management.md`.

## Conceitos que você deve compreender
Repositório, índice de pacotes, pacote, dependência, APT, dpkg, upgrade e atualização de segurança.

## Critérios de aceitação
- [ ] Sistema atualizado sem erro não resolvido.
- [ ] Ferramentas instaladas e verificadas.
- [ ] Você consegue explicar a diferença entre `apt update` e `apt upgrade`.
- [ ] Procedimento documentado.

## Evidências
Saídas de `apt list --upgradable`, `apt show curl` e `curl --version`.

## Não faça
Não adicione repositórios de terceiros sem necessidade.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
