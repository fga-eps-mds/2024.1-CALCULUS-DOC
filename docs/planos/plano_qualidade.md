# Plano de Qualidade

## 1. Introdução

Um dos fundamentos essenciais de um produto reside na qualidade que ele oferece. Nesse contexto, a ISO 9126 define a qualidade como a "totalidade de características e critérios de um produto ou serviço que emprega suas capacidades para satisfazer as necessidades declaradas ou implícitas".

Por sua vez, a ISO 25010, lançada em 2011 como uma substituição da ISO 9126, estabelece padrões para a qualidade de produtos de software. Essa norma define qualidade como o grau em que um sistema atende às necessidades expressas e não expressas dos stakeholders, resultando na criação de valor.

A ISO 25010 identifica oito características fundamentais para a qualidade de um produto, que são: adequação funcional, eficiência de desempenho, compatibilidade, usabilidade, confiabilidade, segurança, manutenibilidade e portabilidade.

## 2. Objetivo

A elaboração deste plano tem como propósito detalhar as ferramentas a serem empregadas e as métricas a serem analisadas pela equipe, visando estabelecer os padrões de qualidade do produto e embasar as decisões a serem tomadas. Com isso, podemos citar os seguintes objetivos específicos deste documento:

- Definir os objetivos de qualidade;
- Apresentar formas de atingir os objetivos de qualidade;
- Selecionar e coletar métricas de qualidade;
- Apresentar a compreensão e a aplicação das métricas para o produto;
- Especificar os procedimentos, técnicas e ferramentas que serão utilizados para a garantia da qualidade do produto.

## 3. Objetivos de Qualidade

No âmbito dos objetivos delineados pela norma ISO 25010:2011, a análise da qualidade do projeto é direcionada a três áreas fundamentais: qualidade interna, qualidade externa e qualidade de uso.

A avaliação da qualidade interna e externa visa examinar o próprio produto e está centrada em seis características primordiais: funcionalidade, confiabilidade, usabilidade, eficiência, manutenibilidade e portabilidade. Cada uma dessas características engloba diversas subcaracterísticas, as quais se tornam observáveis externamente durante a utilização do software e são influenciadas pelos atributos internos do produto.

A qualidade de uso, por outro lado, concentra-se em quatro características principais: eficácia, produtividade, segurança e satisfação. Essas características derivam da combinação das seis características de qualidade (interna e externa) previamente definidas pela norma ISO.

Durante a análise da qualidade do projeto, são abordados tanto os aspectos internos quanto os externos do software, considerando as seis características de qualidade. Além disso, é avaliada a experiência do usuário final por meio das quatro características específicas de qualidade de uso. Ao adotar essas abordagens complementares, busca-se realizar uma avaliação abrangente da qualidade do produto sob diferentes perspectivas.

## 4. Verificação e Validação (V&V)

A verificação e validação são processos essenciais no desenvolvimento de produtos, sistemas ou softwares, desempenhando papéis cruciais na garantia de qualidade e na conformidade com requisitos específicos.

### Verificação

A verificação refere-se à avaliação sistemática de um sistema ou componente para determinar se os resultados esperados estão em conformidade com os requisitos predeterminados. Deste modo, é o processo de checar se o produto está sendo construído corretamente, garantindo que cada etapa do desenvolvimento atenda às especificações e normas estabelecidas.

### Validação

A validação está relacionada à confirmação de que o sistema atende às necessidades e expectativas do usuário final. É o processo de assegurar que o produto seja útil e eficaz para o propósito a que se destina. Assim, a validação garante que o produto construído é o produto certo, atendendo aos requisitos e proporcionando valor real aos usuários.

Para alcançar os objetivos de qualidade propostos para o projeto, serão adotadas três técnicas de verificação e validação:

- **Análise estática do código:** Serão utilizadas as funcionalidades do Sonar Cloud como ferramenta de análise estática de código, visando a obtenção de métricas mensuráveis. Essa ferramenta será capaz de identificar possíveis problemas no código e oferecer informações pertinentes à gestão da qualidade do projeto, promovendo uma contribuição valiosa para a tomada de decisões e a identificação de áreas a serem abordadas pela equipe.

- **Testes automatizados:** Serão empregados testes automatizados, abrangendo tanto os testes unitários quanto os de integração. Essa abordagem possibilita a validação não apenas dos cenários esperados, mas também das situações de erro, assegurando o correto funcionamento do software em diversas condições.

- **Validação com os POs:** Reuniões semanais serão realizadas para validar o progresso e obter feedback. Desta forma, é possível realizar a validação contínua da implementação.

## 5. Padrões e Métricas

As principais normas e modelos utilizados no projeto são:

- NBR - ISO/IEC 25010
- Modelo de Qualidade Q-Rapids

### Métricas

As métricas definidas para o monitoramento de qualidade foram:

| Métrica         | Descrição                                           |
|-----------------|-----------------------------------------------------|
| Reliability     | Quantidade de bugs presentes no código fonte        |
| Security Rating | Avaliação de segurança de falhas e vulnerabilidades |
| Maintainability | Quantidade de code smells                           |
| Coverage        | Porcentagem de linhas de código cobertas por testes |
| Duplications    | Densidade em porcentagem de código duplicado        |
| Size            | Quantidade de linhas de declarações, funções, classes, arquivos e comentários |
| Complexity      | Quantidade de complexidade ciclomática e cognitiva  |
| Issues          | Quantidade de issues abertas, fechadas, reabertas, falsa positiva e "won't fix" |

## 6. Testes

O software é um produto da criatividade humana que envolve alta complexidade e, por isso, pode apresentar falhas e inconsistências. Para garantir que o software funcione conforme o esperado, existem os testes, que são processos que verificam a qualidade do software e evitam que os erros afetem o usuário final.

Os testes podem ser classificados em diferentes tipos, de acordo com o nível de abstração do software:

- **Testes de unidade:** São testes que verificam uma parte isolada do código, geralmente uma classe ou um método.
- **Testes de integração:** São testes que verificam o funcionamento de uma funcionalidade ou uma transação completa, envolvendo a interação entre diferentes componentes do software.
- **Testes de sistema:** São testes que simulam o uso real do software por um usuário, verificando se o software atende aos requisitos e expectativas.

## 7. Ferramentas

- **Jest:** Framework de testes para JavaScript.
- **ESLint:** Ferramenta para identificar e reportar padrões encontrados no código ECMAScript/JavaScript, com o objetivo de tornar o código mais consistente e evitar bugs.
- **SonarCloud:** Ferramenta de análise de código que verifica a qualidade do código conforme as métricas e regras estabelecidas.

## 8. Controle de Código

Para garantir a qualidade dos procedimentos, utilizamos uma combinação de tarefas automáticas e manuais. As tarefas automáticas envolvem documentação, controle de versão, código, commits e testes, que são realizados por ferramentas e sistemas que contribuem para a qualidade do software. Essas tarefas serão realizadas com o auxílio de ferramentas e sistemas, garantindo a qualidade do software.

---

Esse plano de qualidade fornece uma visão abrangente das metas, métodos e ferramentas necessários para assegurar a qualidade do produto de software. A adesão a essas diretrizes garantirá que o software atenda aos padrões exigidos e satisfaça as necessidades dos usuários finais.

## 9. Referências


>  Quality-aware Rapid Software Development Project: The Q-Rapids Project. FRANCH X.; LOPEZ L.; FERNÁNDEZ S. M.; ORIOL M.; RODRÍGUEZ P.; TRENDOWICZ A.

>  ISO/IEC 25010. ISO 25000. Software and data quality. 2011. Disponível em: https://iso25000.com/index.php/en/iso-25000-standards/iso-25010. 

>  Metric Definitions. SonarQube. Disponível em: https://docs.sonarqube.org/latest/user-guide/metric-definitions/

>  A Quality Model for Actionable Analytics in Rapid Software Development. FERNÁNDEZ S. M.; JEDLITSCHKA A.; GUZMÁN L.; VOLLMER A. M. Kaiserslautern, Alemanha.


## 4. Histórico de versão

|**Data**|**Descrição**|**Autor(es)**|
|--------|-------------|--------------|
|03/07/2024| Criação do Documento | Davi Matheus |
