# Issue #16 — Implementar backup e testar restauração

**Labels:** `phase: reliability`, `priority: high`, `type: practical`
**Dependência:** #15

## Contexto
Backup só é confiável quando a restauração foi testada. Um arquivo compactado que nunca foi restaurado não comprova recuperação.

## Objetivo
Criar backup dos dados de laboratório, validar integridade e restaurar em um diretório separado.

## Tarefas
- [ ] Definir escopo: incluir `/srv/lab-data` e documentação/configurações próprias necessárias; excluir caches e dados temporários.
- [ ] Definir destino no disco adicional montado na Issue #13.
- [ ] Criar script de backup com `tar` ou `rsync`, timestamp e log.
- [ ] Garantir que falhas retornem código diferente de zero.
- [ ] Gerar checksum SHA-256 do arquivo de backup.
- [ ] Criar arquivos de teste com conteúdo conhecido.
- [ ] Executar backup.
- [ ] Restaurar para `/tmp/restore-test` ou outro diretório isolado, nunca sobrescrever a origem.
- [ ] Comparar conteúdo e checksum.
- [ ] Documentar política de retenção, frequência, escopo e procedimento de restauração.

## Conceitos que você deve compreender
RPO, RTO, backup full, retenção, checksum, consistência, restore e cópia fora do host.

## Critérios de aceitação
- [ ] Backup é criado com timestamp.
- [ ] Checksum é validado.
- [ ] Restauração em diretório isolado funciona.
- [ ] Conteúdo restaurado corresponde ao original.
- [ ] Procedimento de recuperação está documentado.

## Limitação
O disco adicional está na mesma VM/host físico; isso é um exercício de operação, **não** uma estratégia de disaster recovery real. Em produção, mantenha cópia fora do host e teste recuperação.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
