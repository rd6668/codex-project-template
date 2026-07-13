# Decisions

## 2026-07-13

### Decision

Start with a modular monolith instead of microservices.

### Why

- lower operational complexity for a small team
- easier local development and simpler debugging

### Alternatives Considered

- microservices from the beginning
- serverless function-only architecture

### Impact

- module boundaries must be maintained inside one codebase
- future extraction is possible if boundaries remain clean

## 2026-07-13

### Decision

Use PostgreSQL as the primary database.

### Why

- strong transactional model
- mature tooling and broad ecosystem support

### Alternatives Considered

- MySQL
- SQLite
- MongoDB

### Impact

- schema changes should be migration-driven
- relational modeling becomes the default design path
