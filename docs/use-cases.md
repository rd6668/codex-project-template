# Use Cases

This template is meant to be generic, but different project types should fill it differently.

The goal is not to force every project into the same wording.
The goal is to keep long-lived project facts explicit and easy for humans and AI tools to read.

## 1. Web App Or SaaS

Typical examples:

- internal admin tools
- dashboards
- B2B SaaS products
- consumer web apps

Focus most on:

- `PROJECT.md`: users, scope, non-goals, business constraints
- `ARCHITECTURE.md`: frontend, backend, auth, services, storage
- `API.md`: REST or GraphQL contracts
- `DATABASE.md`: entities, relationships, migration policy
- `DECISIONS.md`: framework, hosting, database, auth choices

Usually less important at the start:

- `PROMPTS.md`

Good opening questions:

- who are the users
- what actions do they need to complete
- what is the minimal product scope
- what data must persist

## 2. Backend Service Or API

Typical examples:

- internal APIs
- public developer platforms
- automation backends
- integration services

Focus most on:

- `PROJECT.md`: consumers, SLAs, boundaries
- `ARCHITECTURE.md`: services, queues, providers, dependency flow
- `API.md`: endpoints, contracts, auth, error shapes
- `DATABASE.md`: storage model, caching, consistency expectations
- `STYLE_GUIDE.md`: error handling, observability, testing rules

Good opening questions:

- who consumes this API
- what contracts must stay stable
- what failure modes matter most
- what latency or throughput constraints exist

## 3. CLI Tool Or Developer Tooling

Typical examples:

- internal developer CLI
- automation scripts
- code generation tools
- local productivity tools

Focus most on:

- `PROJECT.md`: user workflow and supported commands
- `ARCHITECTURE.md`: command flow, parsing, execution layers
- `API.md`: command interface and flags instead of HTTP endpoints
- `DECISIONS.md`: distribution, runtime, packaging decisions

Usually lighter:

- `DATABASE.md`, unless the tool stores local or remote state

Good opening questions:

- who runs the tool
- what inputs and outputs matter
- how will it be installed and upgraded
- what behavior must stay backward compatible

## 4. AI Product Or Agent Workflow

Typical examples:

- prompt-driven tools
- retrieval systems
- agent pipelines
- OCR, summarization, classification workflows

Focus most on:

- `PROJECT.md`: user value, boundaries, evaluation criteria
- `ARCHITECTURE.md`: model calls, retrieval flow, orchestration, fallbacks
- `DECISIONS.md`: model selection, provider decisions, cost tradeoffs
- `API.md`: tool contracts, input-output schemas, integration contracts
- `PROMPTS.md`: stable prompts and operating rules

Usually worth adding explicitly in docs:

- evaluation method
- latency and cost constraints
- fallback behavior when model output is poor

Good opening questions:

- what part is deterministic and what part is model-driven
- how success is evaluated
- what prompts are stable enough to document
- what model/provider dependencies are acceptable

## 5. Mobile App

Typical examples:

- iOS app
- Android app
- React Native or Flutter app

Focus most on:

- `PROJECT.md`: users, product scope, device/platform constraints
- `ARCHITECTURE.md`: app layers, API dependencies, offline behavior
- `API.md`: backend dependencies and client contracts
- `DECISIONS.md`: state management, navigation, platform strategy

Good opening questions:

- what platforms are supported
- what offline behavior is required
- what backend contracts are critical
- what UX constraints matter most

## 6. Library Or SDK

Typical examples:

- frontend component library
- backend SDK
- internal shared package
- open source utility library

Focus most on:

- `PROJECT.md`: target users and supported use cases
- `API.md`: public API surface and compatibility expectations
- `DECISIONS.md`: versioning, packaging, runtime support
- `STYLE_GUIDE.md`: backward compatibility and test rules

Usually less central:

- `DATABASE.md`, unless the library persists state

Good opening questions:

- who integrates this library
- what public API is stable
- what versions or runtimes are supported
- what changes count as breaking

## How To Adapt The Template

Do not fill every file to the same depth on day one.

Use this rule:

- fill deeply where the project has long-lived complexity
- keep short placeholders where the project does not yet have real decisions

The template is working correctly when:

- a new engineer can understand the project quickly
- a new AI session can start without long backstory
- important decisions and boundaries are visible in files
