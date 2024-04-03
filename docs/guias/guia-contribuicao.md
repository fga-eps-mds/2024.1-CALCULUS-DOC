# Guia de Contribuição

Este guia tem como objetivo te ajudar a contribuir com o nosso projeto, por favor leia com atenção!

## 1. Antes de Começar

Os detalhes de como instalar e executar os projetos podem ser encontrados no [README.md](https://github.com/fga-eps-mds/2024.1-CALCULUS-DOC#readme).

## 2. Reportando Bugs

Você encontrou um bug?

- Sugestões de melhoria são rastreadas através de [_issues_](https://guides.github.com/features/issues/) e [_pull requests_](https://guides.github.com/activities/hello-world/#pr) no GitHub. Verifique se nenhuma _issue_ ou _pull request_ foi criada por outra pessoa com o mesmo bug.

- Se não, crie uma _issue_ explicando o problema e adicionando novas informações detalhadas que ajudem a reproduzi-lo.

## 3. Sugerindo Melhorias

Você pode sugerir as melhorias que achar pertinente. Pedimos apenas que tente incluir o máximo de detalhes possíveis e que verifique se nenhuma _issue_ ou _pull request_ já foi criado por outra pessoa com a mesma sugestão.

Caso seja algo novo, você tem duas alternativas:

- Criar uma nova _issue_.
- Compartilhar a sua sugestão com outros participantes e mantenedores do projeto.

Em ambos, tente usar uma linguagem clara e com o máximo de detalhes. Qual a motivação, qual problema resolveria e possíveis desafios, por exemplo, são importantes para entender o que você precisa. Esse é um projeto de código aberto, mantido por voluntários. Frequentemente precisamos escolher bem o que vamos fazer com os recursos que temos.

## 4. Criando Pull Requests

Você decidiu contribuir para o projeto!

Faça um _fork_ do projeto e crie uma nova _branch_.
Mais detalhes [aqui](https://help.github.com/pt/enterprise/2.17/user/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork).


Aqui algumas dicas:

- Caso decida trabalhar em alguma _issue_, comente na _issue_ escolhida. Dessa forma, outras pessoas saberão que tem alguém trabalhando nela. Caso tenha ficado perdido ou com dúvidas, peça ajuda.

- Caso tenha visto algo pontual, como um _typo_ ou algo que pode ser corrigido e testado rapidamente e não envolva mudanças estruturais, você é bem-vindo a abrir um novo PR também.

- Antes de qualquer coisa, tente rodar o projeto localmente.

- Rode os testes localmente. Além de ser uma boa prática, previne idas e vindas nas revisões.

- Embora o código esteja escrito em inglês, por convenção, as mensagens de _commit_, comentários, _pull requests_, _issues_, e demais comunicações do projeto deverão ser escritas em português.

- Marque a opção "Permitir edição pelos mantenedores". Assim poderemos fazer modificações de emergência mantendo o _pull request_ aberto por você.


Nós possuimos também um template para o _pull request_ que seguirá da seguinte forma:

Descrição
- Criando e arrumando alguns docs

 Revisão 
<!-- Verifica se os critérios estabelecidos na issue foram realizados -->
- [x] mkdocs 
- [x] Prototipo de alta
- [x] User  Story Template

 Pre-merge checklist 

- [x] O Pull Request refere-se a um único assunto, um título claro e uma descrição em frases gramaticalmente corretas e completas.
- [x] A branch está atualizada com a branch main.
- [x] Os commits atendem o padrão especificado na política de contribuição.

## 5. Política de Branch

As branches serão nomeadas seguindo de maneira padronizada para a melhorar a organização do projeto. Utilizamos as branches apenas para desenvolvimento de código sendo que todas as branches devem ser criadas a partir da **main** e devem estar nomeadas da seguinte maneira:

**OBSERVAÇÃO:** A fim de evitar dores de cabeça, não utilizar caracteres especiais na criação de branches.


```bash
(tipo)-(issue)-(descrição)

Exemplo: 
tipo: doc
issue: #24
descrição: Criar guia de contribuição

doc-24-guiaDeContribuicao
```

Sendo que X representa número da issue atribuída seguido pelo nome do documento a ser criado ou modificado, como destacado anteriormente. Em ocasiões em que não se está trabalhando com nenhum documento em específico, então deve-se colocar o nome da issue correspondente.

## 6. Política de Commit

### 6.1 Formato:

Os commits devem ser feitos de maneira clara e objetiva respeitando os padrões comentados a seguir:

- Devem possuir um tipo, número da issue associada e o assunto.
- Devem ser escritas em português.
- Os verbos devem estar no gerúndio.

Portanto a formatação do commit será: `<tipo>(#número da issue): assunto`

```bash
feat(#04): Desenvolvendo cadastro da impressora



Co-authored-by: fernandes-natanael <filhonatanael01@gmail.com>

```

#### 6.1.1 Tipos:
- feat: quando adicionar nova funcionalidade
- doc: quando escrever documentação
- repeat: quando alguma alteração for feita
- refact: refatoração ou otimização
- bug: quando consertar um bug
- remove: quando remover código ou arquivos

|**Data**|**Descrição**|**Autore(es)**|
|--------|-------------|--------------|
|04/02/2024| Criação do documento | Natanael Fernandes |




