---
name: "journal"
description: "Drafts a dated journal entry (progress, decisions, difficulties, next step) from the current work session and, after the learner approves it, appends it to the Linear project's Journal document or to a local file. Use when the learner wants to log a session."
---

# Journal

## Before you start

Read `.mentor/config.md`. If it does not exist, tell the learner to run `/mentor:setup` first, and stop. Reply in the language set in the config.

## Ground rules

- Write to Linear only after the learner approves the exact entry, and only by appending to the Journal document. Never edit earlier entries, issues or other documents.
- The entry is the learner's: it may use the first person, and the learner's corrections win.
- Never put solution code in the entry.

## Procedure

1. **Gather the session**: the current issue from the config, the commits on the current branch (`git log main..HEAD --oneline`), the hints and reviews given in this conversation, and what the learner says about the session.
2. **Draft the entry** in the config language, with today's date and four short parts:

```markdown
## <linear-date date="YYYY-MM-DD">YYYY-MM-DD</linear-date> · <issue identifier>

### Progress
### Decisions
### Difficulties
### Next
```

   Translate the four headings into the config language. Under Difficulties, name each blocker and how it was solved, or that it is still open. For a local file, write the date as plain text instead of the `linear-date` element.
3. **Show the draft** and ask whether to append it as is, change it, or drop it.
4. **Append it** once approved:
   - With a Linear source, find the project document whose title means "Journal" and append the entry at the end. If there is none, ask whether to create a Journal document in the project or to keep the entry in `.mentor/journal.md`.
   - Otherwise, append it to `.mentor/journal.md`.
5. **Confirm** where the entry was written, with the link when it is in Linear.
