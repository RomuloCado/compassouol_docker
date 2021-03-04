<h1 align="center">Configurações Docker com Spring Boot e MySQL da API de Produtos em Estoque<h1>

# Índice

- [Sobre](#-sobre)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Testes](https://github.com/RomuloCado/compassouol#testes)
- [Como baixar o projeto](#-como-baixar-o-projeto)

## 🔖&nbsp; Sobre

O **Docker** nada mais é do que uma coleção de tecnologias para facilitar o deploy e a execução das nossas aplicações, através de containers e imagens geradas de uma aplicação ou ferramenta. Basta ter o docker instalado no Sistema Operacional que será possível através do Dockerfile e o docker-compose.yaml, subir e realizar testes da aplicação em qualquer ambiente independente da configuração do seu sistema.
O projeto **Produtos em Estoque** é uma API REST desenvolvida na linguagem Java, com o framework Spring Boot, tem o intuito de manipular no banco de dados a lista de produtos 
relacionados com seu estoque, contendo a descrição do produto, o valor, e sua quantidade em estoque. Permite o cadastro, busca, atualização, e exclusão.
Através dos métodos REST:
-GET
-POST
-PUT
-DELETE


---

## 🚀 Tecnologias utilizadas

O projeto foi desenvolvido utilizando as seguintes tecnologias

- [Docker](https://www.docker.com/products/docker-desktop)
- [SpringBoot](https://spring.io/projects/spring-boot)
- [Swagger](http://springfox.github.io/springfox/)
- [Flyway](https://flywaydb.org/documentation/usage/api/#download)
- [MySQL](https://www.mysql.com)

---

## Testes

Para realizar os testes da aplicação foram configuradas as seguintes portas para funcionamento da API, a porta 8080 para funcionamento tomcat do spring, e a porta 3306 para funcionamento do banco MySQL, certifique-se de que estas portas não estarão em uso antes e subir a aplicação no docker. Através do docker-compose.yaml o banco ira iniciar primeiro e a aplicação só irá subir depois do banco estar estável, através do healthcheck. Pode ser utilizado para teste o Postman ou a própria documentação Swagger do projeto (http://localhost:8080/swagger-ui.html).

---

## 🗂 Como baixar o projeto e subir a aplicação com o docker

```bash
    # Clonar o repositório
    $ git clone https://github.com/RomuloCado/compassouol
    # Entrar no diretório
    $ cd compassouol
    #Realizar o build do arquivo .jar da aplicação
    $ mvn clean package
    #Realizar o build do banco de dados e da api
    $ docker-compose build
    #Iniciar a aplicação para testes
    $ docker-compose up

```

---

Desenvolvido por Rômulo Cadó Dorneles.

