# Dojo Docker

## Conceitos Básicos de Docker

Docker é uma plataforma de software que permite criar, testar e implantar aplicações rapidamente. Ele empacota software em unidades padronizadas chamadas contêineres, que possuem tudo o que a aplicação necessita para rodar, incluindo bibliotecas, ferramentas do sistema, código e runtime.

**Principais Conceitos:**

- **Imagem**: Um pacote leve, autossuficiente e imutável que contém tudo o que é necessário para executar um pedaço específico de software.
- **Contêiner**: Uma instância de uma imagem. Pode ser executado, iniciado, parado, movido e deletado usando a CLI do Docker.
- **Dockerfile**: Um script que contém uma série de instruções sobre como construir uma imagem Docker.
- **Docker Compose**: Uma ferramenta para definir e executar aplicações multi-contêiner Docker.

## Como Criar um Dockerfile

Um Dockerfile é um arquivo de texto que contém todas as instruções para construir uma imagem Docker. Aqui está um exemplo simples:

```dockerfile
# Usando a imagem base do Node.js
FROM node:14

# Definindo o diretório de trabalho dentro do contêiner
WORKDIR /app

# Copiando o package.json e o package-lock.json
COPY package*.json ./

# Instalando dependências
RUN npm install

# Copiando o restante do código da aplicação
COPY . .

# Expondo a porta que a aplicação irá rodar
EXPOSE 3000

# Comando para rodar a aplicação
CMD ["node", "app.js"]
```

## Como Criar um Docker Compose

O Docker Compose permite definir e gerenciar aplicações multi-contêiner. Aqui está um exemplo básico de um arquivo `docker-compose.yml`:

```yaml
services:
  web:
    image: my-web-app
    build: .
    ports:
      - "3000:3000"
    volumes:
      - .:/app
    environment:
      - NODE_ENV=development
  db:
    image: postgres:13
    volumes:
      - pgdata:/var/lib/postgresql/data
    environment:
      - POSTGRES_PASSWORD=mysecretpassword

volumes:
  pgdata:
```

## Comandos Básicos

Aqui estão alguns comandos básicos do Docker para começar:

- docker build -t `<nome-da-imagem>` . - Cria uma imagem a partir do Dockerfile no diretório atual.
- docker run -p `<porta-local>`:`<porta-contêiner>` `<nome-da-imagem>` - Executa um contêiner a partir de uma imagem.
- docker ps - Lista os contêineres em execução.
- docker stop `<id-do-contêiner>` - Para um contêiner em execução.
- docker-compose up - Inicia todos os serviços definidos no arquivo docker-compose.yml.
- docker-compose down - Para e remove todos os contêineres, redes e volumes definidos no docker-compose.yml.

Para mais detalhes, acesse a gravação completa do treinamento no seguinte [link](https://unbbr-my.sharepoint.com/:v:/g/personal/190058650_aluno_unb_br/EU2xkeoNU3BDhUJthfTzOOgBNs0bYO_Xj6LynFDV1DS1gg?e=cGuV53&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D).

|**Data**|**Descrição**|**Autore(es)**|
|--------|-------------|--------------|
|10/07/2024| Criação do documento | Natanael Fernandes |
