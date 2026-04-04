# Plano de Expansão de Generators – shgen

Este arquivo define a fila oficial de generators do projeto.

A IA deve:

1. analisar os generators existentes
2. comparar com este arquivo
3. gerar apenas os que estão como TODO
4. nunca recriar os que já existem
5. seguir obrigatoriamente LLM_CONTROL.md

---

## REGRA DE NOMENCLATURA

O nome do generator DEVE ser: extensão do arquivo + gen

Exemplos:

* `.py` → pygen
* `.rs` → rsgen
* `.go` → gogen
* `.kt` → ktgen
* `.hs` → hsgen

Sempre usar a extensão real do arquivo.
Nunca usar o nome da linguagem.

---

## DEFINIÇÃO DE STATUS

* EXISTS → já existe no projeto
* TODO → precisa ser criado
* SKIP → ignorar
* FUTURE → não gerar ainda

Pipeline obrigatório: TODO → GENERATED → VERIFIED → DONE

---

## GENERATORS EXISTENTES

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

---

## FILA DE GENERATORS

linguagem: C
extensão: .c
generator: cgen
base: shgen
status: EXISTS

linguagem: C++
extensão: .cpp
generator: cppgen
base: cgen
status: EXISTS

linguagem: Header C
extensão: .h
generator: hgen
base: cgen
status: EXISTS

linguagem: Header C++
extensão: .hpp
generator: hppgen
base: cppgen
status: EXISTS

linguagem: Rust
extensão: .rs
generator: rsgen
base: cgen
status: EXISTS

linguagem: Go
extensão: .go
generator: gogen
base: cgen
status: EXISTS

linguagem: Zig
extensão: .zig
generator: ziggen
base: cgen
status: EXISTS

linguagem: V
extensão: .v
generator: vgen
base: cgen
status: EXISTS

linguagem: Java
extensão: .java
generator: javagen
base: groovygen
status: EXISTS

linguagem: Kotlin
extensão: .kt
generator: ktgen
base: javagen
status: EXISTS

linguagem: Scala
extensão: .scala
generator: scalagen
base: javagen
status: EXISTS

linguagem: Swift
extensão: .swift
generator: swiftgen
base: cgen
status: EXISTS

linguagem: Dart
extensão: .dart
generator: dartgen
base: jsgen
status: EXISTS

linguagem: Ruby
extensão: .rb
generator: rbgen
base: pygen
status: EXISTS

linguagem: Julia
extensão: .jl
generator: jlgen
base: pygen
status: EXISTS

linguagem: Nim
extensão: .nim
generator: nimgen
base: pygen
status: EXISTS

linguagem: Crystal
extensão: .cr
generator: crgen
base: rbgen
status: EXISTS

linguagem: Haskell
extensão: .hs
generator: hsgen
base: pygen
status: EXISTS

linguagem: OCaml
extensão: .ml
generator: mlgen
base: pygen
status: EXISTS

linguagem: F#
extensão: .fs
generator: fsgen
base: mlgen
status: EXISTS

---

## INSTRUÇÕES DE EXECUÇÃO PARA IA

Quando solicitado:

* Ler LLM_CONTROL.md
* Ler GENERATORS_PLAN.md
* Processar TODOS os TODO
* Seguir estrutura do base
* Seguir estilo existente
* Passar shellcheck
* Manter compatibilidade POSIX
* Garantir consistência

Após gerar: mudar status para DONE.

Nunca gerar nada fora desta lista.

---

## REGRA FINAL

Ferramentas pequenas devem permanecer pequenas.
Consistência é mais importante que inovação.
