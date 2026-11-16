# Software Implementation task

Implements software components and integrates them into the firmware according to the software architecture.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: sw_implementation` |
| Prefix / ID | `SWIMPL` / `SWIMPL-NNNN` (sequential, never reused) |
| File | `Tasks/Software/Implementation/SWIMPL-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Software Implementation\|Software Implementation template]] |
| Assignee | `SW_DEVELOPER` |
| Parent | Software architecture task |

## Outputs

Source code and build files in `SW/`.

## Definition of done

Common definition of done of agent tasks, plus:

- The firmware builds without errors.
- The implementation follows the software architecture and its interfaces.
