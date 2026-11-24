---
name: "journal"
description: "Drafts a dated journal entry (progress, decisions, difficulties, next step) from the current work session and, after the student approves it, appends it to the Linear project's Journal document. Use when the student wants to log a session, or asks to update their journal."
---

# Journal

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config.

## Ground rules

- Write to Linear only after the student approves the exact entry, and only by appending to the Journal document. Never edit earlier entries, issues or other documents.
- The entry is the student's: it may use the first person, and the student's corrections win.
- Never put solution code in the entry.

## Procedure

1. **Gather the session**: the current issue from the config, the commits on the current branch (`git log main..HEAD --oneline`), the reviews and hints given in this conversation, and what the student says about the session.
2. **Draft the entry** in the config language, with today's date and four short parts:

```markdown
## <linear-date date="YYYY-MM-DD">YYYY-MM-DD</linear-date> · <issue identifier>

### Progress
### Decisions
### Difficulties
### Next
```

   Translate the four headings into the config language. Under Difficulties, name each blocker and how it was solved, or that it is still open.
3. **Show the draft** and ask whether to append it as is, change it, or drop it.
4. **Append it** once approved:
   - With a Linear source, find the project document whose title means "Journal" and append the entry at the end. If there is none, ask whether to create a Journal document in the project or to keep the entry in `.homework/journal.md`.
   - Otherwise, append it to `.homework/journal.md`.
5. **Confirm** where the entry was written, with the link when it is in Linear.
