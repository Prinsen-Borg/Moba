# CONNECTORS.md: Approved connections for AI assistants

Connectors let an assistant read (and sometimes act in) your own apps. **Each person connects their own account**, signing in on the app's own page. Access follows that person's existing permissions, and nobody sees another person's mail or notes.

> Status: **draft.** The organisation-wide Claude account, Microsoft admin consent and the privacy assessment (DPIA) are not yet in place. Until they are, connect only with approval from IT & Digital Transformation.

## Approved connections

| Connection | Tool | What it gives the assistant | Allowed use | Not allowed |
|---|---|---|---|---|
| **Microsoft 365: Outlook mail** | Claude (Copilot: native) | Read and search your mail; create drafts | Summaries, finding information, drafting replies | Sending mail without your explicit confirmation; forwarding mail content outside Moba |
| **Microsoft 365: Calendar** | Claude (Copilot: native) | Read your agenda; propose times | Daily briefing, meeting preparation | Accepting or declining invitations without confirmation |
| **Microsoft 365: SharePoint / OneDrive** | Claude (Copilot: native) | Search and read documents you already have access to | Research, summaries, finding the latest version | Copying confidential documents into this repository |
| **Granola: meeting notes** | Claude | Read your own meeting notes and transcripts | Action lists, meeting summaries, follow-up drafts | Sharing transcripts beyond the meeting's participants; recording without telling participants |

Requests for a new connector go to IT & Digital Transformation through a pull request that adds a row here.

## Ground rules

1. **Tell people when you record.** Mention at the start of a meeting that Granola or Teams is taking notes.
2. **Results only, never raw content.** Use mail and transcripts in your session, but store only the outcome (decisions, actions) in shared places, and never in this repository.
3. **Confirmation before action.** The assistant may draft, but you send, accept and delete.
4. **Never share secrets.** No assistant will ever ask for your password or an authentication code. Connecting always happens on the app's own sign-in page.
