# Issue #07 — Aplicar propriedade, permissões e umask

**Labels:** `phase: operations`, `priority: high`, `type: practical`
**Dependência:** #06

## Contexto
Usuários e grupos só são úteis quando o acesso aos arquivos está corretamente controlado.

## Objetivo
Implementar diretórios de departamentos com acesso baseado em grupos e validar permissões efetivas.

## Tarefas
- [ ] Criar `/srv/departments/development` e `/srv/departments/operations`.
- [ ] Definir grupos proprietários e permissões adequadas usando `chown` e `chmod`.
- [ ] Aplicar setgid nos diretórios compartilhados para herança de grupo quando apropriado.
- [ ] Configurar `umask` e observar permissões de arquivos novos.
- [ ] Testar criação, leitura, alteração e exclusão como `dev01`, `ops01` e usuário administrativo.
- [ ] Usar `namei -l` para inspecionar permissões de cada componente do caminho.
- [ ] Usar `getfacl`/`setfacl` somente se houver um requisito que permissões tradicionais não resolvam; documentar a decisão.
- [ ] Corrigir qualquer acesso excessivo encontrado.

## Conceitos que você deve compreender
Permissões read/write/execute, permissões simbólicas e octais, proprietário, grupo, setgid, sticky bit, umask e ACL.

## Critérios de aceitação
- [ ] Usuários autorizados conseguem acessar o diretório do departamento.
- [ ] Usuários não autorizados recebem `Permission denied`.
- [ ] Novos arquivos herdam o grupo esperado, quando configurado setgid.
- [ ] Não foi usado `chmod -R 777`.
- [ ] Matriz de acesso documentada em `docs/access-matrix.md`.

## Evidências
Tabela com usuário × operação × resultado e saídas de `stat`, `namei -l` e `ls -ld`.

## Não faça
Não altere permissões recursivamente em diretórios do sistema.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
