# Contributing

Thanks for helping grow this collection. The repository is meant to scale, so the rules below keep every skill easy to find, install and maintain.

## Adding a skill

1. Pick the topic folder under `skills/` that fits the use case. If none fits, create a new topic (see below).
2. Create a folder named after the skill, in lowercase kebab-case: `skills/<topic>/<skill-name>/`.
3. Add a `SKILL.md` file with frontmatter:

   ```markdown
   ---
   name: "skill-name"
   description: "One or two sentences: what the skill does and when to use it."
   ---
   ```

   The `name` must match the folder name. The `description` is what the agent reads to decide when to use the skill, so make it specific.
4. Add the skill to the topic's `skills/<topic>/.claude-plugin/plugin.json` (in the `skills` list) and to the topic's `README.md`.
5. Add the skill to the table of skills in the root [`README.md`](./README.md).

## Adding a topic

1. Create `skills/<topic>/` with a `README.md` (a short index of its skills) and `.claude-plugin/plugin.json`.
2. Add one entry to [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) with `name`, `source` (`./skills/<topic>`), `description`, `category` and `keywords`.
3. Add the topic to the table at the top of the root `README.md`.

One topic equals one plugin. Keep a topic focused on one kind of user or use case; split it when it grows too broad.

## Skill guidelines

- **Guide, don't do the work for the user** when the skill is for learning. Explain the reasoning and ask guiding questions.
- **Keep it short.** Long reference material belongs in separate files next to `SKILL.md`, loaded only when needed.
- **Link to official documentation** rather than copying it.
- **No secrets, personal data or private material** in any file, example or documentation link.
- **Write the skill in English**, the same language as the repository.

## Commit messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

```text
<type>(<optional scope>): <imperative description>
```

Use the topic as the scope when a change belongs to one topic, for example `feat(education): add study-plan skill`.

| Type       | Use for                                |
| ---------- | -------------------------------------- |
| `feat`     | A new skill or a new user-facing capability |
| `fix`      | A bug fix                              |
| `docs`     | Documentation-only changes             |
| `refactor` | Restructuring without behaviour changes |
| `chore`    | Maintenance that does not affect users |

Keep titles short, specific and in the imperative mood, for example `feat(education): add homework-reviewer skill`.

## Pull requests

- Keep each pull request focused on one skill or one topic.
- Describe what the skill does, how you tested it (for example, by running it on a real exercise), and any change in behaviour.
- Use the repository [pull request template](./.github/PULL_REQUEST_TEMPLATE.md).

## Reporting bugs and requesting features

Use the issue forms in [`.github/ISSUE_TEMPLATE/`](./.github/ISSUE_TEMPLATE/): a bug report for a skill that misbehaves, or an idea for a new skill, topic or change.

## License

By contributing, you agree that your changes are released under the [MIT License](./LICENSE).
