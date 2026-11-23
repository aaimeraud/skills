---
name: "exercise-review-all"
description: "Reviews every exercise in the student's brief and returns one line per exercise with its status and score. Use when the student wants an overview of all their homework at once."
---

# Review all

Read `../shared/rules.md` first and follow it.

Review each exercise in the brief named in `.homework/config.md`, using the same procedure as `/homework:exercise-review`: status, score out of 5, and the evidence behind it. Keep every line short.

Reply with one line per exercise, in this format:

```
Exercise N: DONE, 5/5. <one sentence>
Exercise N: NOT DONE, 2/5. <one sentence>
```

Do not list the problems here. The student can run `/homework:exercise-review N` for the details.
