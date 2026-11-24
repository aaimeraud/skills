---
name: "linear-sync"
description: "Copies the current Linear issue, its milestone and the project documents into the student's private homework folder, so the other homework commands can read them as the brief. Use when the homework source is a Linear project, after setup, or when the student starts another issue."
---

# Linear sync

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. If its `source` is not `linear`, say that this command is for a Linear source, and stop. Reply in the language set in the config.

Linear tools must be available in the session. If they are not, say that the Linear connector must be connected, and stop.

## Ground rules

- Read Linear only. Never create, edit or comment on anything in Linear.
- Write only inside `.homework/linear/`. The folder is ignored by git: never commit its content.
- Copy the text as it is. Do not summarise or rewrite the issue.

## Procedure

1. **Find the current issue**, in this order:
   - the identifier the student gives (for example `ENG-40`);
   - the current git branch (`git branch --show-current`): Linear branch names contain the identifier, for example `user/eng-40-add-export` gives `ENG-40`;
   - otherwise, list the open issues of the project and ask which one.
2. **Fetch the issue**: title, description, milestone, priority, status, and its "blocked by" relations.
3. **Fetch the milestone**: its name, description, and the title and status of each of its issues.
4. **Fetch the project documents**: every document attached to the project in `linear project`.
5. **Write the files**, each starting with a line `Synced from <identifier or title> on <YYYY-MM-DD>`:
   - `.homework/linear/issue.md`: the current issue.
   - `.homework/linear/milestone.md`: the milestone and its issues.
   - `.homework/linear/docs/<document title>.md`: one file per document.
6. **Update the config**: set `brief` to `.homework/linear/issue.md`, set `current issue` to the identifier, and list the document files as resources.
7. **Report** in two or three lines: the current issue, what it is blocked by if anything is still open, and the files written.

## Reading the issue

Issue sections may be written in any language, so recognise them by meaning, not by exact heading. The usual learning sections are: objective, concepts, requirements, steps, success criteria, hints and documentation. The other homework commands rely on this:

- objective and requirements form the exercise;
- success criteria are the review criteria;
- hints come before any new hint;
- documentation links come before the general catalogue.
