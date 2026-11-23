# Setup

Run this procedure when there is no config at `.homework/config.md`, or when the student runs `/homework:study-setup`. It is the only time the skills ask about the work setup, so ask everything in one message.

## Step 1: protect the folder from git

Before creating anything, make sure `.gitignore` contains the line `.homework/`:

- If `.gitignore` exists and lacks the line, append it.
- If there is no `.gitignore` and the folder is a git repository, create `.gitignore` with that line.
- If the folder is not a git repository, do nothing and say so.

Do this first, so the folder can never be committed by mistake.

## Step 2: find the brief

Look in the current folder for a `README.md`, or a `.txt` or `.md` file that holds the exercises. If exactly one is a clear candidate, use it and say which. If there are several or none, ask for its path. The brief is read where it is: never copy it and never create a folder for it.

## Step 3: ask in one message

Ask only these questions:

1. **Conversation language.** Always ask. Reply in any language the student chooses.
2. **Subject and level.** Propose what you inferred from the brief (for example "Python, beginner"). The student confirms or corrects it here. Never ask again later.
3. **Review criteria.** The criteria in the brief are used by default. Ask whether the student wants to add or change any. This is optional.
4. **Resources.** Ask once whether the student has brought course material (PDFs, notes, links). Never ask again during later commands.
5. **Brief path**, only if step 2 found no clear file.

## Step 4: save the config

Save the answers to `.homework/config.md`: language, subject and level, brief path, criteria, and the list of resources. Do not ask again unless the student runs `/homework:study-setup` again.
