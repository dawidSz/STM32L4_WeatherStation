# Unit Test task

Specifies and executes unit tests of software units.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: unit_test` |
| Prefix / ID | `UNITTEST` / `UNITTEST-NNNN` (sequential, never reused) |
| File | `Tasks/Test/Unit/UNITTEST-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Unit Test\|Unit Test template]] |
| Assignee | `TEST_ENGINEER` |
| Parent | Software implementation task or software architecture task |

## Outputs

Unit test specification, test code and test results.

## Definition of done

Common definition of done of agent tasks, plus:

- All specified tests are executed and the results are recorded.
