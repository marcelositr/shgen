# Plano de Expansão de Generators – shgen

Este arquivo define a fila oficial de generators do projeto.

A IA deve:

1 analisar os generators existentes
2 comparar com este arquivo
3 gerar apenas os que estão como TODO
4 nunca recriar os que já existem
5 seguir obrigatoriamente LLM_CONTROL.md

--------------------------------------------------

REGRA DE NOMENCLATURA

O nome do generator DEVE ser:

extensão do arquivo + gen

Exemplos:

.py → pygen
.rs → rsgen
.go → gogen
.kt → ktgen
.hs → hsgen

Sempre usar a extensão real do arquivo.
Nunca usar o nome da linguagem.

--------------------------------------------------

DEFINIÇÃO DE STATUS

EXISTS   → já existe no projeto
TODO     → precisa ser criado
SKIP     → ignorar
FUTURE   → não gerar ainda

Pipeline obrigatório:

TODO → GENERATED → VERIFIED → DONE

--------------------------------------------------

GENERATORS EXISTENTES

awkgen
cmakegen
dockergen
elgen
groovygen
jsgen
luagen
makegen
phpgen
plgen
psgen
pygen
rgen
schemegen
scmgen
sedgen
shgen
sqlgen
tclgen
tfgen

--------------------------------------------------

FILA DE GENERATORS

linguagem: C
extensão: .c
generator: cgen
base: shgen
status: DONE

--------------------------------------------------

linguagem: C++
extensão: .cpp
generator: cppgen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Header C
extensão: .h
generator: hgen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Header C++
extensão: .hpp
generator: hppgen
base: cppgen
status: DONE

--------------------------------------------------

linguagem: Rust
extensão: .rs
generator: rsgen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Go
extensão: .go
generator: gogen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Zig
extensão: .zig
generator: ziggen
base: cgen
status: DONE

--------------------------------------------------

linguagem: V
extensão: .v
generator: vgen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Java
extensão: .java
generator: javagen
base: groovygen
status: DONE

--------------------------------------------------

linguagem: Kotlin
extensão: .kt
generator: ktgen
base: javagen
status: DONE

--------------------------------------------------

linguagem: Scala
extensão: .scala
generator: scalagen
base: javagen
status: DONE

--------------------------------------------------

linguagem: Swift
extensão: .swift
generator: swiftgen
base: cgen
status: DONE

--------------------------------------------------

linguagem: Dart
extensão: .dart
generator: dartgen
base: jsgen
status: DONE

--------------------------------------------------

linguagem: Ruby
extensão: .rb
generator: rbgen
base: pygen
status: DONE

--------------------------------------------------

linguagem: Julia
extensão: .jl
generator: jlgen
base: pygen
status: DONE

--------------------------------------------------

linguagem: Nim
extensão: .nim
generator: nimgen
base: pygen
status: DONE

--------------------------------------------------

linguagem: Crystal
extensão: .cr
generator: crgen
base: rbgen
status: DONE

--------------------------------------------------

linguagem: Haskell
extensão: .hs
generator: hsgen
base: pygen
status: DONE

--------------------------------------------------

linguagem: OCaml
extensão: .ml
generator: mlgen
base: pygen
status: DONE

--------------------------------------------------

linguagem: F#
extensão: .fs
generator: fsgen
base: mlgen
status: DONE

--------------------------------------------------

INSTRUÇÕES DE EXECUÇÃO PARA IA

Quando solicitado:

Ler LLM_CONTROL.md
Ler GENERATORS_PLAN.md

Processar TODOS os TODO.

Para cada generator:

seguir estrutura do base
seguir estilo existente
passar shellcheck
manter compatibilidade POSIX
garantir consistência

Após gerar:

mudar status para DONE.

Nunca gerar nada fora desta lista.

--------------------------------------------------

REGRA FINAL

Ferramentas pequenas devem permanecer pequenas.

Consistência é mais importante que inovação.
