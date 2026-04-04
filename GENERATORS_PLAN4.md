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
tsgen
exgen
erlgen
fsxgen
asmgen
rktgen
cljgen
scgen
jlmgen
nimblegen
crsgen
ktmgen
goagen
rsmodgen
hscgen
mlibgen
rbxgen
pyxgen
swiftpmgen
dartpkggen

---

## FILA DE NOVOS GENERATORS (TODO) – Segunda-feira

linguagem: Vue.js
extensão: .vue
generator: vuegen
base: jsgen
status: TODO

linguagem: React JSX
extensão: .jsx
generator: jsxgen
base: jsgen
status: TODO

linguagem: TypeScript JSX
extensão: .tsx
generator: tsxgen
base: tsgen
status: TODO

linguagem: Svelte
extensão: .svelte
generator: sveltegen
base: jsgen
status: TODO

linguagem: Elm
extensão: .elm
generator: elmgen
base: jsgen
status: TODO

linguagem: R script
extensão: .r
generator: rscriptgen
base: rgen
status: TODO

linguagem: PL/SQL
extensão: .plsql
generator: plsqlgen
base: sqlgen
status: TODO

linguagem: TCL script
extensão: .tclscript
generator: tclscriptgen
base: tclgen
status: TODO

linguagem: CoffeeScript
extensão: .coffee
generator: coffeegen
base: jsgen
status: TODO

linguagem: MATLAB/Octave
extensão: .m
generator: mgen
base: pygen
status: TODO

linguagem: Nim script
extensão: .nimscript
generator: nimscriptgen
base: nimgen
status: TODO

linguagem: Crystal library
extensão: .crlib
generator: crlibgen
base: crgen
status: TODO

linguagem: Julia package
extensão: .jlpkg
generator: jlpkggen
base: jlgen
status: TODO

linguagem: Elixir script
extensão: .exs
generator: exsgen
base: exgen
status: TODO

linguagem: Haskell script
extensão: .hsx
generator: hsxgen
base: hsgen
status: TODO

linguagem: OCaml script
extensão: .mlscript
generator: mlscriptgen
base: mlgen
status: TODO

linguagem: F# project
extensão: .fsproj
generator: fsprojgen
base: fsgen
status: TODO

linguagem: SwiftUI component
extensão: .swiftui
generator: swiftuigen
base: swiftgen
status: TODO

linguagem: Dart CLI
extensão: .dartcli
generator: dartcligen
base: dartgen
status: TODO

linguagem: Go API skeleton
extensão: .goapi
generator: goapigen
base: gogen
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
