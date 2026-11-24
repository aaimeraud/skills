---
name: "study-setup"
description: "One-time setup for the homework plugin: protects the work folder in git, finds the student's brief in the folder or in a Linear project, and saves their language, subject, criteria, resources and mode. Use when the student runs setup, or when no homework config exists yet."
---

# Study setup

Run this procedure when there is no config at `.homework/config.md`, or when the student runs `/homework:study-setup`. Ask everything in one message, so the student answers once.

## Step 1: protect the folder from git

Before creating anything, make sure `.gitignore` contains the line `.homework/`:

- If `.gitignore` exists and lacks the line, append it.
- If there is no `.gitignore` and the folder is a git repository, create `.gitignore` with that line.
- If the folder is not a git repository, do nothing and say so.

Do this first, so the folder can never be committed by mistake.

## Step 2: find the brief

Look in the current folder for a `README.md`, or a `.txt` or `.md` file that holds the exercises. If exactly one is a clear candidate, use it and say which. The brief is read where it is: never copy it and never create a folder for it.

If there are several candidates, ask for the path. If there is none, offer three choices in the step 3 message:

1. **Add files.** The student gives the brief or course material, converted with `/homework:brief-extract`.
2. **Use a Linear project.** Only when Linear tools are available in the session. List the Linear projects, propose the one whose name is closest to the folder or the repository, and let the student confirm it. If Linear tools are missing, say that the Linear connector must be connected first, and offer the other choices.
3. **No brief.** The student describes each task in their own words.

## Step 3: ask in one message

1. **Conversation language.** Always ask. Reply in any language the student chooses.
2. **Subject and level.** Propose what you inferred from the brief, the Linear project or the code (for example "Go, beginner"). The student confirms or corrects it here. Never ask again later.
3. **Review criteria.** The criteria in the brief are used by default (in a Linear issue, its success criteria). Ask whether the student wants to add or change any. This is optional.
4. **Resources.** Ask once whether the student has brought course material (PDFs, notes, links). With a Linear project, its documents count as resources. Never ask again in later commands.
5. **Brief source**, only if step 2 found no clear file: the three choices above.

## Step 4: save the config

Save the answers to `.homework/config.md`: language, subject and level, criteria, the list of resources, and:

- `source`: `local` (a brief file), `linear` (a Linear project) or `none`.
- `brief`: the brief path, or `.homework/linear/issue.md` for a Linear source.
- `linear project`: the project identifier (for example `P-ENG-12`), for a Linear source only.
- `mode`: `strict` for a local brief (school homework), `guide` for a Linear source or no brief (a personal project). The student may change it here.

Do not ask again unless the student runs `/homework:study-setup` again.

If the student brought resources, convert them with `/homework:brief-extract` and list them in the config. For a Linear source, run `/homework:linear-sync` next to fetch the current issue and the project documents.

## Ground rules

- Never give the answer, the final code, or the correct result.
- Define any term a beginner might not know.
- Read Linear only. Nothing is written to Linear during setup.
