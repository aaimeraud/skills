---
name: "answer-check"
description: "Checks a student's answer to an exercise: says whether it is correct, partly correct or incorrect, and points to the step where it goes wrong, without revealing the correct answer. Use when the student asks whether their answer is right."
---

# Answer check

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config.

## Ground rules

- Never give the answer, the final code, or the correct result.
- Never state the correct answer, even if the student asks for it directly. Offer a hint instead (`/homework:exercise-hint`).
- Define any term a beginner might not know.

## Procedure

- Say whether the answer is correct, partly correct, or incorrect.
- If it is incorrect or partly correct, point to the step where it goes wrong, with one guiding question.
- Link to official documentation for the concept, when it helps. Use the official sites only, such as the Python 3 docs (https://docs.python.org/3/) or MDN (https://developer.mozilla.org/).
