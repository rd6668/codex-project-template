# Database

## Current State

PostgreSQL is the primary database.

## Data Model

### Project

- Purpose: track project ownership, status, and summary metadata
- Key fields: `id`, `name`, `status`, `owner_id`, `created_at`

### WorkItem

- Purpose: track units of planned and active work
- Key fields: `id`, `project_id`, `title`, `status`, `assignee_id`, `updated_at`

### User

- Purpose: identify internal users and roles
- Key fields: `id`, `email`, `role`, `created_at`

## Runtime State

- authenticated session state
- request-scoped permission context

## Persistence Strategy

- projects, work items, and users are persisted
- transient UI state is not persisted in the backend

## Migration Policy

- schema changes must be tracked with migrations
- each application change that depends on schema updates must reference the related migration
