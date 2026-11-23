# Skills

A collection of agent skills, organised by topic and use case. Each topic is an installable plugin, so you only install what you need.

## Topics

| Topic | Plugin | What it covers |
| --- | --- | --- |
| [education](./skills/education/) | `homework` | Studying: reviewing homework and exercises without giving away the answers. |

Each topic folder holds one plugin per use case. New topics are added under [`skills/`](./skills/). See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the layout.

## Installation

### Claude Code (recommended)

Add this repository as a marketplace, then install the plugin for the topic you want:

```shell
/plugin marketplace add aaimeraud/skills
/plugin install homework@aaimeraud-skills
```

### Manual

Copy the skill folders you need (for example `skills/education/homework/`, which contains `shared/` and one folder per command) into your agent's skills directory, such as `~/.claude/skills/`.

## Repository layout

```text
.claude-plugin/
  marketplace.json          # Lists one installable plugin per topic
skills/
  <topic>/                  # One folder per topic or use case
    README.md               # Index of the topic's plugins
    <use-case>/             # One plugin per use case
      .claude-plugin/
        plugin.json         # Plugin manifest: lists the plugin's skills
      shared/               # Rules and reference files shared by the skills
      <skill-name>/
        SKILL.md            # One skill, invoked as /<use-case>:<skill-name>
```

## Skills

- **education / homework**: `setup`, `review`, `review-all`, `check`, `hint`, `explain`, `resources`, `extract`. Reviews exercises with a score out of 5, checks answers without revealing them, and gives hints with official documentation links. Invoked as `/homework:<skill>`.

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## License

Distributed under the [MIT License](./LICENSE).
