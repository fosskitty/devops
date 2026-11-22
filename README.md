# hello-devops

A simple Java 21 + Maven + Spring Boot project for DevOps workflows.

## Project Status

This project is being developed as part of a DevOps assignment.

## Prerequisites

- Java 21
- Maven 3.x

## Port Configuration

Configured to run on port `8081` by default to avoid port conflicts with host services (such as Jenkins on 8080).

## Endpoints

- `GET http://localhost:8081/hello` - Returns `Hello! My DevOps project is running.`
- `GET http://localhost:8081/health` - Returns `UP`

## Build & Run

### Build
```bash
mvn clean package
```

### Run
```bash
mvn spring-boot:run
```
or run the packaged JAR:
```bash
java -jar target/hello-devops-0.0.1-SNAPSHOT.jar
```

## Docker

Build Docker image:
```bash
docker build -t hello-devops .
```

Run Docker container:
```bash
docker run -p 8081:8081 hello-devops
```
