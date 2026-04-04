Fechou, mano. Aqui tá o **GENERATORS_PLAN.md completo para quinta-feira**, com todos os EXISTING do repo e os **20 novos TODOs** selecionados, sem repetir nada dos dias anteriores:

---

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
vuegen
jsxgen
tsxgen
sveltegen
elmgen
rscriptgen
plsqlgen
tclscriptgen
coffeegen
mgen
nimscriptgen
crlibgen
jlpkggen
exsgen
hsxgen
mlscriptgen
fsprojgen
swiftuigen
dartcligen
goapigen
mjmlgen
ejsgen
hjsongen
jsonnetgen
protogen
avdlgen
thriftgen
graphqlgen
gqlgen
mjgen
vhdlgen
veriloggen
xsdgen
wsdlgen
yamlgen
ymlgen
confgen
mdgen
rstgen

---

## FILA DE NOVOS GENERATORS (TODO) – Quinta-feira

linguagem: TOML config
extensão: .toml
generator: tomlgen
base: tfgen
status: TODO

linguagem: INI config
extensão: .ini
generator: inigen
base: shgen
status: TODO

linguagem: Environment file
extensão: .env
generator: envgen
base: shgen
status: TODO

linguagem: Bash profile skeleton
extensão: .bash_profile
generator: bashprofilegen
base: shgen
status: TODO

linguagem: Zsh profile skeleton
extensão: .zprofile
generator: zprofilegen
base: shgen
status: TODO

linguagem: Haskell Cabal project
extensão: .cabal
generator: cabalgen
base: hsgen
status: TODO

linguagem: Haskell Stack project
extensão: .stack
generator: stackgen
base: hsgen
status: TODO

linguagem: Nim package
extensão: .nimble
generator: nimblefilegen
base: nimgen
status: TODO

linguagem: CocoaPods spec
extensão: .podspec
generator: podspecgen
base: swiftgen
status: TODO

linguagem: Gradle Kotlin DSL
extensão: .gradle.kts
generator: gradlektsgen
base: ktgen
status: TODO

linguagem: Dockerfile
extensão: .dockerfile
generator: dockerfilegen
base: dockergen
status: TODO

linguagem: Docker Compose alias
extensão: .compose
generator: composegen
base: dockergen
status: TODO

linguagem: Ansible playbook
extensão: .ansible
generator: ansiblegen
base: pygen
status: TODO

linguagem: Ansible Jinja template
extensão: .yaml.j2
generator: yamlj2gen
base: jinjagen
status: TODO

linguagem: macOS/iOS plist
extensão: .plist
generator: plistgen
base: swiftgen
status: TODO

linguagem: Xcode Interface Builder
extensão: .xib
generator: xibgen
base: swiftgen
status: TODO

linguagem: Xcode storyboard
extensão: .storyboard
generator: storyboardgen
base: swiftgen
status: TODO

linguagem: CMake snippet
extensão: .cmake
generator: cmakefilegen
base: cmakegen
status: TODO

linguagem: Makefile snippet
extensão: .makefile
generator: makefilegen
base: makegen
status: TODO

linguagem: Terraform variables
extensão: .tfvars
generator: tfvarsgen
base: tfgen
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

---

Se tu quiser, mano, posso **continuar já planejando sexta-feira**, mantendo o pipeline de 20 novos TODOs por dia, sempre sem repetir nada, até cobrir configs, scripts, templates, DSLs e niche languages.

Quer que eu faça isso?
