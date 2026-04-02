# shgen

Toolkit de geradores de arquivos e templates focado em portabilidade POSIX e simplicidade.  
O objetivo do projeto é acelerar a criação de scripts, configs e estruturas iniciais
seguindo boas práticas Unix.

## Objetivo

Este repositório reúne pequenos generators escritos em shell script que permitem
criar rapidamente arquivos base para diferentes linguagens e formatos, mantendo:

- Portabilidade (POSIX sh)
- Simplicidade
- Padronização
- Boas práticas básicas
- Estrutura inicial reutilizável

## Ferramentas disponíveis

Atualmente o projeto inclui geradores para:

### Shell e automação
- shgen → scripts POSIX shell
- awkgen → scripts AWK
- sedgen → scripts sed
- makegen → Makefiles

### Containers e build
- dockergen → Dockerfiles
- cmakegen → CMakeLists.txt

### Linguagens
- pygen → Python
- jsgen → JavaScript
- phpgen → PHP
- luagen → Lua
- tclgen → TCL
- rgen → R
- groovygen → Groovy
- schemegen → Scheme
- elgen → Emacs Lisp

### Dados e configuração
- sqlgen → SQL
- yamlgen → YAML
- jsongen → JSON
- tomlgen → TOML
- inigen → INI
- tfgen → Terraform

### Outros
- psgen → PostScript
- scmgen → Scheme configs

## Requisitos

Apenas:

```

POSIX shell (/bin/sh)

```

Nenhuma dependência externa é necessária.

## Uso

Clone o repositório:

```

git clone [https://github.com/marcelositr/shgen](https://github.com/marcelositr/shgen)
cd shgen

```

Dê permissão de execução:

```

chmod +x *

```

Execute o generator desejado:

```

./shgen
./pygen
./dockergen

```

## Filosofia

O projeto segue alguns princípios:

- KISS (Keep It Simple)
- Ferramentas pequenas e focadas
- Zero dependências
- Scripts legíveis
- Compatibilidade máxima

## Estrutura

```

shgen/
├── shgen
├── awkgen
├── dockergen
├── pygen
├── jsgen
├── sqlgen
└── outros generators

```

## Licença

MIT License.

## Autor

Marcelo (marcelositr)

## Status do projeto

Em desenvolvimento contínuo. Novos generators podem ser adicionados conforme necessidade.
