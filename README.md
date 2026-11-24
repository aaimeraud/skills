# Skills

 A collection of agent skills, organised by topic and use case. Each topic is an installable plugin, so you only install what you need.  
  
[![skills.sh](https://skills.sh/b/aaimeraud/skills)](https://skills.sh/aaimeraud/skills)

## Topics

| Topic | Plugin | What it covers |
| --- | --- | --- |
| [education](./skills/education/) | `homework` | Studying: reviewing homework and exercises without giving away the answers. |
| [education](./skills/education/) | `mentor` | Learning by building: a mentor for personal coding projects, with the task read from Linear. |
| [project-management](./skills/project-management/) | `linear` | Planning: turning a discussion into a Linear project, milestones and issues. |

Each topic folder holds one plugin per use case. New topics are added under [`skills/`](./skills/). See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the layout.

To see the skills in use, read the [example workflows](./docs/workflows/): homework with a local or PDF brief, a personal project with the mentor and Linear, and team project planning.

## Installation

### Claude Code (recommended)

Add this repository as a marketplace, then install the plugin for the topic you want:

```shell
/plugin marketplace add aaimeraud/skills
/plugin install homework@aaimeraud-skills
```

### Other agents (skills.sh)

Requires Node.js 22.20 or later. Install every skill in the collection at once:

```shell
npx skills add aaimeraud/skills --all
```

### Manual

Copy the skill folders you need (for example `skills/education/homework/study-setup/`) into your agent's skills directory, such as `~/.claude/skills/`.

## Repository layout

```text
.claude-plugin/
  marketplace.json          # Lists one installable plugin per use case
.github/workflows/
  release-please.yml        # Opens release PRs and publishes releases
release-please-config.json  # Release packages, one per plugin
docs/workflows/             # Example workflows that show the skills in use
skills/
  <topic>/                  # One folder per topic
    README.md               # Index of the topic's plugins
    <use-case>/             # One plugin per use case
      .claude-plugin/
        plugin.json         # Plugin manifest: lists the plugin's skills
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

### education: mentor

A mentor for personal coding projects. It reads the code and the current task (optionally from a Linear project), explains the concepts behind a blocker with examples on other problems, and reviews the work against its success criteria. No grade, and never the task's code.

| Command | What it does |
| --- | --- |
| `/mentor:setup` | One-time setup: language, stack, level, goals and an optional Linear project. |
| `/mentor:sync [issue]` | Copies the current Linear issue, found from the git branch, and the project documents. |
| `/mentor:hint` | Explains the concept behind a blocker, with an example on a different problem. |
| `/mentor:review` | Checks each success criterion and names the concepts to deepen. |
| `/mentor:explain <concept>` | A step-by-step explanation linked to the project, with free resources. |
| `/mentor:journal` | Drafts a dated journal entry, then appends it to the Linear Journal after approval. |

### project-management: linear

Creates a Linear project from a planning discussion, with milestones, documents and issues written in a neutral tone that any teammate can read.

| Command | What it does |
| --- | --- |
| `/linear:plan-to-project` | Drafts the outline in the conversation language, then creates the project, milestones, documents and issues after approval. |

## Releases

Each plugin is versioned and released on its own. After a change is merged into `main`, release-please opens a release PR with the changelog and the new version. Merging that PR creates the tag and the GitHub Release. The changelog for each plugin is in its folder, for example [`skills/education/homework/CHANGELOG.md`](./skills/education/homework/CHANGELOG.md), once the first release is out.

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## License

Distributed under the [MIT License](./LICENSE).
