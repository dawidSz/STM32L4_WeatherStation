# Process Improvement task

Improves the project's engineering process described in `Process/` (strategy, task types, templates). It does not cover the rules for cooperation with Claude Code, which are maintained separately.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: process_improvement` |
| Prefix / ID | `PROCIMPROV` / `PROCIMPROV-NNNN` (sequential, never reused) |
| File | `Tasks/Support/ProcessImprovement/PROCIMPROV-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Process Improvement\|Process Improvement template]] |
| Assignee | `CHIEF_ENGINEER` |
| Parent | Optional – the task that revealed the improvement; empty otherwise |

## Outputs

Changed process documents in `Process/`.

## Definition of done

Common definition of done of agent tasks, plus:

- The strategy, task type descriptions and templates are consistent with each other.
