# Contributing

Thanks for helping grow this collection. The repository is meant to scale, so the rules below keep every skill easy to find, install and maintain.

## Adding a skill

1. Pick the plugin folder `skills/<topic>/<use-case>/` that fits. If none fits, create a new plugin for the use case (see below).
2. Create a folder named after the skill, in lowercase kebab-case, directly under the plugin: `skills/<topic>/<use-case>/<skill-name>/`. Its command is `/<use-case>:<skill-name>`.
   - Make the skill self-contained. Installers copy only the skill's own folder, so repeat any short rules it needs inside its `SKILL.md`, and do not link to files outside it.
3. Add a `SKILL.md` file with frontmatter:

   ```markdown
   ---
   name: "skill-name"
   description: "One or two sentences: what the skill does and when to use it."
   ---
   ```

   The `name` must match the folder name. The `description` is what the agent reads to decide when to use the skill, so make it specific.
4. Add the skill to the plugin's `.claude-plugin/plugin.json` (in the `skills` list, as `./<skill-name>`) and to the topic's `README.md`.
5. Add the skill to the table of skills in the root [`README.md`](./README.md).

## Adding a use case (plugin)

1. Create `skills/<topic>/<use-case>/` with a `.claude-plugin/plugin.json`, with `"version": "0.0.0"`.
2. Add the plugin to the topic's `README.md`.
3. Add one entry to [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) with `name`, `source` (`./skills/<topic>/<use-case>`), `description`, `category` and `keywords`.
4. Add the plugin as a package in [`release-please-config.json`](./release-please-config.json) and to [`.release-please-manifest.json`](./.release-please-manifest.json) with the version `0.0.0`.
5. Add the plugin to the table at the top of the root `README.md`.

One plugin equals one use case. Its skills share a command prefix, so `/<use-case>:<skill-name>`.

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

Keep titles short, specific and in the imperative mood, for example `feat(education): add the review skill to homework`.

## Pull requests

- Pull requests are squash-merged. The PR title becomes the commit that drives releases, so it must be a Conventional Commit title.
- Keep each pull request focused on one skill or one topic.
- Describe what the skill does, how you tested it (for example, by running it on a real exercise), and any change in behaviour.
- Use the repository [pull request template](./.github/PULL_REQUEST_TEMPLATE.md).

## Releases

Releases are automatic. After a pull request is merged into `main`, release-please opens a release PR with the changelog and the new version for each changed plugin. Merging that release PR publishes the tag and the GitHub Release. Maintainers merge the release PR, and nothing is released without that step.

## Reporting bugs and requesting features

Use the issue forms in [`.github/ISSUE_TEMPLATE/`](./.github/ISSUE_TEMPLATE/): a bug report for a skill that misbehaves, or an idea for a new skill, topic or change.

## License

By contributing, you agree that your changes are released under the [MIT License](./LICENSE).
