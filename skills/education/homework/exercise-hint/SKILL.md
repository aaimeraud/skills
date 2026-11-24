---
name: "exercise-hint"
description: "Gives a student a four-step hint for one exercise, with one official documentation link and one guiding question, never the solving code. Use when the student is stuck and asks for a hint."
---

# Hint

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config.

With a Linear source, the exercise is the current issue in `.homework/linear/issue.md`. If the current git branch names another issue than `current issue`, tell the student to run `/homework:linear-sync` first, and stop.

## Ground rules

- Never write solving code, the answer, or the correct result.
- Define any term a beginner might not know.

## Procedure

Use exactly four steps, under about ten lines in total:

1. Restate the goal in one sentence.
2. Name the concept involved.
3. Give one official documentation link on that concept. Use the sites listed below, or another official site for the subject.
4. Ask one guiding question about the first step to take.

With a Linear source, start from the issue's hints section: use the first hint the student has not seen yet in this conversation before writing a new one, and prefer the links of the issue's documentation section.

## Guide mode

When the config `mode` is `guide`, the student works on their own project, and the hint may go further than four steps:

- Read the student's code and point to the part that blocks them.
- Explain the concept in a few sentences, defining each term.
- Show a short example on a different problem than the issue, for example `errors.Is` on a file error rather than on the error the issue defines.
- Give two or three links targeted at the problem met or the concepts around it.

Even in guide mode, never write the code the issue asks for, and never correct the student's line directly. End with one guiding question.

## Official documentation

- Python 3: https://docs.python.org/3/
- The Rust Book: https://doc.rust-lang.org/stable/book/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- Go: https://go.dev/doc/
- MDN Web Docs: https://developer.mozilla.org/
- PostgreSQL: https://www.postgresql.org/docs/
- SQLBolt: https://sqlbolt.com/
- Big-O Cheat Sheet: https://www.bigocheatsheet.com/
- Paul's Online Math Notes: https://tutorial.math.lamar.edu/
- MIT OpenCourseWare: https://ocw.mit.edu/
