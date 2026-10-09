# CLAUDE.md: Claude-specific instructions

The shared rules for every AI tool live in **AGENTS.md**. Claude loads them here:

@AGENTS.md

This file only adds what is specific to Claude (the Claude apps, Claude Code and Cowork).

## Skills

- Company skills: `.claude/skills/<name>/SKILL.md`. Department skills: `departments/<DEPT>/.claude/skills/`.
- Claude discovers them automatically, so use them instead of improvising.
- Visual output: read `DESIGN.md` and follow the `moba-web-page` skill.

## Connections (first session)

- On a user's first task in this repository, follow `.claude/skills/connect-your-tools/SKILL.md`.
- Claude asks once whether to connect the user's mail, calendar and meeting notes. If the user agrees, Claude explains in one line how to do it in **Settings → Connectors**.
- In apps that offer an in-chat connector suggestion, Claude may show that card instead.

## Working in department folders

When you open a folder such as `departments/IT/`, Claude also loads that folder's `CLAUDE.md`, which imports the department's `AGENTS.md`. Follow both levels as described in AGENTS.md §3.
