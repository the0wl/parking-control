# 🚗 parking-control

> API de gerenciamento de estacionamento simplificada para demonstrar conceitos de Spring Boot.

# Definição

| Método | Rota               | Descrição                                                   | Parâmetros                        | Resposta Esperada                                       |
|--------|--------------------|-------------------------------------------------------------|-----------------------------------|---------------------------------------------------------|
| GET    | /parking-slot      | Retorna uma lista de vagas de estacionamento indisponíveis. | `Pageable` -> `page` `size` `etc` | Lista de vagas de estacionamento.                       |
| GET    | /parking-slot/{id} | Retorna uma vaga do estacionamento.                         |                                   | Uma vaga de estacionamento.                             |
| POST   | /parking-slot      | Cria uma nova vaga de estacionamento.                       | `ParkingSlotModel`                | Objeto da vaga de estacionamento criada.                |
| DELETE | /parking-slot/{id} | Remove uma vaga de estacionamento pelo ID.                  |                                   | Mensagem de confirmação da remoção.                     |
| PUT    | /parking-slot/{id} | Atualiza informações de uma vaga de estacionamento pelo ID. | `ParkingSlotModel`                | Objeto da vaga de estacionamento atualizada.            |


# Especificações

- **Gerenciador de pacotes:** Maven
- **Linguagem:** Java 17
- **Spring Boot:** 3.2.2
- **Packaging:** Jar
- **Dependências:**
  - spring-boot-starter-actuator
  -	spring-boot-starter-data-jpa
  -	spring-boot-starter-validation
  -	spring-boot-starter-web
  -	postgresql
  -	spring-boot-starter-test

# PostgreSQL

```
docker run --name parking-control-db -e POSTGRES_DB=parking-control-db -e POSTGRES_PASSWORD=admin -p 5432:5432 -d postgres
```
