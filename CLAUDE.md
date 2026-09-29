# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Spring Boot web service built with Maven.

- **Language / runtime:** Java 8 (JDK 1.8)
- **Framework:** Spring Boot 2.7.18
- **Build tool:** Maven
- **Base package:** `com.testai`

## Commands

- Build: `mvn clean package`
- Run the app: `mvn spring-boot:run`
- Run all tests: `mvn test`
- Run a single test class: `mvn test -Dtest=TestAiApplicationTests`
- Build then run the jar: `mvn clean package && java -jar target/testai-0.0.1-SNAPSHOT.jar`

## Architecture

- `src/main/java/com/testai/` — application code
  - `TestAiApplication.java` — `@SpringBootApplication` entry point
  - `controller/` — REST controllers (e.g. `HelloController` serving `/`)
- `src/main/resources/application.properties` — configuration (`spring.application.name`, `server.port`)
- `src/test/java/com/testai/` — tests (`@SpringBootTest` context-load test)
- `pom.xml` — Maven build using `spring-boot-starter-parent` 2.7.18 with `spring-boot-starter-web` and `spring-boot-starter-test`
