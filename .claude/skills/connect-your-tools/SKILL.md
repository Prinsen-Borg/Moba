---
name: connect-your-tools
description: Use on a user's first task in the Moba repository, or when a task needs their mail, calendar or meeting notes and those connections are missing. Offers to connect the approved tools from CONNECTORS.md, once and without pressure.
metadata: owner IT & Digital Transformation · version 0.1 · applies to Claude (Copilot has M365 natively)
---

## Goal
New users get their mail, calendar and meeting notes connected in their first week. Nobody is nagged, and nobody is ever asked for a password.

## Steps
1. **Check what is already there.** Look at the tools available in this session. Mail and calendar count as connected if a Microsoft 365 or Outlook connector is present (or Gmail/Google Calendar on a personal account). Meeting notes count as connected if a Granola connector is present.
2. **Everything is connected:** say nothing and continue with the task.
3. **Something is missing:** ask **one** short question, then continue with the task whatever the answer. Example:
   > "To help with mail, agenda and meeting follow-up, I can connect to your Outlook and Granola. Do you want to set that up now? It takes about two minutes."
4. **The user says yes:** for each missing connection, explain in one or two lines:
   - Go to **Settings → Connectors** in the Claude app (or use the connector card if the app shows one).
   - Find the connector, click **Connect** and sign in with your **Moba account** on the provider's own page.
   - Tell me when it is done; I will check that it works by listing today's meetings.
5. **The user says no or not now:** accept it, finish the task without those tools and do not ask again in this session.
6. **Verify:** after connecting, run one harmless read (for example today's calendar or the latest meeting title) and confirm in one sentence.

## Output
One question at most, short setup instructions if wanted, and a one-line confirmation that it works.

## Example
User: "Prepare me for tomorrow." No calendar connector is present.
Claude: "I can do this better with your calendar and meeting notes. Shall I help you connect Outlook and Granola first? It takes two minutes." The user says yes, connects both, and Claude lists tomorrow's four meetings with notes from earlier sessions.

## Never
- Never ask for, accept or repeat a password, API key or authentication code. If a user pastes one, tell them to change it.
- Never connect anything not listed in `CONNECTORS.md`.
- Never ask more than once per session or block the user's task until they connect.
- Never read mail or notes "to check if it works" beyond the one harmless read in step 6.

## Gotchas
- On a Moba laptop, the Microsoft 365 connector may need admin consent first. If sign-in shows "Need admin approval", tell the user to contact the IT service desk; this is expected and not their error.
- Copilot users already have mail and calendar. Skip this skill in Copilot.
- Personal and Moba accounts can both be signed in. Ask which one to use when unsure.
