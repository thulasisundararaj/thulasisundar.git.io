# LedgerLeaf — Spring Boot Finance API

## One-line pitch
A well-tested personal finance API for accounts and transactions, built to demonstrate clean Java service design and careful data handling.

## Why this project
Shows Java, Spring Boot, relational modeling, API contracts, validation, security, testing, and production-minded documentation.

## MVP
- Account and transaction CRUD with pagination and filtering.
- PostgreSQL schema with migrations.
- Validation, consistent error responses, and OpenAPI docs.
- Authentication and owner-scoped authorization.
- Unit, repository, and API integration tests.
- Docker Compose local development setup.

## Suggested stack
Java 21, Spring Boot, Spring Data JPA, PostgreSQL, Flyway, Spring Security, Testcontainers, Docker, and GitHub Actions.

## Quality bar
- Use BigDecimal for money and explicit currency handling.
- Enforce ownership in every data access path.
- Keep controllers thin and business rules in service/domain layers.
- Test authorization failures, invalid input, pagination, and transaction boundaries.
- Include a data model, API examples, and one-command local setup.

## Build sequence
1. Define API and domain rules for accounts and transactions.
2. Implement schema, migrations, and core endpoints.
3. Add authentication, authorization, and validation.
4. Add integration tests and CI.
5. Deploy a demo and document architecture and tradeoffs.

## Resume bullet template
Built a Java/Spring Boot finance API backed by PostgreSQL, implementing [features] with [test coverage or measured performance] and secure owner-scoped access.

## Status
Planned. Use real measurements and completed features in the resume bullet.
