---
name: "plan-to-project"
description: "Turns a planning discussion into a Linear project with milestones, documents and issues, written in a neutral tone that any teammate can read. Use when the user asks to create a Linear project or to turn a plan into Linear issues."
---

# Plan to Linear project

## Ground rules

- Write for any future teammate, not for the person in the conversation. Use a neutral, impersonal tone: imperative for instructions ("Define the interface"), third person for descriptions ("The command validates the name"). Never use "you", "we", "I", "tu" or "je".
- Name roles, not people ("the maintainer", "the contributor", "the agent account"). A real handle appears only inside code, a command or a config value.
- Use short sentences and one term per concept. Define each technical term once.
- Refer to other work by issue identifier (for example `PROJ-123`), never by a task number. Order work with milestones and "blocked by" relations, not with number prefixes in titles.
- Never mention Claude, an AI assistant or the planning conversation in any Linear text.
- Do not create anything in Linear before the user approves the outline (step 4).

## Procedure

1. **Ask the language** of the Linear content (for example English or French), even when the conversation is in one language. Write everything in that language.
2. **Choose the mode.** Use the learning variant only when the user asks for it, for example with "learning mode", "homework", "apprentissage" or "devoir maison", or in their own words. Otherwise use the standard variant. Ask whether AI agents will work on the project, unless the user already said so; the answer decides whether issues get Agent notes.
3. **Collect the plan** from the discussion: goal, scope, decisions, phases, tasks and their dependencies. Ask one precise question when something blocks the outline. Check the team with the Linear tools and look for an existing project or issue with the same subject to avoid duplicates.
4. **Present the outline and wait for approval.** Show the project summary, the milestones, and the issue titles under each milestone with their dependencies. Create nothing yet.
5. **Create in Linear**, in this order: project, milestones, documents, issues (with milestone, labels, estimate and "blocked by" relations). Check each tool's parameters before calling it.
6. **Check the result.** Re-read the project and the issues. Confirm the tone rules, the links and the relations, then give the user the project link and a short summary.

## Project

- **Summary field:** one sentence saying what it is and for whom.
- **Description**, about 25 lines, in this order: Context and goal, Scope (in and out), Key decisions, Milestones (one line each, no task counts), Working conventions (branch, pull request, definition of done), Links to the documents.
- **Documents:** a "Spec" for detailed behavior and constraints, a "Resources" for reference links. A personal "Journal" is optional and may use the first person.

## Milestone

- Name: the outcome (for example "Phase 2 · Interactive interface").
- Description: one sentence on the outcome and one exit criterion.
- Set a target date on every milestone or on none of them.

## Issue

- One issue is one branch and one pull request, doable in about one session or one day. Keep it to 400 words or fewer. If it needs more, split it or move the material into a document.
- Title: an imperative verb phrase, no number prefix (for example "Add the `export` command").
- Use a sub-issue only for a part that is checkable on its own and takes more than one session. Smaller items become checkboxes in the acceptance criteria.
- Labels: a real type (Feature, Improvement, Bug), not a generic "Task". Set an estimate. Leave priority empty unless the user gave one.
- Agent notes are optional. Write them only when the user confirmed that AI agents will work on the project and an issue has detail specific to an agent. Never write them in the learning variant, or when the user wants to code by hand. In that case leave no empty block and no mention of agents in any description. When they apply, the detail goes in a collapsible block at the end:

```markdown
+++ Agent notes

Details for agents.

+++
```

### Standard variant

```markdown
## Context
1–3 sentences: why this issue exists.

## Goal
The observable result once the issue is done.

## Scope
* In: …
* Out: …

## Steps
1. … (only when the order matters, 3 to 7 steps)

## Acceptance criteria
- [ ] Verifiable by a command or an observation (3 to 6 items)

## References
* Official documentation links
```

### Learning variant

The contributor writes the code. Never include solution code.

```markdown
## Objective
## Concepts          (definitions only, 6 bullets at most)
## Requirements      (behavior, scope and limits; never inside Concepts)
## Steps             (4 to 7)
## Success criteria  (3 to 6 checkboxes, each checkable with a command)
## Hints             (2 to 3 guiding questions)
## Documentation     (official links only)
```

Add to the project description a "How to work" section: read Concepts first, try alone, check the success criteria, read the Hints before asking for help, one issue per branch and pull request.

## Documentation

- Linear docs: https://linear.app/docs
