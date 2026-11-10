# Task creation rules

Rules that every new task type must satisfy when it is defined in a project's process.

## Deliverables of a new task type

1. Task type description in the process documentation (e.g. `Process/TaskTypes/<Type>.md`).
2. Task template (e.g. `Process/Templates/Tasks/<Type>.md`).
3. Folder for the task instances.
4. A row in the task type table of the process strategy (type, prefix, owner, description, template).

## Identification

- Every task type has a unique **prefix** of 3 uppercase letters (e.g. `CON` for concept tasks),
  registered in the task type table of the process strategy to avoid collisions.
- Task ID format: `PREFIX-NNNN` (4 digits, zero-padded, sequential, never reused), e.g. `CON-0001`.
- File name: `PREFIX-NNNN Topic.md`, e.g. `CON-0001 TFT display support.md`. Spaces are allowed;
  square brackets and `# ^ |` are not (they break Obsidian links).

## Statuses

- Every task type defines its statuses; each status has a one-sentence meaning.
- Status names are UPPERCASE, words separated with `_` (e.g. `IN_PROGRESS`).
- The initial status and the final statuses are stated explicitly, including a status for
  abandoned tasks (e.g. `DROPPED`).
- The same name is used for the same meaning across task types wherever possible.

## Transitions

- Every task type has a transition table: transition, who may perform it (role) and condition.
- Every task type defines the criteria for reaching a final status (definition of done).
- Every status change updates `updated` (and `closed` when a final status is reached) and adds an
  entry to the task's Log section.

## State diagram

- The task type description contains a Mermaid state diagram (`stateDiagram-v2`) of all
  transitions, next to the status table.
- The diagram is not part of the template nor of task instances, so instances do not carry
  outdated diagrams.
- Hints in the template (allowed values, file name, etc.) are placed in a section marked as
  removed on task creation.

## Fields (YAML frontmatter)

Tasks must be usable in tables and overviews (e.g. Obsidian Bases).

- Common base fields, identical in all task types:

  | Field | Content |
  |-------|---------|
  | `type` | Task type, lowercase (e.g. `concept`) |
  | `id` | Task ID (`PREFIX-NNNN`) |
  | `title` | Mandatory, short keyword-style title |
  | `status` | Current status – the single source of truth |
  | `assignee` | Role responsible for the task (e.g. `CHIEF_ENGINEER`) |
  | `parent` | Link to the source task; empty for top-level tasks |
  | `created` | Date the task was created |
  | `updated` | Date of the last change |
  | `closed` | Date a final status was reached; empty until then |

- Type-specific fields are added next to the base fields.
- Dates use the `YYYY-MM-DD` format.
- Flat structure only: no nested objects; links are lists of wikilinks.
- A description in the task body is optional; the title may be sufficient.

## Traceability

- Every task type defines its relation fields (e.g. `parent`, `implements`, `verifies`).
- Links always point from the derived element to its source, never the other way round.
- Links are kept only in YAML fields; the template contains no wikilinks to process documents
  (they would become hub nodes in the graph).
