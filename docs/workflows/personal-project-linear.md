# Personal project with Linear

Use this workflow to learn a language by building a real project, with the plan in Linear and the agent as a guide. The example builds a to-do CLI in Go.

The two plugins share the work: `linear` writes the plan once, and `homework` reads it at every session. The agent then knows the project, the current task and the related documents without being told.

## Commands

```mermaid
flowchart TD
    A["/linear:plan-to-project<br/>learning variant"] --> B["/homework:study-setup<br/>source: Linear"]
    B --> C["git branch from the issue"]
    C --> D["/homework:linear-sync"]
    D --> E["code, then /homework:exercise-hint"]
    E --> F["/homework:exercise-review"]
    F -->|"NOT DONE"| E
    F -->|"DONE"| G["/homework:journal"]
    G --> H["pull request, next issue"]
    H --> C
```

1. **Plan once.** Describe the project, then run `/linear:plan-to-project` and ask for the learning variant. The agent shows the outline and creates nothing before approval. Each issue gets Objective, Concepts, Requirements, Steps, Success criteria, Hints and Documentation, plus Spec, Resources and Journal documents for the project.
2. **Set up homework once.** In the project's repository, run `/homework:study-setup`. The folder has no brief, so choose "Use a Linear project" and confirm the project. The mode is `guide`.
3. **Start an issue.** Create the branch Linear suggests for it, for example `user/eng-12-add-the-list-command`.
4. **Sync.** `/homework:linear-sync` reads `ENG-12` from the branch name and copies the issue, its milestone and the project documents into `.homework/linear/`.
5. **Work and ask.** Code, then use `/homework:exercise-hint` when stuck. The first hints come from the issue itself.
6. **Review.** `/homework:exercise-review` runs the success criteria that only check (tests, build, `grep`) and gives DONE or NOT DONE.
7. **Log the session.** `/homework:journal` drafts a dated entry. It is appended to the Linear Journal only after approval.
8. **Next issue.** Open the pull request, create the next branch, and run `/homework:linear-sync` again.

## Sample exchange

> **Learner:** /homework:exercise-hint
>
> **Agent:** The current issue is `ENG-12`, "Add the `list` command". In `cmd/list.go`, the error from `os.ReadFile` is printed, then the function keeps going with an empty slice.
>
> The concept is *error wrapping*: adding context to an error while keeping the original one. For example, on a different problem:
>
> ```go
> if err != nil {
>     return fmt.Errorf("open settings: %w", err)
> }
> ```
>
> - Errors in Go 1.13+: https://go.dev/blog/go1.13-errors
> - Package `errors`: https://pkg.go.dev/errors
>
> What should `list` return to its caller when the file cannot be read?

> **Learner:** /homework:journal
>
> **Agent:** Draft entry for today, `ENG-12`. Progress: `list` reads the file and prints the tasks. Decisions: errors are wrapped and handled in `main`. Difficulties: the error was swallowed, solved by returning it. Next: `ENG-13`. Append it to the Journal as is, change it, or drop it?

## What the agent does not do

- Write the code the issue asks for, or correct the learner's line, even in guide mode. Examples are always on another problem.
- Write to Linear, except the journal entry after approval.
- Run a criterion that creates, deletes or publishes something without asking first.
