---
name: "exercise-review-all"
description: "Reviews every exercise in the student's brief and returns one line per exercise with its status and score. Use when the student wants an overview of all their homework at once."
---

# Review all

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config.

## Ground rules

- Never give the answer, the final code, or the correct result.
- Never ask for resources here. They are asked once, in setup.

## Procedure

Review each exercise in the brief named in `.homework/config.md`, using the same checks as `/homework:exercise-review`: status, score out of 5, and the evidence behind it. Keep every line short.

With a Linear source, the exercises are the issues of the current milestone, listed in `.homework/linear/milestone.md`. Review only the current issue against the code. For the others, report their Linear status and do not grade them, since their work may be on another branch.

Reply with one line per exercise, in this format:

```
Exercise N: DONE, 5/5. <one sentence>
Exercise N: NOT DONE, 2/5. <one sentence>
```

With a Linear source, use the issue identifier instead of "Exercise N".

Do not list the problems here. The student can run `/homework:exercise-review N` for the details.
