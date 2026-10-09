# Copilot instructions for the Moba repository

**Read `AGENTS.md` in the repository root first.** It holds the shared rules for every AI tool at Moba, covering security, data classification, brand and way of working. This file only adds what is specific to GitHub Copilot and Microsoft 365 Copilot.

## Where things are

- Brand and visual rules: `DESIGN.md` and `design-system/tokens.css`
- Skills (step-by-step procedures): `.claude/skills/<name>/SKILL.md`. Copilot reads skills from this folder as well, so there is no separate Copilot copy.
- Department context: `departments/<DEPT>/AGENTS.md`. When working on files in a department folder, also follow that file.
- Approved connections: `CONNECTORS.md`

## Copilot-specific notes

- Mail, calendar, Teams and SharePoint are native to Microsoft 365 Copilot. **No connector setup is needed for those**, and the `connect-your-tools` skill applies to Claude only.
- Meeting notes from Teams recordings are available to Copilot through Teams recap. Granola notes are not; use Claude for those.
- Follow the Moba look from `DESIGN.md` for any page, document or slide you produce.
