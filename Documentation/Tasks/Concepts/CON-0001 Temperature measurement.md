---
type: concept
id: CON-0001
title: "Temperature measurement"
status: OPEN
assignee: CHIEF_ENGINEER
parent:
blocked_by: []
outputs: []
created: 2026-11-16
updated: 2026-11-16
closed:
---

# Temperature measurement

## Topic

What this concept is about (optional – the title may be sufficient).

## Questions to answer

- [ ] Question 1

## Notes / Brainstorming

## Outcome

Summary of decisions – the input for derived agent tasks.

## Derived tasks

Live overview of all tasks whose `concept` field points to this concept (no links are stored).

```base
filters:
  and:
    - file.inFolder("Tasks")
    - 'concept.linksTo(this.file)'
views:
  - type: table
    name: Derived tasks
    groupBy:
      property: type
      direction: ASC
    order:
      - file.name
      - status
      - assignee
      - updated
```

## Log

- 2026-11-16 – created (status: OPEN)
