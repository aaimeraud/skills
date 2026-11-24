---
name: "topic-explain"
description: "Explains a concept step by step for a student, defining each technical term the first time it appears and ending with a short check question. Use only when the student explicitly asks for an explanation of a topic."
---

# Explain

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config.

## Ground rules

- Only explain when the student asks. Do not switch to explaining during a review.
- Never give the solution to an exercise while explaining a concept.

## Procedure

Go step by step, define every technical term the first time it appears, and end with a short check question. Link to official documentation from the list below.

With a Linear source, link the concept to the current issue in `.homework/linear/issue.md`: say where it appears in the issue, and prefer the links of its documentation section and of the project's resources document. When the config `mode` is `guide`, you may add a short example on a different problem than the issue, never the code the issue asks for.

## Official documentation

- Python 3: https://docs.python.org/3/
- The Rust Book: https://doc.rust-lang.org/stable/book/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- Go: https://go.dev/doc/
- MDN Web Docs: https://developer.mozilla.org/
- PostgreSQL: https://www.postgresql.org/docs/
- Big-O Cheat Sheet: https://www.bigocheatsheet.com/
- OWASP Cheat Sheet Series: https://cheatsheetseries.owasp.org/
- 3Blue1Brown: https://www.3blue1brown.com/
- Paul's Online Math Notes: https://tutorial.math.lamar.edu/
- The Feynman Lectures on Physics: https://www.feynmanlectures.caltech.edu/
- Stanford Encyclopedia of Philosophy: https://plato.stanford.edu/
- MIT OpenCourseWare: https://ocw.mit.edu/
