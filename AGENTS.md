# AGENTS.md: Instructions for AI agents working in the Moba repository

This file is the **single source of truth** for every AI assistant that works with this repository (Claude, GitHub Copilot, Cursor, Codex and others). Tool-specific files such as `CLAUDE.md` only point here.

---

## 1. Who we are

- **Moba** (Barneveld, NL) is the global market leader in egg grading, packing, processing and handling equipment. It is active in more than 100 countries.
- The positioning is "Building Your Sustainable Egg Future". We help egg producers become independent of scarce labour, get the most value out of every egg, fulfil 100% of their contracts and protect food safety.
- Core product families include **Omnia** (graders), **Mopack** (farm packers), **Proxima** (breakers), **Crono** and **M Loader** (loaders), **Forta** (topline), **Magna** (monitoring software) and the **Vision Shell Inspector** (AI crack detection).
- This repository belongs to **IT & Digital Transformation**. It holds the shared context, standards and skills that make AI assistants useful and consistent across Moba.

## 2. What this repository is (and is not)

| Is | Is not |
|---|---|
| Company context for AI: who we are, how we work, our standards | Application source code (that lives in product repos) |
| The design system (`DESIGN.md`, `design-system/`) | A document store or file share (use SharePoint) |
| Reusable **skills**: written procedures an agent follows | A place for personal data, HR files or customer data |
| Small internal tools and demo pages built from those standards | Production systems |

## 3. Repository map

```
AGENTS.md            ← you are here: rules for every agent
CLAUDE.md            ← Claude-specific pointer to this file
DESIGN.md            ← brand and visual rules (read before producing anything visual)
VERSION_CONTROL.md   ← branching and commit conventions
README.md            ← human introduction
context/             ← company and IT context (org, initiatives, principles)
design-system/       ← tokens.css and brand assets
.claude/skills/      ← skills (one folder per skill, each with a SKILL.md)
tools/               ← small web tools and demo pages, one folder each
```

## 4. Working rules for agents

1. **Read before you write.** For anything visual, read `DESIGN.md` and use `design-system/tokens.css`. Never invent brand colours or fonts.
2. **Use a skill when one exists.** Check `.claude/skills/` first. For example, any HTML page follows `moba-web-page`.
3. **Keep the language consistent.** Use English for repository files and anything customer-facing. Use Dutch only when the user writes in Dutch or the audience is internal NL.
4. **Write plainly.** Use short sentences, concrete numbers and no hype words. Name things the way users recognise them.
5. **Separate facts from assumptions.** Label assumptions explicitly. Never present invented figures as Moba data. Mark example data as an example.
6. **Make small, reviewable changes.** Follow `VERSION_CONTROL.md`: one feature branch per change, clear commit messages, and a pull request for review.
7. **Leave no secrets.** Never commit passwords, API keys, tokens, connection strings or personal data. If you find one, stop and tell the user.

## 5. Security & data classification

| Class | Examples | Allowed in this repo? |
|---|---|---|
| Public | Website content, product names, published brochures | Yes |
| Internal | Org structure, initiative list, architecture principles | Yes (repository is private) |
| Confidential | Security assessments, contracts, pricing, budgets | **No.** Reference the SharePoint location instead. |
| Personal data (AVG/GDPR) | Employee feedback, HR files, customer contacts | **Never** |

Moba had a security incident in 2026. Treat security hygiene as a first-class requirement, not an afterthought.

## 6. Output standards

- **Web pages:** follow `.claude/skills/moba-web-page/SKILL.md`.
- **Documents and slides:** follow the "Applying this outside the website" section in `DESIGN.md`.
- **Code:** comment the *why* rather than the *what*, include a README per tool, and avoid adding dependencies when plain HTML/CSS/JS is enough.

## 7. When in doubt

Ask the user one precise question instead of guessing on something that is hard to undo. For anything easy to redo, make a reasonable assumption, state it and proceed.
