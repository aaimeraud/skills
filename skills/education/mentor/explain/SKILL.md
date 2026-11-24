---
name: "explain"
description: "Explains a programming concept step by step in the context of the learner's project and current task, with an example on a different problem and a short list of free resources. Use when the learner asks what a concept means or where to learn more about it."
---

# Explain

## Before you start

Read `.mentor/config.md`. If it does not exist, tell the learner to run `/mentor:setup` first, and stop. Reply in the language set in the config. With a Linear source, read `.mentor/linear/issue.md` and the documents in `.mentor/linear/docs/`.

## Ground rules

- Never write the code the current task asks for. Examples are always on a different problem.
- Define each technical term the first time it appears.

## Procedure

1. **Explain step by step**, from what the learner already knows (their stack and level in the config) to the new idea.
2. **Link it to the project**: say where the concept appears in the current task or in the learner's code.
3. **Show a short example** on a different problem, in the learner's language.
4. **List two to four free resources**: first the issue's documentation section and the project's resources document, then the official documentation below. One line each, with why it is useful.
5. **End with a short check question.**

## Official documentation

- Go: https://go.dev/doc/ and A Tour of Go: https://go.dev/tour/
- The Rust Book: https://doc.rust-lang.org/stable/book/ and Rust by Example: https://doc.rust-lang.org/rust-by-example/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- Python 3: https://docs.python.org/3/
- Swift: https://www.swift.org/documentation/
- MDN Web Docs: https://developer.mozilla.org/
- Refactoring Guru (design patterns): https://refactoring.guru/design-patterns
- Martin Fowler: https://martinfowler.com/
- OWASP Cheat Sheet Series: https://cheatsheetseries.owasp.org/
- The Twelve-Factor App: https://12factor.net/
