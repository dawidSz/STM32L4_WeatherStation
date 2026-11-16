# System Architecture task

Creates the system architecture: the first split of system requirements into functionalities and high-level components (e.g. display handling, sensor handling, format of the displayed image), the deployment diagram and the description of the available hardware.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: system_architecture` |
| Prefix / ID | `SYSARCH` / `SYSARCH-NNNN` (sequential, never reused) |
| File | `Tasks/System/Architecture/SYSARCH-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/System Architecture\|System Architecture template]] |
| Assignee | `SYSTEM_ENGINEER` |
| Parent | System requirements task or concept task |

## Outputs

System architecture in `Architecture/System Level/`.

## Definition of done

Common definition of done of agent tasks, plus:

- Every system requirement in scope is allocated to at least one component.
