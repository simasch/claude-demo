# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Spring Boot REST API that provides time-related endpoints. The application is built using Maven and Java 17.

**Main Components:**
- `TimeApiApplication.java`: Main Spring Boot application entry point
- `TimeController.java`: REST controller exposing `/time` endpoint that returns current timestamp

## Development Commands

**Build and run:**
```bash
mvn clean compile                    # Compile the project
mvn spring-boot:run                  # Run the application (starts on port 8080)
mvn clean package                    # Build JAR file
java -jar target/time-api-1.0.0.jar  # Run the built JAR
```

**Testing:**
```bash
mvn test                             # Run all tests
mvn test -Dtest=ClassName            # Run specific test class
```

**Development workflow:**
```bash
mvn clean install                    # Full build with tests
```

## Architecture Notes

- Standard Spring Boot web application structure using `@SpringBootApplication` and `@RestController`
- Single REST endpoint at `/time` returns formatted current timestamp
- Uses Java 21 and Spring Boot 3.5.0
- No database or external dependencies beyond Spring Boot web starter