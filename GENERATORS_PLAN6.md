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

## FILA DE NOVOS GENERATORS (TODO) – Quarta-feira

linguagem: MJML email template
extensão: .mjml
generator: mjmlgen
base: jsgen
status: TODO

linguagem: EJS template
extensão: .ejs
generator: ejsgen
base: jsgen
status: TODO

linguagem: HJSON config
extensão: .hjson
generator: hjsongen
base: jsgen
status: TODO

linguagem: Jsonnet
extensão: .jsonnet
generator: jsonnetgen
base: jsgen
status: TODO

linguagem: Protocol Buffers
extensão: .proto
generator: protogen
base: pygen
status: TODO

linguagem: Avro IDL
extensão: .avdl
generator: avdlgen
base: pygen
status: TODO

linguagem: Apache Thrift
extensão: .thrift
generator: thriftgen
base: pygen
status: TODO

linguagem: GraphQL schema
extensão: .graphql
generator: graphqlgen
base: jsgen
status: TODO

linguagem: GraphQL query
extensão: .gql
generator: gqlgen
base: jsgen
status: TODO

linguagem: MATLAB module
extensão: .mj
generator: mjgen
base: mgen
status: TODO

linguagem: VHDL
extensão: .vhdl
generator: vhdlgen
base: asmgen
status: TODO

linguagem: Verilog
extensão: .verilog
generator: veriloggen
base: asmgen
status: TODO

linguagem: XML Schema
extensão: .xsd
generator: xsdgen
base: pygen
status: TODO

linguagem: WSDL
extensão: .wsdl
generator: wsdlgen
base: pygen
status: TODO

linguagem: YAML
extensão: .yaml
generator: yamlgen
base: tfgen
status: TODO

linguagem: YAML alias
extensão: .yml
generator: ymlgen
base: tfgen
status: TODO

linguagem: Generic config
extensão: .conf
generator: confgen
base: shgen
status: TODO

linguagem: Markdown skeleton
extensão: .md
generator: mdgen
base: shgen
status: TODO

linguagem: reStructuredText
extensão: .rst
generator: rstgen
base: shgen
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
