# Issue #05 — Explorar e organizar o filesystem Linux

**Labels:** `phase: foundation`, `priority: high`, `type: practical`
**Dependência:** #04

## Contexto
Antes de administrar um servidor, você precisa localizar configurações, logs, dados, executáveis e diretórios temporários.

## Objetivo
Compreender a hierarquia padrão do filesystem (FHS) e organizar diretórios de trabalho do laboratório.

## Tarefas
- [ ] Explorar `/`, `/etc`, `/var`, `/var/log`, `/home`, `/tmp`, `/usr`, `/opt`, `/srv` e `/proc`.
- [ ] Usar `pwd`, `ls -lah`, `tree`, `find`, `file`, `stat`, `which` e `whereis`.
- [ ] Diferenciar caminho absoluto e relativo.
- [ ] Criar `/opt/lab` para arquivos de laboratório e `/srv/lab-data` para dados de serviço.
- [ ] Criar subdiretórios `scripts`, `config`, `data` e `backup` em `/opt/lab` ou justificar outra estrutura.
- [ ] Identificar arquivos de configuração de SSH em `/etc/ssh`.
- [ ] Identificar logs em `/var/log`.
- [ ] Documentar a finalidade dos diretórios relevantes em `docs/filesystem.md`.

## Conceitos que você deve compreender
Filesystem hierarchy, inode, diretório, arquivo, caminho, filesystem virtual e diferença entre `/opt`, `/srv`, `/etc` e `/var`.

## Critérios de aceitação
- [ ] Você localiza os diretórios principais sem depender de um tutorial.
- [ ] `/opt/lab` e `/srv/lab-data` existem com finalidade documentada.
- [ ] Nenhum arquivo do sistema foi movido ou apagado.
- [ ] Documento inclui exemplos de comandos de navegação e busca.

## Evidências
Saídas de `find /opt/lab -maxdepth 2 -type d`, `df -hT` e `ls -lah /var/log`.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
