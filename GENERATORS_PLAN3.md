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
cgen
cppgen
hgen
hppgen
rsgen
gogen
ziggen
vgen
javagen
ktgen
scalagen
swiftgen
dartgen
rbgen
jlgen
nimgen
crgen
hsgen
mlgen
fsgen

---

## FILA DE NOVOS GENERATORS (TODO)

linguagem: TypeScript
extensão: .ts
generator: tsgen
base: jsgen
status: TODO

linguagem: Elixir
extensão: .ex
generator: exgen
base: mlgen
status: TODO

linguagem: Erlang
extensão: .erl
generator: erlgen
base: mlgen
status: TODO

linguagem: F# Script
extensão: .fsx
generator: fsxgen
base: fsgen
status: TODO

linguagem: Assembly
extensão: .asm
generator: asmgen
base: cgen
status: TODO

linguagem: Racket
extensão: .rkt
generator: rktgen
base: schemegen
status: TODO

linguagem: Clojure
extensão: .clj
generator: cljgen
base: schemegen
status: TODO

linguagem: Scala Script
extensão: .sc
generator: scgen
base: scalagen
status: TODO

linguagem: Julia Module
extensão: .jlm
generator: jlmgen
base: jlgen
status: TODO

linguagem: Nim Package
extensão: .nimble
generator: nimblegen
base: nimgen
status: TODO

linguagem: Crystal Shard
extensão: .crs
generator: crsgen
base: crgen
status: TODO

linguagem: Kotlin Module
extensão: .ktm
generator: ktmgen
base: ktgen
status: TODO

linguagem: Go App
extensão: .goa
generator: goagen
base: gogen
status: TODO

linguagem: Rust Module
extensão: .rsmod
generator: rsmodgen
base: rsgen
status: TODO

linguagem: Haskell Cabal
extensão: .hsc
generator: hscgen
base: hsgen
status: TODO

linguagem: OCaml Library
extensão: .mlib
generator: mlibgen
base: mlgen
status: TODO

linguagem: Ruby Gem
extensão: .rbx
generator: rbxgen
base: rbgen
status: TODO

linguagem: Python C Extension
extensão: .pyx
generator: pyxgen
base: pygen
status: TODO

linguagem: Swift Package
extensão: .swiftpm
generator: swiftpmgen
base: swiftgen
status: TODO

linguagem: Dart Package
extensão: .dartpkg
generator: dartpkggen
base: dartgen
status: TODO

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
