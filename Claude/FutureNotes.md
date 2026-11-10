# Future notes

Ideas and topics deferred for later. Each entry says what to remember and when it becomes
relevant. Remove an entry once it has been addressed.

## Agent role profiles

- **Enforce permissions technically, not only in the profile.** A rule like "the Reviewer must not
  modify code" in a prompt is a request, not a restriction. Claude Code can block tools or paths
  when a session starts (per-role permission settings or CLI flags), e.g. deny editing `SW/**` for
  the Reviewer. The profile explains *why*, the settings *enforce* it. Verify the exact mechanism
  when implementing. *Relevant when:* defining the first role profiles.
- **List out-of-scope files and topics in every profile.** Reading cannot be blocked, but telling
  the agent what is irrelevant keeps it focused and reduces the number of tokens used.
  *Relevant when:* writing each role profile.
- **Role profile may fade after context compaction.** A profile read on request is summarised in
  long sessions, unlike `CLAUDE.md`. Options: keep profiles short, add a rule "re-read your
  profile after compaction", or load the role as the session's system prompt at startup (verify).
  *Relevant when:* defining the role profile template.
- **Status transitions per role.** Each profile should state which task status transitions the
  role may perform; this complements the transition tables in the task type definitions.
  *Relevant when:* defining role profiles and agent task types.
- **Concurrent edits between sessions.** Two sessions editing the same file overwrite each other.
  Roles that modify code may need separate git worktrees. *Relevant when:* the first
  code-producing role is defined.

## Traceability and artifact model

To be elaborated together with the ADR and note templates. Goal: a concept task (feature-level,
e.g. "TFT display support") links to the tasks and work products created for it (notes, ADRs,
requirements, architecture, implementation, tests), so that it is visible what was produced
within the concept. The Obsidian graph with plain links is sufficient; relation types do not need
to be visible in the graph.

- **Links only in typed YAML fields** (`parent`, `derived_from`, `implements`, `verifies`, ...).
  No ad-hoc wikilinks in note bodies, to avoid linking everything with everything.
- **One direction only:** a derived element points to its source, never the other way round.
  The concept does not list its children; they are visible in backlinks and the local graph.
- **No links from tasks to process documents** (strategy, task type descriptions, templates);
  they would become hub nodes connected to everything.
- **Check the Concept template:** its comment contains wikilinks (`[[Process/TaskTypes/Concept|...]]`,
  `[[CON-NNN_...]]`) that may create noise in the graph; replace them with plain text if needed.
- **Reconsider the `outputs` field of the Concept task:** it duplicates `parent` in ADRs and notes
  in the opposite direction. Proposal: remove it and rephrase the `BRAINSTORMING` →
  `IN_IMPLEMENTATION` condition accordingly.
- **Tools:** local graph of a concept (depth 2–3) for a quick overview; Bases views embedded in the
  concept for a status overview of derived elements, if needed.

*Relevant when:* defining ADR and note templates and the agent task types.
