---
name: meeting-to-actions
description: Use when the user asks for actions, decisions or follow-ups from one or more meetings (Granola notes or Teams recap). Turns meeting notes into a clean action list per owner.
metadata: owner IT & Digital Transformation · version 0.1
---

## Goal
A short, checked list of decisions and actions from a meeting, with an owner and a date for each, that the user can paste into a task list or follow-up mail.

## Steps
1. Find the meeting(s): by title, date or participant. If more than one matches, ask which one.
2. Read the summary first and the transcript only if the summary lacks owners or dates.
3. Extract:
   - **Decisions**: what was agreed.
   - **Actions**: what, who and by when. Mark a missing owner or date as "to confirm".
   - **Open questions**: anything unresolved.
4. Separate facts from interpretation: use "(assumed)" for anything not said explicitly.
5. Show the list to the user first. Then offer one next step: a follow-up mail draft, or adding the actions to the user's task list.
6. **Adding to the task list:** if the user has a personal task list (see `tools/task-list/README.md`), write the user's *own* actions there in the documented data format, with `addedBy: "claude"`. Check for existing tasks first and update instead of duplicating. Actions owned by others go in the follow-up mail, not in the user's list. If the user has no list yet, offer to set one up.

## Output
```
Meeting: <title>, <date>
Decisions
- …
Actions
- [ ] <action> | <owner> | <date or "to confirm">
Open questions
- …
```

## Never
- Never quote personal remarks, HR matters or sensitive details in the output.
- Never store the transcript or the action list in this repository.
- Never send the follow-up mail yourself; draft it for the user to send.

## Gotchas
- Automatic transcripts misspell names. Check spellings against the meeting invitation.
- A note titled "New note" is often a test or a solo voice memo. Confirm before treating it as a meeting.
