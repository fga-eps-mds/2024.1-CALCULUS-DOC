# Dojô  GitHub

## 1. Introdução

Este documento representa contéudo apresentado durante a elaboração do dojo de git  feito pela equipe de EPS para os integrantes de MDS.

Reunião foi elaborada no dia **03/04/2024**

### Git
Git é um **sistema de controle de versão distribuído** usado para rastrear alterações no código fonte durante o desenvolvimento de software.
- Permite que vários desenvolvedores trabalhem simultaneamente no mesmo projeto
- Audita as alterações feitas em arquivos específicos ao longo do tempo.
- Permite que os desenvolvedores revertam para versões anteriores, criem novas funcionalidades em paralelo e colaborem de maneira eficaz.

### GitHub
GitHub é uma **plataforma de hospedagem** baseada na web para projetos Git, fornecendo uma interface visual para o controle de versão e colaboração em equipe.
- Hospeda repositórios Git remotamente na nuvem
- Recursos adicionais: rastreamento de problemas, controle de acesso, integração contínua

## 2. Conceitos chave

### Commit
Um commit é uma operação que salva alterações feitas em arquivos específicos no repositório **local** Git.
- Cada commit é acompanhado de uma mensagem descritiva
- Ajuda a rastrear e documentar o progresso do desenvolvimento

### Branch
Uma branch é uma ramificação independente do código fonte principal.
- Permite desenvolvimento de novas funcionalidades ou correções sem interferir no código principal
- Pode ser mesclada de volta ao código principal após conclusão e testes

### Merge
Merge é o processo de combinar alterações de uma branch em outra.
- Ex.: mesclar branch de desenvolvimento na branch principal

### Pull Request (Pedido de Pull)
Um pull request é uma solicitação para incorporar alterações de uma branch específica em um repositório.
- Usado para revisão de código e integração de novas funcionalidades ou correções de bugs

### Como funciona o GitHub
O GitHub funciona como um repositório remoto para projetos Git.
- Permite envio ("push") de commits, colaboração, criação de branches, abertura de pull requests, revisão de código e mesclagem de alterações

---

## 3. Comandos básicos

### Configuração Inicial
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
### Clonando um Repositório
```bash
git clone _url-do-repositorio.git_
```
### Adicionando Arquivos

```bash
git add nome_do_arquivo
git add .
```
### Fazendo um Commit

```bash
git commit -m "Mensagem do commit"
```
### Enviando commits para um repositório remoto

```bash
git push nome_remoto nome_branch

```
### Verificando o Status

```bash
git status

```
### Atualizando a branch atual

```bash
git fetch

```
### Listando todas as branches

```bash
git branch
```
### Criando uma nova branch

```bash
git branch nome_da_branch

```
### Mudando para uma branch


```bash
git checkout nome_da_branch

```

### Excluindo uma branch

```bash
git branch -d nome_da_branch

```


## 4. Gerenciando Conflitos de Merge

- Abra os arquivos com conflitos e edite-os manualmente
- Adicione os arquivos modificados


```bash
git add nome_do_arquivo

```
- Faça um novo commit


### Rebase interativo 

```bash
git rebase -i commit_referencia 
```
## 5. Aprendizado extra

Caso queira aprender mais de uma forma pratica acessa o site: 

[https://learngitbranching.js.org/](https://learngitbranching.js.org/)


|**Data**|**Descrição**|**Autore(es)**|
|--------|-------------|--------------|
|03/07/2024| Criação do documento | Davi Matheus |
