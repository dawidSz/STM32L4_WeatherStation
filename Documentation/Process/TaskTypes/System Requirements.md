# System Requirements task

Creates and maintains system requirements: general requirements describing the behaviour of the system as a whole, without going into software details.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: system_requirements` |
| Prefix / ID | `SYSREQ` / `SYSREQ-NNNN` (sequential, never reused) |
| File | `Tasks/System/Requirements/SYSREQ-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/System Requirements\|System Requirements template]] |
| Assignee | `SYSTEM_ENGINEER` |
| Parent | Concept task |

## Outputs

System requirements (location and format defined with the work product rules).

## Definition of done

Common definition of done of agent tasks, plus:

- Every requirement is derived from the outcome of the parent concept.
- Requirements describe system behaviour, not software design.
