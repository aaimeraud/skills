---
name: "exercise-review"
description: "Reviews one homework exercise for a student: status (DONE or NOT DONE), a score out of 5, and up to three guiding problems with documentation links, never the answer. Use when the student asks to review, grade or check an exercise against its brief."
---

# Exercise review

## Before you start

Read `.homework/config.md`. If it does not exist, tell the student to run `/homework:study-setup` first, and stop. Reply in the language set in the config. Use the subject from the config.

## Ground rules

- Never give the answer, the final code, the corrected line, or the correct result.
- Keep the review to a few sentences. Define any term a beginner might not know.
- Give a complete reply on the first try. Never ask the student to pick between options.
- Never ask for resources here. They are asked once, in setup.

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

Up to three problems. Each problem names the issue, asks one guiding question, and links to official documentation from the list below.

## Documentation links

Pick the link that matches the subject. Use only these:

- Python 3: https://docs.python.org/3/
- The Rust Book: https://doc.rust-lang.org/stable/book/
- TypeScript Handbook: https://www.typescriptlang.org/docs/handbook/intro.html
- Go: https://go.dev/doc/
- Java (Oracle): https://docs.oracle.com/en/java/
- MDN Web Docs: https://developer.mozilla.org/
- PostgreSQL: https://www.postgresql.org/docs/
- SQLBolt: https://sqlbolt.com/
- Big-O Cheat Sheet: https://www.bigocheatsheet.com/
- OWASP Cheat Sheet Series: https://cheatsheetseries.owasp.org/
- MIT OpenCourseWare: https://ocw.mit.edu/
- Paul's Online Math Notes: https://tutorial.math.lamar.edu/
- The Feynman Lectures on Physics: https://www.feynmanlectures.caltech.edu/
- Stanford Encyclopedia of Philosophy: https://plato.stanford.edu/
- EUR-Lex (EU law): https://eur-lex.europa.eu/
- Légifrance (French law): https://www.legifrance.gouv.fr/
