# Backend

[![StandWithUkraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://github.com/vshymanskyy/StandWithUkraine/blob/main/docs/README.md)
[![CI](https://github.com/MykolaVaskevych/cs4135_week2_backend/actions/workflows/ci.yml/badge.svg)](https://github.com/MykolaVaskevych/cs4135_week2_backend/actions/workflows/ci.yml)
[![Java](https://img.shields.io/badge/java-21-orange.svg)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/spring%20boot-3.5-brightgreen.svg)](https://spring.io/projects/spring-boot)

Spring Boot backend with JPA, H2/PostgreSQL, and Bruno API tests.

## Quick Start

```bash
./mvnw spring-boot:run
```

Runs on http://localhost:8080

## Endpoints

| Endpoint | Description |
|----------|-------------|
| `/actuator/health` | Health check |
| `/h2-console` | H2 database console (dev only) |

## API Tests

API tests are in the `bruno/` directory using [Bruno](https://www.usebruno.com/).

```bash
# Install Bruno CLI
npm install -g @usebruno/cli

# Run tests
cd bruno
bru run --env ci
```

## Pre-commit Hooks

This project uses Lefthook + Spotless for code formatting.

```bash
# Install hooks
lefthook install

# Auto-fix formatting
./mvnw spotless:apply
```

On commit, Spotless checks Java formatting (Google Java Format, AOSP style).
