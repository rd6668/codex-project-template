# Architecture

## High-Level Flow

User

-> Web Client

-> API Layer

-> Application Services

-> Repository Layer

-> PostgreSQL

## Main Components

### Web Client

- Responsibility: render product UI and collect user actions
- Inputs: user navigation and form interactions
- Outputs: authenticated API requests

### API Layer

- Responsibility: expose application capabilities through stable endpoints
- Inputs: HTTP requests from the client
- Outputs: validated requests for service execution

### Application Services

- Responsibility: enforce business rules and orchestration
- Inputs: validated commands and queries
- Outputs: state changes and query results

### Repository Layer

- Responsibility: persistence access and query isolation
- Inputs: persistence requests from services
- Outputs: stored and retrieved records

## Boundaries

- business rules belong in services, not in route handlers
- persistence concerns should stay behind repository interfaces
- the client should not depend on database-specific behavior

## Cross-Cutting Concerns

- Auth: session or token-based authentication
- Permissions: role-based access control
- Caching: none in the current phase
- Logging: structured application logs
- Observability: basic metrics and error tracking

## Operational Notes

- first deployment target is a single environment with one database
- database migrations must be tracked explicitly
- breaking API changes require coordinated documentation updates
