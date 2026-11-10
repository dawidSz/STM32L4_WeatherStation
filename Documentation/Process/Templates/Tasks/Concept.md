---
type: concept
id: CON-NNNN
title: ""
status: OPEN
assignee: CHIEF_ENGINEER
parent:
blocked_by: []
outputs: []
created: {{date:YYYY-MM-DD}}
updated: {{date:YYYY-MM-DD}}
closed:
---

# {{title}}

> [!warning] Template reference – delete this section when creating a task
> - File name: `Tasks/Concepts/CON-NNNN Topic.md`
> - status: OPEN | BLOCKED | BRAINSTORMING | IN_IMPLEMENTATION | IMPLEMENTED | DROPPED
> - blocked_by: links to blocking concepts – mandatory when status is BLOCKED
> - outputs: links to ADRs (Architecture/Concept Level/ADR/) and notes (Architecture/Concept Level/Notes/)
> - closed: set when status becomes IMPLEMENTED or DROPPED
>
> ```mermaid
> stateDiagram-v2
>     [*] --> OPEN
>     OPEN --> BRAINSTORMING
>     OPEN --> BLOCKED
>     BRAINSTORMING --> BLOCKED
>     BLOCKED --> OPEN
>     BLOCKED --> BRAINSTORMING
>     BRAINSTORMING --> IN_IMPLEMENTATION
>     IN_IMPLEMENTATION --> IMPLEMENTED
>     OPEN --> DROPPED
>     BLOCKED --> DROPPED
>     BRAINSTORMING --> DROPPED
>     IMPLEMENTED --> [*]
>     DROPPED --> [*]
> ```

## Topic

What this concept is about (optional – the title may be sufficient).

## Questions to answer

- [ ] Question 1

## Notes / Brainstorming

## Outcome

Summary of decisions – the input for derived agent tasks.

## Log

- {{date:YYYY-MM-DD}} – created (status: OPEN)
