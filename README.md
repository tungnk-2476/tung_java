# TripGo API

Backend application for the TripGo travel platform, built with Spring Boot, Java 21,
PostgreSQL, Spring Data JPA, Flyway, Spring Security, and Thymeleaf.

## Requirements

- Java 21
- PostgreSQL
- Docker (for integration tests)

The Maven Wrapper is included, so a separate Maven installation is not required.

## Database configuration

Create a local environment file from the provided template:

```shell
cp .env.example .env
```

Update `.env`, then export its values in the current shell before starting the
application:

```shell
set -a
source .env
set +a
```

`DB_URL` and `DB_USERNAME` have local defaults. `DB_PASSWORD` is required in every
environment; the application fails to start when it is missing.

## Run locally

```shell
./mvnw spring-boot:run
```

## Run tests

```shell
./mvnw test
```

Integration tests start PostgreSQL 17 with Testcontainers, apply all Flyway
migrations, and require Docker to be running.

## Build

```shell
./mvnw clean package
```
