# Estrutura Analítica de Riscos


## 1. Definição

O planejamento de riscos é uma parte crucial do planejamento de um projeto. Ao identificar os possíveis riscos, é possível definir estratégias para minimizar os impactos que esses riscos podem causar no projeto. Isso envolve a identificação dos riscos, análise da probabilidade de ocorrência e impacto no desenvolvimento da aplicação, e a definição de estratégias para mitigação dos riscos [1].

A estrutura analítica de riscos (EAR) é uma ferramenta que permite a identificação, análise e priorização dos riscos durante o desenvolvimento do projeto. Para facilitar a identificação dos riscos, a EAR é dividida em categorias: riscos organizacionais, riscos de gerenciamento do projeto, riscos técnicos e riscos externos [2]. Essa categorização pode ser visualizada no diagrama a seguir:

### Externo
- **Faculdade:** Riscos relacionados a outras disciplinas que acontecem durante o projeto.
- **Saúde:** Riscos relacionados à saúde dos integrantes e clientes do projeto, incluindo a possibilidade de retorno ao ensino à distância.
- **Profissional:** Riscos relacionados às vidas profissionais dos integrantes.
- **Cliente:** Riscos associados às indisponibilidades dos clientes.

### Organizacional
- **Priorização:** Riscos associados a possíveis priorizações equivocadas dos requisitos.
- **Financiamento:** Riscos inerentes aos custos do projeto e possíveis financiamentos monetários.
- **Habilidades individuais:** Riscos relacionados às capacidades e habilidades de cada integrante.

### Técnico
- **Dependências de projeto:** Riscos relacionados a dependências externas utilizadas no projeto.
- **Tecnologia:** Riscos associados às tecnologias utilizadas.
- **Infraestrutura:** Riscos relacionados à infraestrutura do projeto.
- **Arquitetura:** Riscos relacionados à arquitetura utilizada no projeto.
- **Qualidade:** Riscos associados às características de qualidade do produto.

### Gerenciamento do Projeto
- **Pessoas:** Riscos relacionados à gerência das pessoas integrantes do projeto.
- **Estimativas:** Riscos relacionados à definição e alterações das estimativas.
- **Planejamento:** Riscos relacionados ao planejamento do projeto.
- **Execução:** Riscos associados à execução do projeto.
- **Comunicação:** Riscos associados à comunicação entre membros e entre clientes.


## 2. Análise Quantitativa
### Probabilidade
| Probabilidade | Intervalo | Peso |
|---------------|-----------|------|
| Muito Alta    | 81 ~ 100   | 5    |
| Alta          | 61 ~ 80    | 4    |
| Média         | 41 ~ 60    | 3    |
| Baixa         | 21 ~ 40    | 2    |
| Muito Baixa   | 0 ~ 20     | 1    |

### Impacto
| Impacto      | Descrição                              | Peso |
|--------------|----------------------------------------|------|
| Muito Alto   | O impacto inviabiliza o projeto        | 5    |
| Alto         | Grande impacto no desenvolvimento      | 4    |
| Médio        | Certo impacto, mas facilmente recuperado| 3    |
| Baixo        | Pouco impacto no desenvolvimento       | 2    |
| Muito Baixo  | Impacto pouco expressivo               | 1    |

## 3. Prioridade (Probabilidade x Impacto)
Multiplicando-se a probabilidade de um risco acontecer pelo seu impacto, pode-se calcular a prioridade do risco. Esses valores determinam a urgência de medidas de mitigação. A matriz abaixo ilustra essa relação:

| Probabilidade x Impacto | Muito Baixo | Baixo | Médio | Alto | Muito Alto |
|-------------------------|-------------|-------|-------|------|------------|
| Muito Alta              | 5           | 10    | 15    | 20   | 25         |
| Alta                    | 4           | 8     | 12    | 16   | 20         |
| Média                   | 3           | 6     | 9     | 12   | 15         |
| Baixa                   | 2           | 4     | 6     | 8    | 10         |
| Muito Baixa             | 1           | 2     | 3     | 4    | 5          |

## 4. Planilha de Riscos
Compreendendo as fontes de riscos (Organizacional, Externo, Gerenciamento de Projeto e Técnico), foram criadas tabelas detalhando suas probabilidades, impactos, prevenções e respostas. Esse detalhamento auxiliou a equipe a gerenciar e se organizar melhor durante o projeto.

### Externo
| ID | Risco                                                | Probabilidade | Impacto | Prevenção                                        | Resposta                                                      |
|----|------------------------------------------------------|---------------|---------|-------------------------------------------------|---------------------------------------------------------------|
| R1 | Indisponibilidade do cliente no decorrer do projeto  | Médio         | Alto    | Organizar, comunicar e definir horários         | Repriorizar/Alterar para problemas que não envolvem o cliente |
| R2 | Indisponibilidades dos integrantes por motivos profissionais | Alto    | Médio   | Planejamento e divisão de tarefas               | Redistribuição de tarefas entre a equipe                      |
| R3 | Indisponibilidades dos integrantes por motivos de saúde        | Médio         | Baixo   | Estar atento às medidas de saúde                | Redistribuição de tarefas entre a equipe                      |
| R4 | Indisponibilidades dos integrantes por demandas da faculdade   | Médio         | Médio   | -                                               | Redistribuição de tarefas entre a equipe                      |

### Organizacional
| ID | Risco                                                 | Probabilidade | Impacto  | Prevenção                                    | Resposta                                                      |
|----|-------------------------------------------------------|---------------|----------|---------------------------------------------|---------------------------------------------------------------|
| R5 | Realização de pareamentos de forma ineficiente        | Baixo         | Médio    | Entendimento das habilidades da equipe       | Reparear ou transformar pareamento em um grupo maior          |
| R6 | Priorização equivocada das tarefas                    | Médio         | Muito Alto | Entendimento do produto, avaliações com clientes, comunicação entre a equipe | Repriorizar e levantar novos requisitos se necessário          |
| R7 | Familiaridade com a tecnologia                        | Médio         | Médio    | Avaliação do conhecimento da equipe          | Realização de treinamentos e divulgação do conhecimento        |
| R8 | Financiamento do projeto                              | Baixo         | Baixo    | -                                             | Avaliação dos requisitos, apresentação do projeto, comunicação com os clientes |

### Técnico
| ID  | Risco                                              | Probabilidade | Impacto  | Prevenção                                   | Resposta                                  |
|-----|----------------------------------------------------|---------------|----------|--------------------------------------------|-------------------------------------------|
| R9  | Utilização de bibliotecas desatualizadas/comprometidas | Muito Baixo  | Alto     | Avaliação antes do uso                     | Implementação própria ou mudança de biblioteca |
| R10 | Utilização de tecnologias que não atendem às demandas | Muito Baixo  | Médio    | Avaliação prévia da tecnologia             | Refatorações de código                    |
| R11 | Infraestrutura definida não atende o projeto       | Alto          | Muito Alto | Avaliação dos custos e capacidades         | Alteração da infraestrutura               |
| R12 | Arquitetura definida não atende o projeto          | Baixo         | Alto     | Análise e avaliação da arquitetura         | Alteração da arquitetura com refatorações |
| R13 | Qualidade de código                                | Médio         | Alto     | Análise estática de código, avaliação de padrões de qualidade | Refatorações de código                    |

### Gerenciamento de Projeto
| ID  | Risco                                               | Probabilidade | Impacto  | Prevenção                                    | Resposta                                         |
|-----|-----------------------------------------------------|---------------|----------|---------------------------------------------|--------------------------------------------------|
| R14 | Perda de reuniões da equipe                         | Baixo         | Médio    | Análise do quadro de disponibilidades       | Realização de reuniões rápidas, gravação das reuniões |
| R15 | Saída de membros da equipe                          | Baixo         | Médio    | Ajudar membros com dificuldades, avaliações de stress e saúde | Realocação dos membros nas atividades             |
| R16 | Subestimativas ou Superestimativas                  | Alto          | Médio    | Avaliação das estimativas com a equipe      | Reavaliação das estimativas                       |
| R17 | Falta de planejamento                               | Baixo         | Alto     | Planejamento antecipado                     | Replanejamento e realocação de membros            |
| R18 | Atrasos nas execuções das atividades                | Médio         | Alto     | Entendimento dos cronogramas e capacidades  | Reavaliação do cronograma e das tarefas esperadas |
| R19 | Falta de comunicação entre a equipe e clientes      | Baixo         | Alto     | Manter canal de comunicação ativo           | Propor atividades para interação do grupo         |

## 5. Burndown de Riscos
Para melhorar a visualização do desenvolvimento dos riscos durante a execução do projeto, foram utilizados quadros de burndown para cada agrupamento de risco. Esses gráficos permitem observar e comparar a evolução dos riscos de acordo com as sprints do projeto.

<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vT1dqQpT91WdcLBHzKcK9wLJ1z7ySFbQykfJaNVRufi2uC4qfxiWmvQbE-oj-JxXPBdh1RV49J1bHcd/pubhtml?widget=true&amp;headers=false" width="100%" height="800"></iframe>

## 6. Referências

> FREITAS, Renata. Aplique o Plano de Gerenciamento de Riscos no seu negócio. Disponível em: https://www.glicfas.com.br/plano-de-gerenciamento-de-riscos/.

## 7. Histórico de versão

|**Data**|**Descrição**|**Autor(es)**|
|--------|-------------|--------------|
|03/07/2024| Criação do Documento | Davi Matheus |
