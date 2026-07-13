# Project

## Summary

This project is a web application for tracking internal work items, priorities, and project status across a small team.

## Goals

- provide a clear shared view of work items and ownership
- make project status visible without manual spreadsheet tracking
- keep the product simple enough for a small team to maintain
- support steady iteration over months of development

## Non-Goals

- full enterprise portfolio management
- external customer-facing collaboration
- highly customizable workflow engines
- real-time chat or messaging platform features

## Users

- team managers
- individual contributors
- internal operators

## Current Scope

- authentication and role-based access
- project and work item management
- status dashboards
- activity history for key changes

## Tech Stack

- Backend: Node.js
- Frontend: React
- Database: PostgreSQL
- Cache: None yet
- AI: None yet
- Hosting: Docker

## Constraints

- small team with limited maintenance bandwidth
- product should be understandable by new contributors quickly
- infrastructure should stay lightweight in the first phase

## Success Criteria

- users can create, assign, and track work items reliably
- project status can be reviewed without separate manual reporting
- the team can change the product without losing architectural clarity
