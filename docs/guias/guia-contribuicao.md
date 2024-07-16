# Git Flow
Este documento tem o objetivo de consolidar padrões de uso do git no desenvolvimento de nossa aplicação.
***

## Motivação
Conforme nomeação do documento, neste projeto usaremos uma adaptação do padrão **git flow**. Este conceito tem seu fundamento
na organização de repositórios, atribuindo políticas de uso e restrições de segurança, sempre com objetivo de cumprir com
as práticas mais adequadas, observadas e aperfeiçoadas ao longo do tempo.

***

## Políticas de Contribuição
***
### Idioma
Por se tratar de um projeto univesitário do Brasil, por padrão, usaremos o idioma nativo, **Português**. Poŕem, sabe-se
que a área de engenharia de software possui muitos conteúdos e termos em outros idiomas, como o próprio *git flow*, portanto 
também será aceito o uso de **terminologias** no idioma **Inglês**. 

***
### Ética
O projeto espera do colaborador bom senso na escrita, além de não permitir a produção contribuições com linguagem ofensiva.
A proposta perpassa pela interação direta com a vivência e moradia de pessoas, portanto também assume-se o compromisso 
de não violar o respeito em qualquer aspecto, sobretudo étnico racial, religião e sexualidade.

***
## Branches
### Fluxo de Branches
Para garantir um fluxo de trabalho contínuo e de forma padronizada, possibilitando o rastreamento das funcionalidades
desenvolvidas e facilitando o desenvolvimento contínuo. Os conceitos chave para implementação da estratégia serão:

* `Main`
Branch de **produção**, responsável por abrigar o código do último release. 

* `Qas`
Branch de **verificação**, representa uma etapa intermediária entre o processo de desenvolvimento e produção. Nesta etapa
são realizados os eventuais testes e revisões que antecedem o processo de deploy.

* `Dev`
Branch de **desenvolvimento**, tem a função e prioridade de ser a branch mais atualizada, a qual os desenvolvedores utilizaram
de ponto de partida para desenvolver as *features branches*.

* `Feature`
Branch de desenvolvimento de **funcionalidade**, representa a branch de trabalho sob uma determinada funcionalidade, tarefa, 
correção de bugs e afins.

* `Fix`
Branch de **correção**, possibilita os desenvolvedores de corrigirem eventuais funcionalidades quebradas. 

#### Exemplo do fluxo de branches
Abaixo segue a ilustração do fluxo:


![Figura 1: Fluxo de Branches](../assets/gitflow/diagrama-gitflow.drawio.png) 
Figura 1: Fluxo de Branches

Autor: Calculus Team

### Nomenclatura de Branch
É importante que a branch de **funcionalidade** seja criada seguindo o padrão: 

* **(número-da-issue)-(nome-da-issue)**

e seja criada a partir da branch de desenvolvimento `Dev` e deve-se trocar os espaços no nome para '-'.

A branch de **correção** deve ser criada no padrão: 

- **fix#(número-da-issue)/nome-da-issue**

e originar-se da branch que apresentou o erro, exceto se for a branch `Main`. Em caso de exceção, deve-se crira uma branch a partir de `Dev`.


## Commits

As informações abaixo referem-se aos padrões de escrita de commits do nosso repositório:

### Commits Atômicos
Sempre dividir o trabalho em **pequenos e significativos commits**, de maneira que cada commit implemente apenas uma
funcionalidade.

### Anatomia do Commit
Na estrutura do padrão convencionado, possuímos as variáveis **tipo**, **número da issue**, **assunto** e **corpo**.
A anatomia do commit deve seguir o formato determinado abaixo:

```
[tipo](#número da issue): assunto 
> corpo
```

#### Observações
> As opções permitidas para o campo `tipo` são:

> - `feat`: nova funcionalidade
> - `docs`: relacionado a documentação
> - `refact`: refatoração  de código
> - `test`: adicionar/refatorar testes
> - `fix`: correções

> As regras para o campo `assunto` são:

> - Mensagem curta e sucinta
> - Todo texto deve estar sempre em letras minúsculas

> As regras para o campo `corpo` são:

> - Máximo de 100 caracteres
> - Detalhar minimamente as novas alterações
> - Deve conter `o que` e o `por que` foi feito

### Exemplo de commit:
Abaixo segue um exemplo de commit feito no padrão do projeto:
```git
[refact](#25): ajustando página de login  
Refatoração do método de login pois a execução estava muito lenta. 
```

***
## Pull Request
#### Passo 1 
Por meio do processo de **pull request**, realizado no github, toda nova funcionalidade deve ser integrada à branch de
desenvolvimento, seguindo o fluxo `Feature -> Dev`.

#### Passo 2
Uma vez que a branch de desenvolvimento esteja com todos os artefatos necessários para se fazer deploy, deve-se criar um
pull request de `Dev -> Qas`.

#### Passo 3
A branch de validação (qas) deve ser **revisada por todos os membros antes de relizar-se o merge para a branch Main**. 
Desta forma pode-se adicionar mais uma camada de validação pré-deploy e conferir mais acertividade nas entregas. Após 
concluir a validação, 

> Dentre as atividades obrigatórias de um pull request, estão a **revisão em pares** da entrega e **ajuste de eventuais conflitos**. 

> O colaborador que abrir o pull request **não pode mergear o mesmo sem revisões de terceiros**.

Para publicar uma nova versão estável da aplicação na branch `main` é necessário realizar um **Pull Request** da branch `qas` para a `main`. Assim garantido a revisão da nova versão do código.

### Nomenclatura
Toda branch deve estar necessariamente estar relacionada a uma funcionalidade ou correção, logo a uma _Issue_. O nome da branch deve estar em PORTUGUÊS seguindo o padrão:

- Para funcionalidades: `feat#(número-da-issue)/descrição-curta`
- Para correções: `fix#(número-da-issue)/descrição-curta`

Exemplo: `feat#75/criar-jornada`

***
## Histórico de Versões

| Versão |    Data    |           Descrição           |                                                    **Autore(es)**                                                   |
|:------:|:----------:|:-------------------------------:|:-----------------------------------------------------------------------------------------------------------:|
|  1.0   |04/02/2024| Criação do documento | Natanael Fernandes |
|  1.1   | 08/07/2024 | Atualização de documento e diagrama | Paulo Gontijo |



