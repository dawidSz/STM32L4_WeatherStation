# Environment Setup task

Sets up and maintains the development environment: toolchain, build system, debugging, test frameworks, CI.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: environment_setup` |
| Prefix / ID | `ENVSETUP` / `ENVSETUP-NNNN` (sequential, never reused) |
| File | `Tasks/Support/Environment/ENVSETUP-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Environment Setup\|Environment Setup template]] |
| Assignee | `SW_DEVELOPER` |
| Parent | Optional – any task that needs the environment; empty for standalone setup work |

## Outputs

Configuration and scripts in the repository and their description.

## Definition of done

Common definition of done of agent tasks, plus:

- The setup is reproducible from the description in the repository.
