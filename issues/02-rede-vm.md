# Issue #02 — Configurar e validar a rede da VM

**Labels:** `phase: foundation`, `priority: high`, `type: practical`
**Dependência:** #01

## Contexto
Um servidor remoto precisa de conectividade previsível. Antes de configurar SSH, precisamos entender como a VM se conecta à rede local.

## Objetivo
Conectar a VM à LAN usando a rede Bridged do VMware e documentar como localizar seu endereço IP.

## Tarefas
- [ ] Desligar a VM e selecionar `Bridged` nas configurações de Network Adapter.
- [ ] Marcar a opção de conectar ao ligar, se disponível.
- [ ] Iniciar a VM e executar `ip -brief address`.
- [ ] Identificar a interface ativa e o endereço IPv4 atribuído.
- [ ] Executar `ip route` e identificar o gateway padrão.
- [ ] Verificar resolução DNS com `resolvectl status` e `getent hosts ubuntu.com`.
- [ ] Testar conectividade IP com `ping -c 4 1.1.1.1` e conectividade DNS com `ping -c 4 ubuntu.com` (se ICMP for permitido).
- [ ] No Windows, testar `ping <IP_DA_VM>` e registrar o resultado.
- [ ] Documentar que o IP pode mudar por DHCP; não presumir que ele é fixo.
- [ ] Se Bridged não funcionar na rede atual, registrar o problema e usar NAT com encaminhamento de porta SSH apenas no VMware, documentando a configuração.

## Conceitos que você deve compreender
IP, máscara/prefixo, gateway, DNS, DHCP, interface, rota, NAT e Bridged.

## Critérios de aceitação
- [ ] VM tem endereço IPv4 válido na rede esperada.
- [ ] Existe rota padrão.
- [ ] Resolução DNS funciona.
- [ ] O Windows consegue alcançar a VM, ou a alternativa NAT está documentada e validada.
- [ ] IP, interface, gateway e modo de rede estão registrados em `docs/network.md`.

## Evidências
`ip -brief address`, `ip route`, `resolvectl status` e testes feitos no Windows.

## Segurança
Não configure redirecionamento de portas no roteador. Não exponha a VM à internet.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
