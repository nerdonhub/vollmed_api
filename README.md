# Voll.Med - API REST para Gestão de Clínica Médica

Bem-vindo ao repositório da API REST da Voll.Med, uma clínica fictícia dedicada à gestão de médicos, pacientes, usuários e consultas. Esta API foi desenvolvida com a ajuda da formação Java e Spring da Alura, utilizando Java 17, Spring 3.1.5, Maven 4.0.0, MySQL 8.0.35, além das tecnologias Spring Boot, JWT, Lombok, Flyway, Auth0, SpringDoc (Swagger), Spring Security, JUnit com Spring.

## Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:

- Java 17
- Maven 4.0.0
- MySQL 8.0.35
- Docker (opcional para implantar o banco de dados)

## Configuração do Banco de Dados

A aplicação utiliza o Flyway para gerenciar as migrações do banco de dados. Certifique-se de configurar as propriedades do banco de dados no arquivo `application.properties` e execute as migrações com o seguinte comando:

```bash
mvn flyway:migrate
```

## Configuração do Auth0

A autenticação é feita por meio do Auth0. Configure as credenciais no arquivo `application.properties`. Certifique-se de ter as permissões adequadas configuradas no Auth0 para os escopos necessários.

## Configuração do JWT

A aplicação utiliza JWT para autenticação e autorização. As configurações do JWT estão no arquivo `application.properties`.

## Execução da Aplicação

Execute a aplicação usando o seguinte comando:

```bash
mvn spring-boot:run
```

A API estará disponível em `http://localhost:8080`.

## Documentação da API

A documentação da API pode ser acessada em `http://localhost:8080/swagger-ui.html`. Utilizamos o SpringDoc (Swagger) para gerar automaticamente a documentação.

## Endpoints

### `/login`

- **Método**: POST

**Descrição**: Endpoint para autenticação de usuários. Retorna um token JWT válido.

### `/medicos`

- **Método**: GET

**Descrição**: Lista todos os médicos cadastrados.

- **Método**: POST
**Descrição**: Adiciona um novo médico.

- **Método**: GET `/{id}`

**Descrição**: Detalha as informações de um médico específico.

- **Método**: DELETE `/{id}`

**Descrição**: Desativa um médico.

### `/consultas`

- **Método**: POST

**Descrição**: Marca uma nova consulta.

### `/pacientes`

- **Método**: GET

**Descrição**: Lista todos os pacientes cadastrados.

- **Método**: POST

**Descrição**: Adiciona um novo paciente.

- **Método**: GET `/{id}`

**Descrição**: Detalha as informações de um paciente específico.

- **Método**: DELETE `/{id}`

**Descrição**: Desativa um paciente.

## Contribuições

Sinta-se à vontade para contribuir para o desenvolvimento deste projeto. Abra uma issue para discutir novos recursos ou correções.

## Agradecimentos

Este projeto foi desenvolvido com o apoio da formação Java e Spring da Alura.
