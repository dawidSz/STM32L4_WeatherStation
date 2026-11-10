# Project specific information

This is the only file in this vault that refers to a concrete project. Everything else in
`ClaudeCooperationRules/` is project-independent; when the vault is reused in another project,
only this file is rewritten.

## Project

**STM32L4 Weather Station** – embedded firmware for a weather station based on an STM32L4
microcontroller (hardware details: TBD). The project is also a pilot for a repeatable,
agent-based engineering process: the user acts as Chief Engineer / Architect, the main Claude Code
session acts as orchestrator delegating work to specialised agents.

## Process – start here

The software development and project management process is described in the process strategy:

**`Documentation/Process/Strategy.md`** (path relative to the repository root)

Read it before working on any task. It describes roles, task types, statuses and the
documentation structure, and links to the detailed process rules.

## Status

Process definition in progress. Defined so far: Concept task type. Agent task types, ADR and note
templates, agent profiles: TBD.

## Repository layout

| Path | Content |
|------|---------|
| `Documentation/` | Obsidian vault of the project: process, tasks, architecture |
| `SW/` | Software project: STM32CubeMX configuration, source code, build files |
| `ClaudeCooperationRules/` | This vault: project-independent rules for cooperation with Claude Code |
