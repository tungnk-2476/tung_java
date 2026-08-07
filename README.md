# TripGo API

Backend application for the TripGo travel platform, built with Spring Boot, Java 21,
PostgreSQL, Spring Data JPA, Flyway, Spring Security, and Thymeleaf.

## Requirements

- Java 21
- PostgreSQL

The Maven Wrapper is included, so a separate Maven installation is not required.

## Database configuration

Set the following environment variables before starting the application:

```shell
export DB_URL=jdbc:postgresql://localhost:5432/tripgo
export DB_USERNAME=tripgo
export DB_PASSWORD=your_password
```

`DB_URL` and `DB_USERNAME` default to the local values shown above. `DB_PASSWORD`
defaults to an empty value for local development and should always be supplied in
deployed environments.

## Run locally

```shell
./mvnw spring-boot:run
```

## Run tests

```shell
./mvnw test
```

Tests use an in-memory H2 database in PostgreSQL compatibility mode and do not
require a running PostgreSQL instance.

## Build

```shell
./mvnw clean package
```
