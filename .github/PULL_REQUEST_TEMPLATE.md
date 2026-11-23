<!--
  Before opening a pull request:
  - Use a Conventional Commit title: type(scope): imperative summary, 72 characters max
    (scope = the topic, for example education).
  - Keep the change focused on one skill or one topic.
  - Test the skill with a real agent, not only by reading it.
  - Remove secrets, personal data and private exercise content from the diff and logs.
-->

## Summary

<!-- What does this change do? Keep this section concise. -->

## Motivation and context

<!-- Why is this change needed? Link related issues with "Closes #123" when applicable. -->

Closes #

## Changes

- 

## Affected skill or topic

<!-- For example: skills/education/homework/review, or "new topic: skills/<topic>". -->

## Validation

- [ ] `SKILL.md` has `name` (matching the folder) and `description` in its frontmatter
- [ ] The skill is listed in its topic's `plugin.json` and `README.md`
- [ ] For a new topic: it is added to `.claude-plugin/marketplace.json` and the root `README.md`
- [ ] Both JSON files still parse
- [ ] I ran the skill with a real agent and noted the result below

<!-- Describe the test run (agent, prompt, outcome). Write "N/A" with a reason if not applicable. -->

## Screenshots or recordings

<!--
  Only for changes that alter what the user sees in the agent's output.
  Delete this section when it does not apply.
-->

## Breaking changes

<!-- Describe migration steps, changed commands, or compatibility concerns. Write "None" otherwise. -->

None

## Review checklist

- [ ] The change follows [CONTRIBUTING.md](../CONTRIBUTING.md).
- [ ] The change is limited to the stated scope.
- [ ] For education skills: the skill still guides instead of giving answers.
- [ ] No credentials, personal data or private material are included.
