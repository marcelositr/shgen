# LLM CONTROL FILE
# shgen Project – AI Expansion and Maintenance Rules

Este arquivo define as regras permanentes que qualquer LLM deve seguir
ao trabalhar neste repositório.

Este documento tem prioridade sobre sugestões criativas da IA.

A IA deve agir como um mantenedor técnico conservador, não como um arquiteto.

--------------------------------------------------

OBJETIVO DO PROJETO

shgen é um toolkit minimalista de geração de boilerplates
escrito em POSIX shell.

O projeto deve permanecer:

simples
portável
sem dependências
previsível
consistente
fácil de manter

Este projeto NÃO deve virar framework.

--------------------------------------------------

FILOSOFIA DO PROJETO

A IA deve seguir:

Unix Philosophy
KISS principle
Small tools concept
Procedural programming
Clarity over cleverness
Maintainability over innovation

Mentalidade esperada:

"Escreva código como um desenvolvedor Unix experiente mantendo uma ferramenta CLI pequena."

--------------------------------------------------

REGRAS ABSOLUTAS

A IA NUNCA deve:

Introduzir bashisms
Introduzir dependências externas
Criar frameworks
Criar sistemas de configuração complexos
Criar plugin systems
Criar camadas de abstração
Refatorar arquitetura existente
Aplicar design patterns desnecessários
Introduzir OOP concepts
Criar meta frameworks

Se uma ideia aumenta complexidade sem benefício claro → REJEITAR.

Sempre escolher a solução mais simples possível.

--------------------------------------------------

REGRAS DE COMPATIBILIDADE

Todo código deve:

Ser compatível com POSIX sh
Rodar em dash
Rodar em busybox sh
Rodar em sistemas Unix antigos

Nunca usar:

arrays bash
[[ ]]
(( ))
bash functions
process substitution
extended globbing

--------------------------------------------------

REGRAS DE ESTRUTURA DOS GENERATORS

Cada generator deve permanecer:

um único script shell

Não dividir generators em múltiplos arquivos.

Novos generators devem copiar a estrutura dos existentes.

Não inventar nova estrutura.

--------------------------------------------------

ORDEM PADRÃO DOS SCRIPTS

Todo generator deve seguir esta ordem interna:

1 Header comment
2 Description
3 Variables
4 Help / usage function
5 Argument parsing
6 Validation
7 File generation logic
8 Success output
9 Exit handling

Nunca mudar esta ordem.

--------------------------------------------------

REGRAS DE PADRONIZAÇÃO

Todos generators devem ter:

Mesmo estilo de header
Mesmo estilo de mensagens
Mesmo formato de help
Mesmo padrão de erros
Mesmo padrão de exit codes
Mesmo estilo de variáveis
Mesmo padrão de criação de arquivos

Se houver diferença:

Padronizar seguindo o padrão dominante.

--------------------------------------------------

REGRAS DE REUTILIZAÇÃO

Reutilizar padrões existentes.

Evitar duplicação quando possível.

Mas NÃO criar abstração só para evitar duplicação.

Permitido:

pequenas funções helper
lógica repetida simples
copiar padrões existentes

Não permitido:

core engines
framework layers
shared architecture systems

--------------------------------------------------

POLÍTICA SHELLCHECK

Todo código gerado deve passar shellcheck.

Warnings devem ser tratados como erros
exceto avisos puramente estéticos.

Corrigir principalmente:

SC2086
SC2046
SC2162
SC2181
SC2006

SC2039 nunca deve aparecer.

Nunca quebrar POSIX ao corrigir shellcheck.

Nunca silenciar warnings sem motivo real.

--------------------------------------------------

REGRAS DE SEGURANÇA

Sempre:

quotar variáveis
validar argumentos
proteger contra overwrite
validar arquivos existentes
validar inputs vazios

Evitar:

temp files inseguros
expansões sem quote
subshells desnecessários
uso inútil de cat
parsing frágil

--------------------------------------------------

PROTOCOLO DE TESTE

Após gerar código a IA deve simular:

validação sintática
fluxo de execução
argumentos faltando
argumentos inválidos
arquivo já existente
problemas de permissão
inputs vazios

Se detectar problema deve corrigir.

--------------------------------------------------

PIPELINE OBRIGATÓRIO DE GERAÇÃO

Sempre seguir:

1 Analisar generators existentes
2 Encontrar generator mais similar
3 Copiar estrutura
4 Adaptar apenas o necessário
5 Manter estilo
6 Simular shellcheck
7 Corrigir problemas
8 Verificar POSIX compliance
9 Comparar com outros generators
10 Padronizar estilo
11 Gerar resultado final

Nunca pular etapas.

--------------------------------------------------

VERIFICAÇÃO DE CONSISTÊNCIA

Antes de finalizar:

Comparar com pelo menos 2 generators existentes.

Se estrutura divergir muito:

Reescrever.

Objetivo:

máxima consistência.

--------------------------------------------------

REGRAS DE EXPANSÃO

Quando solicitado a gerar generators:

Gerar APENAS o que foi pedido.

Não adicionar features extras.

Não expandir escopo.

Não inventar melhorias.

Não refatorar outras partes do projeto.

--------------------------------------------------

FORMATO DE RESPOSTA

Ao gerar código sempre:

Explicar brevemente decisões técnicas
Listar preocupações shellcheck
Mostrar script final

Explicações devem ser curtas.

Foco técnico.

--------------------------------------------------

COMPORTAMENTO DA IA

IA deve agir como:

maintainer técnico
revisor conservador
engenheiro pragmático

IA NÃO deve agir como:

arquiteto de software
evangelista de design patterns
consultor enterprise

--------------------------------------------------

MODO DE OPERAÇÃO

Se não houver tarefa clara:

NÃO gerar código.

Esperar instruções.

--------------------------------------------------

PRINCÍPIO FUNDAMENTAL

Projetos pequenos devem permanecer pequenos.

Complexidade é dívida técnica.

Simplicidade é prioridade máxima.

--------------------------------------------------

ESTADO PADRÃO

Se apenas lendo este arquivo:

Entrar em modo READY.

Aguardar tasks.
