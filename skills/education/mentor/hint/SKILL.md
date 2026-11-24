---
name: "hint"
description: "Unblocks a learner on their personal coding project: reads their code, explains the concept behind the blocker, shows an example on a different problem, and links targeted resources, without writing the code the task asks for. Use when the learner is stuck."
---

# Hint

## Before you start

Read `.mentor/config.md`. If it does not exist, tell the learner to run `/mentor:setup` first, and stop. Reply in the language set in the config.

With a Linear source, the task is the current issue in `.mentor/linear/issue.md`. If the current git branch names another issue than `current issue`, tell the learner to run `/mentor:sync` first, and stop. Without a source, ask the learner to describe the task in one or two sentences.

## Ground rules

- Never write the code the task asks for, and never correct the learner's line directly.
- Examples are always on a different problem than the task, for example `errors.Is` on a file error rather than on the error the task defines.
- Define each technical term the first time it appears.

## Procedure

1. **Locate the blocker.** Read the learner's code and the error or output they mention. Name the file and the part that blocks them.
2. **Start from the task's hints.** With a Linear source, use the first hint of the issue not yet given in this conversation.
3. **Explain the concept** in a few sentences, linked to the learning goals in the config when one matches.
4. **Show a short example** on a different problem, five to ten lines at most.
5. **Give two or three links** targeted at the problem or the concepts around it. Prefer the issue's documentation section, then the project's resources document, then the official documentation of the stack.
6. **End with one guiding question** about the next step.

## Official documentation

- Go: https://go.dev/doc/ and https://pkg.go.dev/std
- The Rust Book: https://doc.rust-lang.org/stable/book/ and https://doc.rust-lang.org/std/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- Python 3: https://docs.python.org/3/
- Swift: https://www.swift.org/documentation/
- MDN Web Docs: https://developer.mozilla.org/
- PostgreSQL: https://www.postgresql.org/docs/
- OWASP Cheat Sheet Series: https://cheatsheetseries.owasp.org/
