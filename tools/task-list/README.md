# task-list

A personal task list in Moba style. **Claude adds tasks** (for example from meeting notes); **you tick them off**.

- Purpose: one place for actions from meetings, voice memos and mail, filled by the `meeting-to-actions` skill.
- Owner: IT & Digital Transformation · created 2026-10-09 · v0.1

## Why not Microsoft To Do or Planner?

Microsoft To Do (personal) and Planner (team) are the Moba standard. **Today, Claude cannot write into them.** The Microsoft 365 connector can only read mail, calendar, Teams and SharePoint. Until that changes, this page is the bridge:

| Need | Use |
|---|---|
| Claude collects and updates your actions | This task list |
| Team tasks with shared owners | Planner (copy tasks across by hand) |
| Copilot users | Microsoft To Do; Copilot works there natively |

Revisit this choice when a Microsoft To Do or Planner connector becomes available. Add it to `CONNECTORS.md` and update the `meeting-to-actions` skill.

## Set up your own list (once, about 2 minutes)

1. Open Claude (chat), with this repository available.
2. Ask: *"Publish tools/task-list/index.html as my personal task list, with the db capability."*
3. Claude publishes it as a private page that only you can open, and gives you the link. Pin it in your sidebar.
4. From then on, ask: *"Get the to-dos from today's meetings and add them to my task list."*

Each person gets their **own** copy with its own data. Never share your list's link with edit rights; it can contain meeting details.

## Data format (for agents)

Collection `tasks`, one document per task. Use a readable `doc_id`, e.g. `moba-mt-intro`.

| Field | Type | Example |
|---|---|---|
| `title` | string | "Prepare 2-minute introduction for the MT meeting" |
| `due` | `YYYY-MM-DD` or `null` | "2026-10-12" |
| `dueNote` | string, optional | "Date to confirm" |
| `status` | `open` · `done` | "open" |
| `owner` | string | "Eric" |
| `source` | string | "Moba intro with Erik Wasbauer, 9 Oct" |
| `addedBy` | `claude` · `you` | "claude" |
| `createdAt` | ISO timestamp | "2026-10-09T18:10:00Z" |

Rules: never put meeting quotes, personal remarks or confidential figures in a task title (AGENTS.md §5). Before adding, check for an existing task with the same meaning and update it instead of creating a duplicate.
