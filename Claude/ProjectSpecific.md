# Project specific information

This is the only file in this vault that refers to a concrete project. Everything else in
`Claude/` is project-independent; when the vault is reused in another project,
only this file is rewritten.

## Project

**STM32L4 Weather Station** – embedded firmware for a weather station based on an STM32L4
microcontroller. The project is also a pilot for a repeatable,
agent-based engineering process: the user acts as Chief Engineer / Architect, parallel Claude Code
sessions take agent roles (orchestrator, engineers, reviewer, ...).

## Process – start here

The software development and project management process is described in the process strategy:

**`Documentation/Process/Strategy.md`** (path relative to the repository root)

Read it before working on any task. It describes roles, task types, statuses and the
documentation structure, and links to the detailed process rules.

## Start of session

If no role has been assigned, start the session with a review of the tasks assigned to the Chief
Engineer and present them as "To do":

- Tasks are the files in `Documentation/Tasks/`; read their YAML frontmatter.
- Include tasks with `assignee: CHIEF_ENGINEER` and a status other than `DONE`, `DROPPED` or
  `IMPLEMENTED` (the same criteria as `Documentation/Tasks/Dashboards/My open tasks.base`).
- Group them by status and type; show ID, title and status.

The current state of the project is defined only by the tasks; there is no separate status list.

## Repository layout

| Path | Content |
|------|---------|
| `Documentation/` | Obsidian vault of the project: process, tasks, architecture |
| `SW/` | Software project: STM32CubeMX configuration, source code, build files |
| `Claude/` | This vault: project-independent rules for cooperation with Claude Code |
