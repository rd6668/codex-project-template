# Workflow

## Default Maintenance Rules

Use the template documents as the long-term project memory.

Recommended responsibility by file:

- `README.md`: public entry point and quick start
- `PROJECT.md`: project goals, scope, constraints, non-goals
- `ARCHITECTURE.md`: long-lived structure and system boundaries
- `DECISIONS.md`: important decisions and why they were made
- `TODO.md`: project task tracking
- `API.md`: interface contracts
- `DATABASE.md`: persistent data model and runtime state notes
- `STYLE_GUIDE.md`: code and naming conventions
- `WORKFLOW.md`: collaboration rules
- `PROMPTS.md`: fixed prompts for repeated AI collaboration

## When To Update Documents

After any major change, check whether the following need updates:

- `ARCHITECTURE.md`
- `DECISIONS.md`
- `API.md`
- `DATABASE.md`
- `TODO.md`

## What Counts As A Major Change

- new core module added or removed
- interface behavior changes
- persistence model changes
- new provider or infrastructure introduced
- security or permission model changes

## Working Pattern

Keep implementation work in code and active discussion in chat.
Keep durable project knowledge in the documents.

If a project starts drifting away from its documents, fix the documents early.
