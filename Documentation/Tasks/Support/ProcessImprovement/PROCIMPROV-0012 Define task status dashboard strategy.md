---
type: process_improvement
id: PROCIMPROV-0012
title: "Define task status dashboard strategy"
status: DONE
assignee: CHIEF_ENGINEER
parent:
concept:
blocked_by: []
outputs:
  - "Process/Strategy.md"
  - "Process/TaskTypes/AgentTask.md"
  - "Process/Templates/Tasks/Concept.md"
  - "Tasks/Dashboards/Waiting for approval.base"
  - "Tasks/Dashboards/Concepts to close.base"
  - "Tasks/Dashboards/My open tasks.base"
  - "Tasks/Dashboards/Process Improvement.base"
  - "Tasks/Dashboards/Environment Setup.base"
  - "Tasks/Dashboards/Concepts.base"
created: 2026-11-16
updated: 2026-11-18
closed: 2026-11-18
---

# Define task status dashboard strategy

## Scope

Define how the current status of tasks is presented in dashboards.

- [x] Identify the audiences and their questions (Chief Engineer, orchestrator, agents)
- [x] Define the dashboard views (e.g. per task type, per status, per assignee, per concept)
- [x] Choose the technology (e.g. Obsidian Bases) and the location of dashboard files
- [x] Define which YAML fields the dashboards rely on and whether task fields need changes
- [x] Describe the strategy in the process documentation

## Notes

- Decisions: three Chief Engineer dashboards (Waiting for approval: agent tasks in IN_REVIEW;
  Concepts to close: concepts in IN_IMPLEMENTATION; My open tasks: own tasks not in a final
  status); separate dashboards for process improvement and
  environment setup; concept overview via the new `concept` field and a base embedded in the
  concept template.
- IN_REVIEW → DONE is now approved by the Chief Engineer after the Reviewer's review.
- Bases filter syntax (especially `concept.linksTo(this.file)`) was not verified in Obsidian
  within this task.

## Summary

- **Strategy:** new section "Dashboards" in `Process/Strategy.md` – dashboards are Obsidian Bases
  in `Tasks/Dashboards/`, they only read task YAML fields and store no data; task files remain
  the single source of truth. Rules: statuses are changed only in task files, every new dashboard
  is listed in the strategy, dashboards are updated together with the task fields they use.
- **Dashboards:** Waiting for approval (agent tasks in `IN_REVIEW`), Concepts to close (concepts
  in `IN_IMPLEMENTATION`), My open tasks (Chief Engineer's tasks not in a final status), Process
  Improvement and Environment Setup (active and all), Concepts (agent tasks grouped by concept).
- **Task fields:** new `concept` field in all agent task templates (link to the source concept,
  copied from the parent task), because Bases cannot follow the `parent` chain over several
  levels.
- **Concept template:** embedded base "Derived tasks" listing the concept's tasks grouped by task
  type.
- **Lifecycle:** `IN_REVIEW` → `DONE` is approved by the Chief Engineer after the review.
- **Session start:** a session without a role starts with a review of the open tasks assigned to
  the Chief Engineer (same criteria as My open tasks).

## Log

- 2026-11-16 – created (status: OPEN)
- 2026-11-16 – status: OPEN → IN_PROGRESS
- 2026-11-18 – status: IN_PROGRESS → IN_REVIEW
- 2026-11-18 – review by the Chief Engineer passed; status: IN_REVIEW → DONE
