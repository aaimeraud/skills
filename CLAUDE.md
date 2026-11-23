# CLAUDE.md

Agent skills organised by topic and use case, each use case installable as a Claude Code plugin. The repository is meant to grow, so keep every addition in the same shape.

## Layout

```text
.claude-plugin/marketplace.json   # One entry per plugin (per use case)
skills/<topic>/                   # Topic, for example education
  README.md                       # Index of the topic's plugins
  <use-case>/                     # Plugin, for example homework
    .claude-plugin/plugin.json    # Lists the plugin's skills
    <skill>/SKILL.md              # One skill, invoked as /<use-case>:<skill>
```

- A skill's folder name is its command name, so `name` in its frontmatter must match the folder.
- Each skill must be self-contained. The skills.sh installer copies only the skill's own folder, so a `SKILL.md` must not link to files outside it. Repeat the short rules it needs in its own file.
- Keep each `SKILL.md` short. Put long reference material in the one skill that needs it.

## Adding a skill

1. Create `skills/<topic>/<use-case>/<skill>/SKILL.md` with `name` and `description` in the frontmatter.
2. Add `./<skill>` to the plugin's `.claude-plugin/plugin.json`.
3. List the skill in the topic's `README.md` and in the table in the root `README.md`.
4. Add an entry under `[Unreleased]` in `CHANGELOG.md`.
5. Run `claude plugin validate . --strict` and `claude plugin validate skills/<topic>/<use-case> --strict`.

## Adding a plugin (use case)

Do the same as for a skill, plus: add one entry to `.claude-plugin/marketplace.json` (`name`, `source` as `./skills/<topic>/<use-case>`, `description`, `category`, `keywords`), and list the plugin in the topic's `README.md`.

## Changelog

`CHANGELOG.md` follows Keep a Changelog. Every change that touches a skill, a plugin manifest, or the marketplace adds a line under `[Unreleased]`, in the matching section (`Added`, `Changed`, `Fixed`, `Removed`). Write what the user will notice, not the file list.

Versions are per plugin in `plugin.json`. Bump a plugin's version and move its `[Unreleased]` entries under a dated release heading only when releasing it. Do not bump versions in ordinary changes.

## Education skills (`homework`)

- The skills guide the student and never give the answer, the final code, or the correct result. Each skill repeats the ground rules it needs.
- The `.homework/` folder is the student's private working folder. Setup adds it to `.gitignore`. Never commit student material, briefs or answers to this repository.
- Commands are invoked as `/homework:<skill>`, so a skill called `homework` would be a different command.

## Documentation links

Only link official documentation or well-known free resources, and check each link before adding it. Each skill keeps its own short list of links. The full catalogue is in `skills/education/homework/topic-resources/SKILL.md`.

## Git

- Use GitButler (`but`) for commits and branches, as set in the user's global instructions. Do not commit to `main`. Use `type/short-description` branch names.
- Commit titles use Conventional Commits with the topic as scope where it applies, for example `feat(education): ...`.
- Open pull requests as drafts with the agent GitHub account, following `.github/PULL_REQUEST_TEMPLATE.md`. Never merge a pull request.
- Prose, skill text, commit messages and pull requests are in English.
- Do not commit secrets, `.env` files, or the `.homework/` folder.
