# API

## Overview

This project exposes a REST API for managing projects, work items, and status reporting.

## Endpoints Or Commands

### `GET /api/projects`

#### Input

- optional filters for status, owner, and search

#### Behavior

- return a filtered list of visible projects

#### Output

- list of project summaries

### `POST /api/work-items`

#### Input

- title
- description
- project id
- assignee id

#### Behavior

- create a new work item if the caller has permission

#### Output

- created work item record

## Internal Contracts

- route handlers validate and delegate, but do not own business rules
- services own permission checks and workflow rules
- repositories hide persistence implementation details

## Change Policy

The following changes must update this file:

- endpoint additions or removals
- request or response field changes
- permission behavior changes
