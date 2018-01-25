Testando funcionalidades do Git e GitHub

# Resumo

**Instalando o Git**
1. Windows: site, abre a página do projeto e clica na opção "Git bash here"
2. Linux: já vem instalada. Ou, no Ubuntu: sudo apt-get install git

**Configurar usuário**
```
git config --global user.name "Seu nome"
```
```
git config --global user.email "Seu  email"
```
Ver o nome e email (para ver separado, é só colocar apenas um comando):
```
git config --global user.name && git config --global user.email
```
**Clonar um projeto do Github (remoto):** altera localmente

Projeto (página) ->  Clone or Download -> copia url -> terminal -> pasta que vai clonar ->
```
git clone <link>
```
**Git Fork:** copia repositório de alguém (clona para o seu github)

## Comandos básicos do Git
**Git Init:** criando um repositório local

Terminal -> entra na pasta do projeto ->
```
git init
```
**Linkando o projeto local com o github (remoto)**

página no github -> new repository -> criar com o mesmo nome (manter padrão) -> copia o link dado -> terminal na raiz (dentro) do projeto ->
```
git remote add origin <link>
```
**Git Status:** verificando o status do projeto

Raiz do projeto ->
``` 
git status
```
**Git add:** adicionando arquivos para serem comitados (submetidos)
Raiz do projeto ->
```
git add <arquivos> [ou] git add * (pega todos os arquivos não traqueados e colocam para serem submetidos)
```
**Git commit:** comitando arquivos
```
git commit -m "mensagem dizendo o que alterou"
```
**Push e pull:** atualizando repositório

*"master" é o nome da sua branch principal e, normalmente, commita para ela (se adicionada uma nova branch e quer colocar seus arquivos nela, é só trocar "master" pelo nome da sua branch)*

Para enviar do local para o remoto:
```
git push origin master
```
Para enviar do remoto para o local:
```
git pull origin master
```
**Git log:** acompanhando os commits (ver as alterações feitas)
```
git log --oneline --decorate --all --graph
```
Ou simplesmente:
```
git log
```
**Git ignore:** restringindo arquivos do commit

### Apagando commits
1. **Git reset soft:** revertendo as coisas

O arquivo volta para ser commitado de novo (recommitar ou adicionar novos arquivos)
```
git reset --soft <numero do commit de onde quer partir>
```
2. **Git reset mixed (padrão)** ou apenas **git reset**

Precisa ser adicionado de novo, ou seja, pode ser ser alterado/editado e depoiis adicionar
```
git reset [--mixed] <numero do commit de onde quer partir>
```
3. **Git reset hard:** brute force

É o reset mais perigoso, pois ele apaga as arquivos e volta para o commit pedido
```
git reset --hard <numero do commit de onde quer partir>
```
