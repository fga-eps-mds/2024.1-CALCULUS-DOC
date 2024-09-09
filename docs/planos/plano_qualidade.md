# Plano de Qualidade
## 1. Introdução

A qualidade de um produto de software é um dos seus pilares essenciais, garantindo que ele atenda às necessidades dos usuários e ofereça valor real. Segundo a ISO 25010, que substituiu a ISO 9126 em 2011, a qualidade de um software é definida como o grau em que um sistema atende às necessidades expressas e não expressas dos stakeholders, resultando na criação de valor.

A ISO 25010 identifica oito características fundamentais para a qualidade de um produto: adequação funcional, eficiência de desempenho, compatibilidade, usabilidade, confiabilidade, segurança, manutenibilidade e portabilidade.

Este documento visa detalhar as ferramentas, métricas e procedimentos que serão utilizados para assegurar a qualidade do produto, com foco na testabilidade e na aderência ao modelo de qualidade Q-Rapids.

## 2. Objetivo

Este plano tem como propósito estabelecer as diretrizes de qualidade do projeto, assegurando que todas as etapas do desenvolvimento sejam conduzidas de maneira a garantir um produto final de alta qualidade. Especificamente, os objetivos deste documento são:

- Definir os objetivos de qualidade;
- Estabelecer métodos para alcançar os objetivos de qualidade;
- Selecionar e coletar métricas de qualidade;
- Apresentar a compreensão e a aplicação das métricas para o produto;
- Especificar os procedimentos, técnicas e ferramentas que serão utilizados para a garantia da qualidade do produto;
- Incluir práticas de testabilidade para assegurar que o código seja facilmente testável, promovendo a manutenção da qualidade ao longo do tempo.

## 3. Objetivos de Qualidade

Com base na norma ISO 25010:2011, o plano de qualidade do projeto foca em três áreas principais: qualidade interna, qualidade externa e qualidade de uso.

- **Qualidade Interna e Externa:** Estas são avaliadas através de características como funcionalidade, confiabilidade, usabilidade, eficiência, manutenibilidade e portabilidade. A qualidade interna se refere aos atributos que são observados durante o processo de desenvolvimento, enquanto a qualidade externa é avaliada quando o produto está em uso.
  
- **Qualidade de Uso:** Concentra-se em quatro características principais: eficácia, produtividade, segurança e satisfação. Essas características avaliam a experiência do usuário final, garantindo que o software atenda às suas expectativas.

Além dessas áreas, a **testabilidade** é considerada um fator crítico para garantir que o produto seja fácil de testar, o que, por sua vez, contribui para a manutenção da qualidade ao longo do ciclo de vida do software.

## 4. Verificação e Validação (V&V)

### 4.1. Verificação

A verificação é o processo sistemático de avaliação de um sistema ou componente para determinar se os resultados de uma fase de desenvolvimento atendem aos requisitos estabelecidos para essa fase. Esta abordagem visa garantir que o software esteja sendo construído corretamente, em conformidade com as especificações.

### 4.2. Validação

A validação assegura que o sistema atende às necessidades e expectativas dos usuários finais, garantindo que o produto certo está sendo construído. A validação será realizada de forma contínua ao longo do desenvolvimento, com validações regulares realizadas com os Product Owners.

### 4.3. Técnicas de V&V

Para alcançar os objetivos de qualidade, serão adotadas as seguintes técnicas:

- **Análise Estática do Código:** Utilização do SonarCloud para analisar o código e coletar métricas relacionadas a code smells, duplicações, complexidade e cobertura de testes. A análise estática é fundamental para identificar problemas de qualidade no código que possam comprometer a manutenibilidade e a testabilidade do software.

- **Testes Automatizados:** Implementação de testes unitários e de integração automatizados para garantir que cada componente funcione conforme o esperado e que a integração entre os componentes seja robusta. A cobertura de código será monitorada para assegurar que as áreas críticas do software estão devidamente testadas.

- **Validação com POs:** Reuniões semanais serão realizadas com os Product Owners para validar o progresso e obter feedback. Este processo contínuo de validação ajuda a garantir que o desenvolvimento esteja alinhado com as expectativas dos stakeholders e com os objetivos de qualidade.

## 5. Padrões e Métricas

As principais normas e modelos utilizados no projeto são:

- **NBR - ISO/IEC 25010:** Padrão internacional para a qualidade de produtos de software.
- **Modelo de Qualidade Q-Rapids:** Um modelo baseado em métricas de qualidade que permite a avaliação contínua e orientada por dados do software.

### 5.1. Métricas

As métricas definidas para monitorar a qualidade do projeto, conforme o modelo Q-Rapids e alinhadas com a testabilidade e qualidade de produto, incluem:

| Métrica         | Descrição                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------|
| **Reliability** | Quantidade de bugs presentes no código fonte.                                                   |
| **Security Rating** | Avaliação de segurança de falhas e vulnerabilidades, conforme as diretrizes de segurança do projeto.|
| **Maintainability** | Quantidade de code smells identificados no código, que podem impactar a manutenibilidade e testabilidade.|
| **Coverage**    | Porcentagem de linhas de código cobertas por testes automatizados, com um valor de referência mínimo de 80%.|
| **Duplications** | Densidade de código duplicado em porcentagem, que deve ser mantida abaixo de 5% para facilitar a manutenção.|
| **Size**        | Quantidade de linhas de declarações, funções, classes, arquivos e comentários, usada para avaliar a complexidade geral.|
| **Complexity**  | Medição da complexidade ciclomática e cognitiva, com foco em manter a complexidade baixa para melhorar a testabilidade.|
| **Issues**      | Quantidade de issues abertas, fechadas, reabertas, falsa positiva e "won't fix", usada para monitorar a saúde do projeto.|

### 5.2. Valores de Referência

Para cada métrica, foram definidos valores de referência que servirão como indicadores de qualidade e auxiliarão na tomada de decisões:

- **Coverage:** 80% de cobertura mínima das linhas de código.
- **Duplications:** Menos de 0% de duplicação de código.
- **Complexity:** Manter a complexidade ciclomática abaixo de 10 por método/função.

Esses valores de referência são críticos para garantir que o software permaneça testável e de alta qualidade ao longo de seu ciclo de vida.

## 6. Testes

Os testes desempenham um papel crucial na garantia da qualidade do software. Eles verificam se o software funciona conforme o esperado e ajudam a evitar que erros afetem o usuário final.

### 6.1. Tipos de Testes

- **Testes de Unidade:** Verificam a funcionalidade de componentes isolados do sistema, como métodos ou classes, garantindo que cada parte funcione de forma independente.
- **Testes de Integração:** Avaliam a interação entre diferentes componentes do sistema, assegurando que eles funcionem bem em conjunto.
- **Testes de Sistema:** Simulam o uso real do software para verificar se ele atende aos requisitos e expectativas do usuário final.

### 6.2. Implementação de Testes

Os testes serão implementados de forma a maximizar a cobertura de código e garantir que todas as funcionalidades críticas sejam validadas. O foco na **testabilidade** garante que o código seja estruturado de maneira a facilitar a criação e execução de testes, permitindo detecção precoce de defeitos.

## 7. Ferramentas

As ferramentas a serem utilizadas para suportar as práticas de qualidade incluem:

- **Jest:** Framework de testes para JavaScript, utilizado principalmente para testes de unidade.
- **ESLint:** Ferramenta para identificar e reportar padrões inconsistentes no código ECMAScript/JavaScript, contribuindo para a qualidade e manutenibilidade do código.
- **SonarCloud:** Plataforma de análise de código que verifica a qualidade do código conforme as métricas e regras estabelecidas, incluindo cobertura de testes, duplicação, complexidade, entre outros.

## 8. Controle de Código

Para garantir a qualidade dos procedimentos, o controle de código será realizado por meio de tarefas automáticas e manuais, envolvendo:

- **Documentação e Controle de Versão:** Uso de sistemas de controle de versão para gerenciar o histórico de mudanças no código, facilitando o rastreamento de alterações e a colaboração entre membros da equipe.
- **Commits e Pull Requests:** Revisões de código serão realizadas por meio de pull requests, garantindo que todas as mudanças passem por uma análise rigorosa antes de serem integradas ao código base.
- **Testes Automatizados:** Execução de testes automatizados para cada commit, assegurando que novas alterações não introduzam regressões.


## 9. Referências

> Quality-aware Rapid Software Development Project: The Q-Rapids Project. FRANCH X.; LOPEZ L.; FERNÁNDEZ S. M.; ORIOL M.; RODRÍGUEZ P.; TRENDOWICZ A.

> ISO/IEC 25010. ISO 25000. Software and data quality. 2011. Disponível em: https://iso25000.com/index.php

> Quality-aware Rapid Software Development Project: The Q-Rapids Project. FRANCH X.; LOPEZ L.; FERNÁNDEZ S. M.; ORIOL M.; RODRÍGUEZ P.; TRENDOWICZ A.

> ISO/IEC 25010. ISO 25000. Software and data quality. 2011. Disponível em: https://iso25000.com/index.php/en/iso-25000-standards/iso-25010.

> Metric Definitions. SonarQube. Disponível em: https://docs.sonarqube.org/latest/user-guide/metric-definitions/

> A Quality Model for Actionable Analytics in Rapid Software Development. FERNÁNDEZ S. M.; JEDLITSCHKA A.; GUZMÁN L.; VOLLMER A. M. Kaiserslautern, Alemanha.

---

## 10. Histórico de Versão

| **Data**   | **Versão** | **Descrição**                                                           | **Autor(es)**     |
|------------|------------|-------------------------------------------------------------------------|-------------------|
| 03/07/2024 | 1.0        | Criação do documento                                                    | Davi Matheus      |
| 01/09/2024 | 1.1        | Revisão e aperfeiçoamento com foco em testabilidade e qualidade         | Paulo Gontijo      |
| 05/09/2024 | 1.2        | Ajuste das métricas         | Paulo Gontijo      |
