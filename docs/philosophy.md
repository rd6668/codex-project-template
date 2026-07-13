# Philosophy

## What This Template Optimizes For

This template optimizes for context durability in long-running software projects.

The real cost in long projects is usually not writing code. It is losing track of:

- what the system is supposed to do
- what the architecture actually is
- why a decision was made
- which interfaces are stable
- which tasks are still open

This template exists to keep that information in the repository.

## Stable Facts Vs. Temporary Context

Treat project information as two different classes.

Stable facts belong in repository documents:

- project goals and scope
- architecture boundaries
- technical decisions and rationale
- APIs and data models
- workflow rules

Temporary context belongs in chat:

- a current bug investigation
- implementation brainstorming
- one-off debugging notes
- refactor tradeoff discussion

If a piece of information should still matter in a few weeks, it probably belongs in a document.

## Why This Works Well With AI Tools

AI tools are good at reading the current visible context.
They are not good at preserving months of evolving project history unless you keep that history in files.

When the important facts live in the repository:

- new chats start faster
- different AI tools see the same project facts
- key decisions are easier to trace
- the team repeats itself less

## Practical Rule

Documents should contain durable facts.
Chats should contain active problem-solving.

That separation is the main value of this template.
