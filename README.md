## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues  
- Email: `marcopaulosrodrigues04@gmail.com`  
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues  
- Email: `marcopaulosrodrigues04@gmail.com`  
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues  
- Email: `marcopaulosrodrigues04@gmail.com`  
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues  
- Email: `marcopaulosrodrigues04@gmail.com`  
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues  
- Email: `marcopaulosrodrigues04@gmail.com`  
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`# Cadastro de Usuário

Aplicação de exemplo em Spring Boot para um CRUD simples de usuários (Java 17).

## Visão geral
Este projeto demonstra um backend REST com Spring Boot, JPA e banco em memória H2. Ele inclui endpoints para criar, buscar, atualizar e deletar usuários.

## Requisitos
- Java 17
- Maven 3.x

## Como rodar
1. Build com Maven:

   mvn -DskipTests package

2. Executar com Maven:

   mvn spring-boot:run

   ou executar o JAR gerado:

   java -jar target\cadastro-usuario-0.0.1-SNAPSHOT.jar

A aplicação por padrão sobe em http://localhost:8080

## Banco de dados
O projeto usa H2 em memória. As configurações estão em `src/main/resources/application.properties`.
- JDBC URL: `jdbc:h2:mem:usuario`
- Usuário: `sa`
- Senha: (vazia)

Você pode acessar o console H2 em: http://localhost:8080/h2-console
Use a JDBC URL acima para se conectar.

> Observação: como o banco é em memória, os dados são perdidos quando a aplicação é finalizada.

## Endpoints
Base: `http://localhost:8080/usuario`

- POST /usuario
  - Descrição: cria um novo usuário
  - Body (JSON): { "nome": "Joao", "email": "j@ex.com" }

- GET /usuario?email={email}
  - Descrição: busca um usuário pelo email
  - Exemplo: `/usuario?email=j@ex.com`

- DELETE /usuario?email={email}
  - Descrição: deleta um usuário pelo email

- PUT /usuario?id={id}
  - Descrição: atualiza um usuário pelo id
  - Body (JSON): { "nome": "Nome Novo", "email": "novo@ex.com" }

## Exemplos com curl (PowerShell)
- Criar:

  curl -H "Content-Type: application/json" -d '{"nome":"Joao","email":"j@ex.com"}' http://localhost:8080/usuario -v

- Buscar:

  curl "http://localhost:8080/usuario?email=j@ex.com"

- Deletar:

  curl -X DELETE "http://localhost:8080/usuario?email=j@ex.com"

- Atualizar:

  curl -X PUT -H "Content-Type: application/json" -d '{"nome":"Joao Atualizado","email":"j@ex.com"}' "http://localhost:8080/usuario?id=1"

## Observações importantes
- Lombok está presente no projeto. No IntelliJ/JetBrains certifique-se de:
  - Ter o plugin Lombok instalado e habilitado.
  - Habilitar `Annotation Processing` em `Settings -> Build, Execution, Deployment -> Compiler -> Annotation Processors`.

- Se o IDE mostrar classes/métodos do controller como "never used", isso é esperado — o Spring injeta/usa os controllers em runtime via reflexão.


## Problemas comuns
- Autocomplete ou imports não funcionando: reimporte o projeto Maven e, se necessário, invalidar caches (`File -> Invalidate Caches / Restart`).

- Erro de conexão H2: verifique a URL em `application.properties` (deve ser `jdbc:h2:mem:usuario` para este projeto).

## Testes
Testes manuais: foram realizados testes manuais usando Postman para validar os endpoints. Também é possível usar `curl` conforme os exemplos acima.  
Para testes automatizados (unitários/integrados), execute:

\`\`\`
mvn test
\`\`\`

## Contato
- Nome: Marco Rodrigues
- Email: `marcopaulosrodrigues04@gmail.com`
- LinkedIn: `https://www.linkedin.com/in/marcopaulosoaresrodrigues/`
