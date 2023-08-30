# java-spring-boot-rest-api

## Requirements
[Docker](https://www.docker.com/)

## Technologies 
[Java 17 (openjdk)](https://openjdk.org/projects/jdk/17/), [Maven](https://maven.apache.org/), [Spring Boot](https://spring.io/projects/spring-boot)

## sh folder

The sh folder allows you to quickly launch docker commands to perform tasks

## Build project
On the root folder
```bash
sh sh/build
```

## Run the project
```bash
sh sh/deploy
```

The service is deployed at http://localhost:8085

## Swagger

Swagger UI, the interactive documentation tool for your API, is accessible at the URL http://localhost:8085/swagger-ui/index.html, providing a user-friendly interface to explore and test your APIs. Additionally, the raw Swagger JSON representation of your API documentation can be accessed at http://localhost:8085/v3/api-docs, serving as a machine-readable document describing your API endpoints and schemas.

## Query

Get all personnes : 
```bash
curl -X 'GET' \
  'http://localhost:8085/api/personnes' \
  -H 'accept: */*'
```

Create personne :
```bash
curl -X 'POST' \
  'http://localhost:8085/api/personnes' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
  "firstName": "toto",
  "lastName": "tata"
}'
```

Get a personne :
```bash
curl -X 'GET' \
  'http://localhost:8085/api/personnes/1' \
  -H 'accept: */*'
```
