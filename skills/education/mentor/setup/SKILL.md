---
name: "setup"
description: "One-time setup for the mentor plugin on a personal coding project: protects the work folder in git, saves the learner's language, stack, level and goals, and links an optional Linear project. Use when the learner runs setup, or when no mentor config exists yet."
---

# Mentor setup

Run this procedure when there is no config at `.mentor/config.md`, or when the learner runs `/mentor:setup`. Ask everything in one message, so the learner answers once.

## Ground rules

- The mentor teaches concepts; the learner writes the project's code.
- Read Linear only. Nothing is written to Linear during setup.

## Step 1: protect the folder from git

Before creating anything, make sure `.gitignore` contains the line `.mentor/`:

- If `.gitignore` exists and lacks the line, append it.
- If there is no `.gitignore` and the folder is a git repository, create it with that line.
- If the folder is not a git repository, do nothing and say so.

## Step 2: read the project

Look at the repository: languages, build files (`go.mod`, `Cargo.toml`, `package.json`…), README and tests. Infer the stack and how to run the tests.

## Step 3: ask in one message

1. **Conversation language.** Always ask.
2. **Stack and level.** Propose what step 2 found (for example "Go, beginner; tests with `go test ./...`"). The learner confirms or corrects it.
3. **Learning goals.** What the learner wants to understand through this project (for example "error handling, testing, concurrency"). Optional.
4. **Task source.** Offer:
   - **A Linear project**, only when Linear tools are available. List the projects, propose the one whose name is closest to the repository, and let the learner confirm. If the tools are missing, say that the Linear connector must be connected first.
   - **None**: the learner describes each task in their own words.

## Step 4: save the config

Save the answers to `.mentor/config.md`: language, stack and level, test command, learning goals, `source` (`linear` or `none`) and, for Linear, `linear project` (the identifier, for example `P-ENG-12`).

For a Linear source, run `/mentor:sync` next.
