# Software Requirements task

Derives software requirements from the system requirements and the system architecture.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: sw_requirements` |
| Prefix / ID | `SWREQ` / `SWREQ-NNNN` (sequential, never reused) |
| File | `Tasks/Software/Requirements/SWREQ-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Software Requirements\|Software Requirements template]] |
| Assignee | `SW_ARCHITECT` |
| Parent | System architecture task or system requirements task |

## Outputs

Software requirements (location and format defined with the work product rules).

## Definition of done

Common definition of done of agent tasks, plus:

- Every software requirement is derived from a system requirement or architecture element.
