---
name: "exercise-review"
description: "Reviews one homework exercise for a student: status (DONE or NOT DONE), a score out of 5, and up to three guiding problems with documentation links, never the answer. Use when the student asks to review, grade or check an exercise against its brief."
---

# Review

Read `../shared/rules.md` first and follow it.

## Input

- The exercise: the number or title the student gives. Find it in the brief named in `.homework/config.md`.
- The student's work: the file, code or text they point to.
- The criteria from the config. If the config has none, use the criteria in the brief.

## Procedure

1. Read the exercise and the criteria.
2. Check each requirement against the student's work. Note the evidence: the line, value or sentence that proves it.
3. Decide the status:
   - **DONE**: every requirement is met. Only then.
   - **NOT DONE**: at least one requirement is missing or wrong.
4. Give a score out of 5, based on the share of requirements met and their weight.
5. Write the reply in this shape:

```
**Status:** DONE | NOT DONE
**Score:** X/5

<3 to 4 sentences: what works, what is missing, and why it matters.>

1. <problem>. <one guiding question>. <doc link>
2. ...
3. ...
```

Up to three problems. Each problem names the issue, asks one guiding question, and links to official documentation (see `../shared/catalogue.md`). Never give the corrected line, value, or code.
