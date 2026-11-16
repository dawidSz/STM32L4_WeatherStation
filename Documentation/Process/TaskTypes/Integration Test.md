# Integration Test task

Specifies and executes integration tests verifying the interaction of components through their interfaces.

The lifecycle (statuses, transitions, state diagram) and the common fields are shared by all
agent tasks: see [[Process/TaskTypes/AgentTask|Agent task lifecycle]].

## Identification

| Item | Rule |
|------|------|
| Type | `type: integration_test` |
| Prefix / ID | `INTTEST` / `INTTEST-NNNN` (sequential, never reused) |
| File | `Tasks/Test/Integration/INTTEST-NNNN Topic.md` |
| Template | [[Process/Templates/Tasks/Integration Test\|Integration Test template]] |
| Assignee | `TEST_ENGINEER` |
| Parent | Software architecture task or system architecture task |

## Outputs

Integration test specification, test code and test results.

## Definition of done

Common definition of done of agent tasks, plus:

- All specified tests are executed and the results are recorded.
