# Trabalho 1 - ES2

Este repositório contém o código-fonte do software desenvolvido para o Trabalho 1 da matéria de Engenharia de Software 2 (ES2).

#  Front-End

### Requisitos abordados:

- *CRUD de Profissionais*: O sistema permite incluir, alterar, excluir e consultar informações sobre os profissionais de sua empresa. Os dados dos profissionais são: nome, endereço, nascimento, gênero, raça e especialidade;
- *CRUD de Times*: O sistema permite incluir, alterar, excluir e consultar informações sobre times da sua empresa. Os dados de times são: nome do time e relação de profissionais do time;
- *CRUD de Projetos*: O sistema permite incluir, alterar, excluir e consultar informações sobre projetos desenvolvidos por sua empresa. Os dados de projetos são: nome do projeto, nome do cliente, objetivo do projeto, data de início/término, valor do projeto e time responsável.

### Tecnologias:

- Linguagem de programação: JavaScript;
- Frameworks: Vue 3 + Vite;
- APIs: Fetch API;
- Conceitos: SPA (Single Page Application).

### Rotas:

- `/profissionais` - Interface dos Profissionais;
- `/times` - Interface dos Times;
- `/projetos` - Interface dos Projetos.

  
### Instruções de uso:

#### Para uso local:
Clone o repositório para o seu computador usando `git clone https://github.com/aminmismail/ES2_Front.git`

Dentro da pasta `ES2_Front`, instale as dependências com `npm install`.

Inicie a aplicação com `npm run dev`.

Acesse a aplicação no navegador em `http://localhost:3000`.

#### Para uso em Docker:

Primeiramente, na pasta `ES2_Front`, execute: `docker build -t front . `

Em seguida, execute `docker run -p 3000:3000 front`

Para utilizar o docker-compose ao invés de rodar com o docker, basta executar `docker-compose up` ao invés da instrução anterior.


# Back-End

O backend foi construído utilizando Java, Spring Framework, JPA, Hibernate e PostgreSQL.

> Sistema de Gerenciamento de Projetos

Configuração de Ambiente
------------

Certifique-se de ter as seguintes ferramentas instaladas antes de executar o projeto:

- Java
- Maven
- PostgreSQL

Além disso, é necessário configurar o arquivo application.properties dentro da pasta resources com as informações do banco de dados PostgreSQL:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco_de_dados
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

Executando o Projeto
------------

### Executando com Maven

1. Clone este repositório.

2. Execute o comando Maven para baixar as dependências:
``` mvn clean install ```

3. Inicie a aplicação SpringBoot:

``` mvn spring-boot:run ```

### Executando com Docker/Docker-Compose

Também é possível executar o projeto usando Docker e Docker-Compose, Siga os passos abaixo:

1. Certifique-se de ter o Docker e o Docker-Compose instalados em sua máquina.

2. Clone este repositório.

3. No diretório raiz do projeto, execute o seguinte comando para construir a imagem Docker:

```docker build -t nome-do-repositorio-backend .```

4. No diretório raiz do projeto, execute o seguinte comando para construir a imagem Docker:

``` docker-compose up ```

Isso iniciará o contêiner do backend juntamente com um contêiner PostgreSQL. A aplicação estará disponível em http://localhost:8080.

Certifique-se de que não há nenhum serviço em execução na porta 8080 e 5432 antes de iniciar o Docker-Compose.

Estrutura do Projeto
------------

O projeto segue uma estrutura organizada para facilitar a manutenção e escalabilidade. Os principais pacotes incluem:

- Controller: Contém os controladores responsáveis por lidar com as - requisições HTTP.
- Service: Camada de serviço que implementa a lógica de negócios.
- Repository: Repositórios JPA para interação com o banco de dados.
- Domain: Modelos de entidades que representam os dados persistentes.

