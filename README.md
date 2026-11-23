# Skills

 A collection of agent skills, organised by topic and use case. Each topic is an installable plugin, so you only install what you need.  
  
[![skills.sh](https://skills.sh/b/aaimeraud/skills)](https://skills.sh/aaimeraud/skills)

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

### education: homework

Reviews exercises with a score out of 5, checks answers without revealing them, and gives hints with official documentation links. Run the setup once, then use the commands below.

| Command | What it does |
| --- | --- |
| `/homework:study-setup` | One-time setup: language, subject, criteria and resources. |
| `/homework:exercise-review <exercise>` | Status, score out of 5, and up to three guiding problems. |
| `/homework:exercise-review-all` | One line per exercise in the brief. |
| `/homework:answer-check <answer>` | Says whether an answer is right, without revealing it. |
| `/homework:exercise-hint <exercise>` | A four-step hint with documentation links. |
| `/homework:topic-explain <topic>` | A step-by-step explanation, only when you ask for one. |
| `/homework:topic-resources <topic>` | Free documentation for a topic. |
| `/homework:brief-extract <file>` | Converts a PDF, image or docx brief into markdown. |

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## License

Distributed under the [MIT License](./LICENSE).
