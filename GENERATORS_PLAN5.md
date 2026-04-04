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

---

## FILA DE NOVOS GENERATORS (TODO) – Terça-feira

linguagem: CoffeeScript TypeScript
extensão: .coffee.ts
generator: coffeetsgen
base: tsgen
status: TODO

linguagem: Vuex module
extensão: .vuex
generator: vuexgen
base: vuegen
status: TODO

linguagem: Serverless config
extensão: .sls
generator: slsgen
base: jsgen
status: TODO

linguagem: HashiCorp config
extensão: .hcl
generator: hclgen
base: tfgen
status: TODO

linguagem: Puppet manifest
extensão: .puppet
generator: puppetgen
base: tfgen
status: TODO

linguagem: Puppet snippet
extensão: .pp
generator: ppgen
base: tfgen
status: TODO

linguagem: Jinja template
extensão: .jinja
generator: jinjagen
base: pygen
status: TODO

linguagem: ERB template
extensão: .erb
generator: erbgen
base: rbgen
status: TODO

linguagem: Mustache template
extensão: .mustache
generator: mustachegen
base: jsgen
status: TODO

linguagem: Handlebars template
extensão: .hbs
generator: hbsgen
base: jsgen
status: TODO

linguagem: Docker Compose
extensão: .docker-compose.yml
generator: dcgen
base: dockergen
status: TODO

linguagem: Gradle build
extensão: .gradle
generator: gradlegen
base: javagen
status: TODO

linguagem: Bash RC skeleton
extensão: .bashrc
generator: bashrcgen
base: shgen
status: TODO

linguagem: Zsh RC skeleton
extensão: .zshrc
generator: zshrcgen
base: shgen
status: TODO

linguagem: Fish shell config
extensão: .fish
generator: fishgen
base: shgen
status: TODO

linguagem: Vim config
extensão: .vim
generator: vimgen
base: shgen
status: TODO

linguagem: Emacs config
extensão: .emacs
generator: emacsgen
base: elgen
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
