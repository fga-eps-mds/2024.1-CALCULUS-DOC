Aqui está o documento de arquitetura revisado com todas as alterações solicitadas:

---

# Documento de Arquitetura

## 1. Introdução

Este documento tem como objetivo principal fornecer uma visão abrangente e estruturada da arquitetura do software *Calculus*. Utilizando diferentes perspectivas arquiteturais, ele detalha diversos aspectos do sistema, incluindo decisões de design, componentes, módulos, interações e a estrutura geral do software. O intuito é facilitar o entendimento da arquitetura por parte dos desenvolvedores e demais stakeholders.

### 1.1. Estrutura do Documento

Este documento está organizado da seguinte forma:

- **Introdução**: Contextualiza o documento e descreve sua estrutura.
- **Representação Arquitetural**: Apresenta os diagramas e conceitos-chave da arquitetura.
- **Visão Lógica**: Descreve a organização dos componentes e a interação entre eles.
- **Referências Bibliográficas**: Lista as fontes referenciadas no documento.
- **Histórico de Versão**: Registra as alterações realizadas no documento ao longo do tempo.

## 2. Representação Arquitetural

### 2.1. Diagrama de Relações

<iframe frameborder="0" style="width:100%;height:308px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=I-6fpici55m38HMQ_MQw#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>
**Autor:** Calculus Team

A arquitetura de microsserviços adotada no *Calculus* segue uma abordagem onde a aplicação é composta por serviços menores, implementados de forma independente e com baixo acoplamento. Esses serviços, organizados por domínios de negócios, comunicam-se entre si, principalmente por meio de APIs. Essa arquitetura promove um desenvolvimento mais ágil e facilita a escalabilidade da aplicação. Cada microsserviço possui sua própria base de dados independente, assegurando isolamento e robustez.

### 2.2. Serviços

#### 2.2.1. User Service

O *User Service* é responsável pela gestão completa dos usuários da aplicação. Suas funcionalidades incluem registro, autenticação, atualização de informações, gerenciamento de permissões e controle de acesso, garantindo uma experiência segura e personalizada para cada usuário.

#### 2.2.2. Studio Maker Service

O *Studio Maker Service* é responsável pela criação e gestão de conteúdo na plataforma. Esse serviço lida com todas as funcionalidades necessárias para que os usuários autenticados possam criar, editar e organizar conteúdos de forma eficiente, permitindo uma gestão eficaz do material disponibilizado na plataforma.

### 2.3. Tecnologias

#### 2.3.1. Next.js

O Next.js é um framework de desenvolvimento baseado em React, que permite a criação de interfaces de usuário robustas e escaláveis. Ele facilita a renderização no servidor, a geração de páginas estáticas e a integração com APIs, proporcionando uma experiência de desenvolvimento otimizada. O Next.js será utilizado no front-end do *Calculus*, garantindo alta performance e SEO aprimorado.

#### 2.3.2. NestJS

O NestJS é um framework de desenvolvimento baseado em Node.js, ideal para criar aplicações escaláveis e eficientes. Utilizando uma arquitetura modular e orientada a objetos, ele permite uma organização de código clara e manutenível. O NestJS será utilizado no back-end do *Calculus*, facilitando o desenvolvimento de APIs e microsserviços robustos.

#### 2.3.3. MongoDB

O MongoDB é um banco de dados NoSQL, flexível e escalável, projetado para lidar com grandes volumes de dados de maneira eficiente. Ele será utilizado para gerenciar as bases de dados dos serviços da aplicação, proporcionando agilidade e suporte a aplicações que demandam grande flexibilidade no armazenamento e recuperação de dados.

#### 2.3.4. Docker

O Docker é uma plataforma de virtualização que permite criar ambientes isolados para aplicações, conhecidos como contêineres. Ele garante consistência e portabilidade entre diferentes ambientes, facilitando o desenvolvimento e a implantação do *Calculus*.

## 3. Visão Lógica

### 3.1. Diagrama de Pacotes

#### 3.1.1 Introdução

O Diagrama de Pacotes organiza as classes do projeto em grupos lógicos chamados pacotes, oferecendo uma visão de alto nível especialmente útil em sistemas complexos. No *Calculus*, seguimos uma arquitetura de microsserviços, onde o pacote principal representa o sistema. Dentro dele, a camada de front-end realiza requisições que são processadas pela camada de back-end, composta pelos microsserviços principais: *User Service*, *Studio Maker Service* e *Gamification Service*, que interagem com os bancos de dados para armazenamento e recuperação de dados.

<iframe frameborder="0" style="width:100%;height:553px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>


**Autor:** *Calculus* Team

### 3.2. Diagrama de Implantação

O Diagrama de Implantação oferece uma visão detalhada de como os componentes do sistema *Calculus* estão distribuídos em diferentes máquinas ou servidores dentro da infraestrutura de TI. Ele demonstra como os serviços são implantados em contêineres, como a comunicação ocorre entre eles e como os dados são armazenados e acessados.

No *Calculus*, a implantação é realizada com o auxílio de contêineres Docker, orquestrados pelo Kubernetes. Esta abordagem garante que cada serviço, como o *User Service* e o *Studio Maker Service*, possa ser escalado de forma independente, mantendo a alta disponibilidade e eficiência operacional. Além disso, o Kubernetes gerencia a distribuição de cargas de trabalho e proporciona resiliência, assegurando que os serviços permaneçam acessíveis mesmo em caso de falhas.

<iframe frameborder="0" style="width:100%;height:513px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=calculus-diagram.drawio&page-id=nR3126rXf9x62OpuHPoS#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1a0Ob_2W3N1eerm0drMZDin9y0jveMfpN%26export%3Ddownload"></iframe>


**Autor:** *Calculus* Team

### 3.3. Diagrama de Arquitetura
O Diagrama de Arquitetura mostra a estrutura planejada do projeto Calculus, enfatizando a arquitetura de microsserviços. Ele destaca a individualização dos bancos de dados NoSQL para cada serviço, o que garante maior robustez e organização. Cada microsserviço opera de forma independente, permitindo escalabilidade e flexibilidade no desenvolvimento e na manutenção do sistema. A comunicação entre os microsserviços ocorre diretamente, sem a necessidade de um ponto de entrada centralizado.

<iframe style="border:none" width="1600" height="900" src="https://whimsical.com/embed/DPq1eFQn1xkJjiRNhKL4N7"></iframe>

 
**Autor:** *Calculus* Team

## 4. Referências Bibliográficas

> [1] EQUIPE ALECTRION 2022-2. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-2-Alectrion-DOC/#/./Documentos/arquitetura.  
> [2] SOARES, João Pedro; ESTANISLAU, Matheus. Documento de Arquitetura. Disponível em: https://fga-eps-mds.github.io/2022-1-Alectrion-DOC/documentation/Documentos/documento-arquitetura.html.

## 5. Histórico de Versão

|**Data**|**Descrição**|**Autor(es)**|
|--------|-------------|--------------|
| 09/07/2024 | Criação do documento | Davi Matheus|
| 10/07/2024 | Revisão | Natanael Filho |
| 15/07/2024 | Adição do Diagrama de Arquitetura | Paulo Gontijo, João Bisinotti |
| 28/08/2024 | Atualização do Diagrama de Arquitetura | João Bisinotti |
| 01/09/2024 | Atualização geral do documento | Paulo Gontijo |
