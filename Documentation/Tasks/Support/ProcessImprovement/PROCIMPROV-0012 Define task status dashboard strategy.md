---
type: process_improvement
id: PROCIMPROV-0012
title: "Define task status dashboard strategy"
status: IN_PROGRESS
assignee: CHIEF_ENGINEER
parent:
concept:
blocked_by: []
outputs:
  - "Process/Strategy.md"
created: 2026-11-16
updated: 2026-11-16
closed:
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
- To verify in Obsidian: Bases filter syntax, especially `concept.linksTo(this.file)`.

## Log

- 2026-11-16 – created (status: OPEN)
- 2026-11-16 – status: OPEN → IN_PROGRESS
