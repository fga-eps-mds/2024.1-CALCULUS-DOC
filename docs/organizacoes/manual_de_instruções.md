# Manual de Instalação do Projeto

## Visão Geral

Calculus é uma plataforma de aprendizado, 100% feita por estudantes da UnB, projetada para tornar o estudo de várias disciplinas escolares uma experiência envolvente e eficaz. Inspirado nos modelos de sucesso do Duolingo e Brilliant, o Calculus oferece uma abordagem inovadora para o aprendizado de matérias escolares, tornando-o acessível, divertido e altamente personalizado.

Este projeto adota uma arquitetura de microserviços, dividida em 3 repositórios distintos que colaboram para oferecer uma solução coesa e escalável. Cada repositório tem um papel específico e interage com os outros serviços para compor a aplicação completa. Abaixo está uma visão geral detalhada de cada componente:



## Repositórios

- [2024.1-CALCULUS-Frontend](https://github.com/fga-eps-mds/2024.1-CALCULUS-Frontend) : A interface do usuário (UI)
- [2024.1-CALCULUS-UserService](https://github.com/fga-eps-mds/2024.1-CALCULUS-UserService) Serviço responsável pelo gerenciamento de usuários.
- [2024.1-CALCULUS-StudioMaker](https://github.com/fga-eps-mds/2024.1-CALCULUS-StudioMaker) Serviço responsável pelo gerenciamento das Jornadas/Conteudos.
Todos os repositórios são dockerizados, garantindo que os serviços possam ser facilmente configurados e executados.

### Pré-requisitos

Antes de iniciar o processo de instalação, certifique-se de que os seguintes softwares estejam instalados:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

Para fazer alterações na documentação é necessário que se tenha python instalado. Com o python instalado siga orientações a baixo:


---

## Setup da Instalação

### 1. Clonar os Repositórios

Clone os repositórios do projeto para diretórios separados, conforme indicado abaixo:

```bash


# Clonar o backend do UserService
$ git clone https://github.com/fga-eps-mds/2024.1-CALCULUS-UserService.git

# Clonar o backend do StudioMaker
$ git clone https://github.com/fga-eps-mds/2024.1-CALCULUS-StudioMaker.git

# Clonar o frontend
$ git clone https://github.com/fga-eps-mds/2024.1-CALCULUS-Frontend.git

```

### 2. Configurar Variáveis de Ambiente

Para cada serviço, crie ou edite um arquivo .env na raiz do repositório correspondente e configure as variáveis de ambiente necessárias. Em cada projeto ja possui um arquivo chamado .env.dev que mostra a configuração da .env de cada repositorio.
Abaixo está um exemplo de configuração genérica para cada serviço:

```
# Exemplo de .env
MONGODB_URI='' 
EMAIL_USER=""
EMAIL_PASS=""
SENDGRID_API_KEY=""
JWT_SECRET=""
JWT_EXPIRATION=""
GOOGLE_CLIENT_ID=""
GOOGLE_CLIENT_SECRET=""
GOOGLE_CALLBACK_URL=""
MICROSOFT_CLIENT_ID=""
MICROSOFT_CLIENT_SECRET=""
MICROSOFT_TENANT_ID=""
MICROSOFT_CALLBACK_URL=""
FRONTEND_URL=""
EMAIL_LINK=""
```

Certifique-se de que as variáveis estejam corretamente configuradas em cada microserviço.

### 3. Subir os Containers com Docker

Vá até o diretório de cada serviço e execute os comandos abaixo para iniciar os containers com Docker. A seguir, você encontrará o passo a passo para cada serviço:


#### 3.2 Backend - Usuários

Entre na pasta do backend de usuários e execute:

```bash
$ cd 2024.1-CALCULUS-UserService
$ docker-compose up --build
```

Este serviço estará disponível na porta como http://localhost:3000.

#### 3.3 Backend - StudioMaker

Entre na pasta do backend do Studio e execute:

```bash
$ cd 2024.1-CALCULUS-StudioMaker
$ docker-compose up --build
```

Este serviço estará disponível na porta configurada no .env, como http://localhost:3002.


#### 3.1 Frontend

Entre na pasta do frontend e execute os seguintes comandos:

```bash
$ cd 2024.1-CALCULUS-Frontend 
$ docker-compose up --build
```

O frontend estará disponível em: http://localhost:4000 

## Monitoramento dos Containers

Você pode verificar o status de todos os containers em execução utilizando o comando:

```bash
$ docker ps
```

Caso queira parar todos os serviços, navegue até cada repositório e execute:

```bash
$ docker-compose down --volumes
```

Para remover containers que não estão mais em execução criados pelos docker-compose:

```
$ docker-compose rm -f
```

## Histórico de Versões

| Alteração            | Data     | Autor           |
| -------------------- | -------- | --------------- |
| Criação do documento | 08/09/24 | Davi Matheus    |
