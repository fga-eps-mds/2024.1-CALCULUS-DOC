
# Documento de Arquitetura

## 1. Introdução

Este documento tem como principal objetivo fornecer uma visão abrangente e estruturada da arquitetura do software Calculos. Utilizando diferentes visões arquiteturais, ele destaca diversos aspectos do sistema, proporcionando uma visão geral completa. A descrição abrange as principais decisões de design, componentes, módulos, interações e estrutura do software, facilitando assim o entendimento da arquitetura para os desenvolvedores.

### 1.1. Visão Geral

Este documento está estruturado da seguinte forma:

- Introdução
- Representação arquitetural
- Visão Lógica
- Referências bibliográficas
- Histórico de versão

## 2. Representação Arquitetural

### 2.1. Diagrama de Relações

<iframe frameborder="0" style="width:100%;height:308px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=I-6fpici55m38HMQ_MQw#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>

O estilo arquitetural de microsserviços consiste em uma abordagem onde a aplicação é composta por serviços menores, implementados de forma independente e com baixo acoplamento. Esses serviços, organizados por recursos de negócios, comunicam-se entre si normalmente por meio de APIs.

A arquitetura de microsserviços acelera o desenvolvimento e facilita a escalabilidade da aplicação. Esse padrão será utilizado no Calculos, com cada microsserviço possuindo sua própria base de dados independente.

### 2.2. Representação dos serviços

#### 2.2.1. Gateway

O gateway é responsável por atuar como a interface entre o usuário e os demais serviços da aplicação, garantindo autenticação e autorização. Além disso, ele facilita a comunicação entre os serviços, servindo como ponto central para a gestão de requisições e respostas. No Caluculos, utilizaremos RabbitMQ para gerenciar a comunicação assíncrona entre os microsserviços, assegurando um fluxo de dados eficiente e confiável.

#### 2.2.2. Usuário

O serviço de usuário é responsável pela gestão completa dos usuários da aplicação. Isso inclui o registro, autenticação, atualização de informações, gerenciamento de permissões e controle de acesso, garantindo uma experiência segura e personalizada para cada usuário.

#### 2.2.3. Jornadas

O serviço de jornadas é responsável pela gestão das jornadas na aplicação. Isso inclui a criação, atualização e exclusão de jornadas, bem como a administração das inscrições dos clientes, permitindo que eles ingressem e participem das jornadas de forma eficiente e organizada.

#### 2.2.4. Gamificação

O serviço de gamificação é responsável por gerenciar a progressão dos usuários nas trilhas, acompanhando o avanço passo a passo nos exercícios. Ele também administra o sistema de recompensas, incentivando a participação ativa dos usuários através de pontos, medalhas e outros incentivos, promovendo uma experiência mais envolvente e motivadora na aplicação.

### 2.3. Tecnologias

#### 2.3.1. NextJS

O Next.js é um framework de desenvolvimento baseado em React que permite a criação de interfaces de usuário robustas e escaláveis. Ele facilita a renderização no servidor, a geração de páginas estáticas e a integração com APIs, proporcionando uma experiência de desenvolvimento otimizada. Com Next.js, é possível criar UIs complexas de forma eficiente, garantindo alta performance e SEO aprimorado. O Next.js será utilizado no front-end.

#### 2.3.2. NestJS

O NestJS é um framework de desenvolvimento baseado em Node.js que facilita a criação de aplicações escaláveis e eficientes. Ele utiliza uma arquitetura modular e orientada a objetos, permitindo a organização de código em módulos, controladores e serviços. Com suporte integrado para TypeScript, injeção de dependências e uma estrutura robusta para desenvolvimento de APIs e microsserviços, o NestJS é ideal para construir back-ends robustos e manuteníveis. O NestJS será utilizado no back-end.

#### 2.3.3. MongoDB

O MongoDB é um banco de dados NoSQL de código aberto reconhecido pela sua flexibilidade e escalabilidade. Ele é projetado para lidar com grandes volumes de dados de forma eficiente e oferece esquemas dinâmicos, permitindo a modelagem de dados de maneira mais livre em comparação com bancos de dados relacionais. O MongoDB suporta operações de leitura e gravação de alto desempenho, distribuição automática de dados e consultas complexas usando sua linguagem de consulta avançada. Será utilizado para gerenciar as bases de dados dos serviços da aplicação, proporcionando agilidade, escalabilidade e suporte para aplicações que demandam grande flexibilidade no armazenamento e recuperação de dados.

#### 2.3.4. Docker

O Docker é uma plataforma de virtualização de contêineres que transformou a maneira como aplicações são desenvolvidas, empacotadas e implantadas. Ele proporciona aos desenvolvedores a capacidade de criar ambientes isolados e autossuficientes para suas aplicações, conhecidos como contêineres. Esses contêineres encapsulam não apenas o código da aplicação, mas também todas as dependências necessárias, como bibliotecas e configurações, garantindo consistência e portabilidade entre diferentes ambientes de desenvolvimento e produção.

#### 2.3.5. RabbitMQ

O RabbitMQ é um sistema de mensageria de código aberto amplamente utilizado para facilitar a comunicação entre diferentes partes de uma aplicação distribuída. Ele funciona como um intermediário que permite que os diversos componentes do sistema troquem mensagens de forma assíncrona e confiável. O RabbitMQ suporta diversos padrões de mensageria, como filas, trocas e roteamento de mensagens, proporcionando flexibilidade na configuração e escalabilidade para aplicações que exigem comunicação distribuída.

## 3. Visão Lógica

### 3.1. Diagrama de Pacotes

#### 3.1.1 Introdução

O Diagrama de Pacotes é uma representação estrutural usada para organizar as classes de um projeto em grupos lógicos chamados pacotes. Cada pacote agrupa elementos relacionados, como diagramas, classes e outros pacotes, oferecendo uma visão de alto nível especialmente útil em projetos e sistemas complexos.

No nosso diagrama de pacotes, seguimos a arquitetura definida pelas diretrizes de microsserviços. O pacote principal representa o nosso sistema, dentro do qual encontramos a camada de front-end responsável por realizar requisições. Essas requisições são direcionadas para a camada de back-end, que por sua vez abriga nossos três microsserviços principais: UserService, JornadaService e GamificationService. Esses microsserviços interagem com o banco de dados para armazenamento e recuperação de dados.

Ambos os Diagramas estão abaixo:

<iframe frameborder="0" style="width:100%;height:553px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>

### 3.2. Diagrama de Implementação

<iframe frameborder="0" style="width:100%;height:513px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=nR3126rXf9x62OpuHPoS#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>

## 4. Referencências bibliográficas

> [1] EQUIPE ALECTRION 2022-2. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-2-Alectrion-DOC/#/./Documentos/arquitetura.
> [2] SOARES, João Pedro; ESTANISLAU, Matheus. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-1-Alectrion-DOC/documentation/Documentos/documento-arquitetura.html.
## 5. Histórico de versão

|**Data**|**Descrição**|**Autore(es)**|
|--------|-------------|--------------|
| 09/07/2023 | Criação do documento | Davi Matheus|
| 10/07/2023 | Revisao | Natanael Filho |
