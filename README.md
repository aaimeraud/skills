# Skills

A collection of agent skills, organised by topic and use case. Each topic is an installable plugin, so you only install what you need.

## Topics

| Topic | Plugin | What it covers |
| --- | --- | --- |
| [education](./skills/education/) | `education-skills` | Studying: reviewing homework and exercises without giving away the answers. |

New topics are added as folders under [`skills/`](./skills/). See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the layout.

## Installation

### Claude Code (recommended)

Add this repository as a marketplace, then install the plugin for the topic you want:

```shell
/plugin marketplace add aaimeraud/skills
/plugin install education-skills@aaimeraud-skills
```

### Manual

Copy the skill folder you need (for example `skills/education/homework-reviewer/`) into your agent's skills directory, such as `~/.claude/skills/`.

## Repository layout

```text
.claude-plugin/
  marketplace.json          # Lists one installable plugin per topic
skills/
  <topic>/                  # One folder per topic or use case
    .claude-plugin/
      plugin.json           # Plugin manifest: lists the topic's skills
    README.md               # Index of the topic's skills
    <skill-name>/
      SKILL.md              # The skill itself
```

## Skills

- **education**
  - [homework-reviewer](./skills/education/homework-reviewer/SKILL.md): Reviews exercises with a score out of 5, checks answers without revealing them, and gives hints with official documentation links.

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## License

No license has been chosen yet. Until one is added, all rights are reserved by the author.
