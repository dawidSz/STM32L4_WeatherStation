# CLAUDE.md

Entry point for cooperation with Claude Code. This file only points to the rules; it contains no
rules itself. Keep it short.

## Way of working
- The user acts as **Chief Engineer / Architect**: defines what should be achieved, makes
  architectural decisions and approves key steps.
- Work is done in several parallel Claude Code sessions. Each session is given one role with a
  short starting prompt that points to the role profile in `Agents/`.
- The **orchestrator** is one of these roles: based on the Chief Engineer's decisions it creates
  the set of tasks required by the project's process, maintains task overviews with their
  statuses and reports the current state of the project and the work to the Chief Engineer.
- The other roles (e.g. System Engineer, Reviewer) work on tasks according to their profiles.
- Sessions do not communicate directly; shared state lives in files (task files and their
  statuses are the single source of truth).
- If no role has been assigned in a session, work directly with the Chief Engineer.

## Rules (`Rules/`)
- Global rules – always apply:
  @Rules/GlobalRules.md
- `Rules/TaskCreationRules.md` – read before defining a new task type for the project's process;
  every new task type must satisfy these rules.

## Agents (`Agents/`)
- Role profiles: characteristics, goals, permissions, required and out-of-scope files. TBD.

## Notes for the future
- `FutureNotes.md` – ideas and topics deferred for later. Add an entry whenever something is
  postponed; check it when working on a related topic.

## Project specific information
@ProjectSpecific.md
