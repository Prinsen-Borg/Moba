# Moba: AI context & design repository

The shared "brain" for AI assistants at Moba. When you clone this repository and open it in Claude, Copilot or Cursor, the assistant knows who Moba is, how we work and what our output should look like.

## Start here

| File | What it gives you |
|---|---|
| [`AGENTS.md`](AGENTS.md) | Rules every AI agent follows |
| [`DESIGN.md`](DESIGN.md) | Moba brand and visual system |
| [`VERSION_CONTROL.md`](VERSION_CONTROL.md) | How we branch, commit and review |
| [`.claude/skills/`](.claude/skills) | Reusable procedures, such as building a web page |
| [`tools/design-showcase/`](tools/design-showcase/index.html) | Living demo of the design system |

## Try it

1. Clone the repo and open the folder in Claude Code or VS Code with Copilot.
2. Ask: *"Build a one-page overview of our IT initiatives in Moba style."*
3. The agent reads `AGENTS.md`, then `DESIGN.md`, then the `moba-web-page` skill, and produces an on-brand page.

Owner: IT & Digital Transformation
