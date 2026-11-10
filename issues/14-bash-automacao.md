# Issue #14 — Criar scripts Bash operacionais

**Labels:** `phase: automation`, `priority: high`, `type: practical`
**Dependência:** #13

## Contexto
Operações repetitivas devem ser automatizadas de forma previsível, validável e segura.

## Objetivo
Criar scripts Bash pequenos para verificar a saúde do servidor e organizar arquivos de laboratório.

## Tarefas
- [ ] Criar `scripts/server-health.sh` para exibir hostname, uptime, uso de memória, uso de disco e estado do SSH.
- [ ] Usar shebang, `set -euo pipefail` quando adequado, variáveis, funções e códigos de saída.
- [ ] Validar argumentos e caminhos antes de agir.
- [ ] Enviar mensagens informativas para stdout e erros para stderr.
- [ ] Criar `scripts/archive-lab-data.sh` para arquivar apenas dados de teste dentro de `/srv/lab-data`.
- [ ] Usar `shellcheck` para analisar scripts; instalar se necessário.
- [ ] Testar cenários de sucesso, argumento ausente e caminho inexistente.
- [ ] Garantir permissões executáveis e documentação de uso.
- [ ] Versionar scripts no GitHub.

## Conceitos que você deve compreender
Shebang, variável, quoting, exit code, stdout, stderr, pipefail, função, argumento posicional e idempotência básica.

## Critérios de aceitação
- [ ] Scripts executam sem erro nos cenários previstos.
- [ ] Entradas inválidas geram mensagem útil e código de saída diferente de zero.
- [ ] Nenhum script apaga ou altera arquivos fora da área de laboratório.
- [ ] `shellcheck` não aponta problemas relevantes sem justificativa documentada.
- [ ] README de cada script explica pré-requisitos, uso e exemplo.

## Evidências
Scripts versionados, saída de execução e resultado do ShellCheck.

## Não faça
Não use `sudo` indiscriminadamente dentro dos scripts. Não coloque senhas ou tokens no código.

---
**Registro de execução**
- Data:
- Resultado:
- Dificuldades encontradas:
- O que aprendi:
- Evidências/links:
