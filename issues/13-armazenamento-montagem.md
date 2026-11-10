# Issue #13 — Inspecionar armazenamento, filesystems e montagem

**Labels:** `phase: operations`, `priority: medium`, `type: practical`
**Dependência:** #12

## Contexto
Servidores precisam monitorar espaço e entender dispositivos, partições e pontos de montagem.

## Objetivo
Inspecionar o armazenamento da VM e praticar montagem usando um segundo disco virtual descartável.

## Tarefas
- [ ] Consultar `lsblk -f`, `blkid`, `findmnt`, `df -hT` e `df -i`.
- [ ] Diferenciar disco, partição, filesystem e mount point.
- [ ] Adicionar um segundo disco virtual pequeno (por exemplo, 2–4 GB) no VMware, com a VM desligada.
- [ ] Identificar o novo dispositivo com `lsblk` e confirmar tamanho/modelo antes de qualquer operação.
- [ ] Criar uma partição e filesystem somente no disco virtual novo e descartável.
- [ ] Montar temporariamente em `/mnt/lab-disk`.
- [ ] Criar arquivo de teste, desmontar e montar novamente.
- [ ] Configurar montagem persistente por UUID em `/etc/fstab`.
- [ ] Validar a configuração com `sudo findmnt --verify` e `sudo mount -a` antes de reiniciar.
- [ ] Reiniciar e verificar a montagem.
- [ ] Documentar recuperação se a montagem falhar.

## Conceitos que você deve compreender
Block device, partição, filesystem, UUID, mount, `/etc/fstab`, espaço livre e inode.

## Critérios de aceitação
- [ ] O disco correto foi identificado pelo tamanho e por `lsblk`.
- [ ] O filesystem do disco adicional monta no ponto esperado.
- [ ] Montagem persiste após reboot.
- [ ] O disco original do sistema não foi formatado.
- [ ] `docs/storage.md` explica o processo e a recuperação.

## Evidências
Saídas de `lsblk -f`, `findmnt`, `df -hT` antes/depois e trecho não sensível de `/etc/fstab`.

## ATENÇÃO
Esta Issue envolve particionamento e formatação. **Nunca copie um comando `mkfs`, `fdisk` ou `parted` sem identificar novamente o dispositivo.** Se tiver qualquer dúvida sobre qual disco é o novo, pare e peça revisão.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
