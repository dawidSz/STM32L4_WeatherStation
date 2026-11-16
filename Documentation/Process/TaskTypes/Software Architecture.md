# Software Architecture task

Creates the software architecture: software components, their responsibilities and interfaces.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: sw_architecture` |
| Prefix / ID | `SWARCH` / `SWARCH-NNNN` (sequential, never reused) |
| File | `Tasks/Software/Architecture/SWARCH-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Software Architecture\|Software Architecture template]] |
| Assignee | `SW_ARCHITECT` |
| Parent | Software requirements task |

## Outputs

Software architecture in `Architecture/Software Level/`.

## Definition of done

Common definition of done of agent tasks, plus:

- Every software requirement in scope is allocated to a component.
- Interfaces between components are defined.
