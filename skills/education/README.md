# Education

Skills for students and self-learners: reviewing exercises, checking answers, and getting hints without being handed the solution.

## Plugins

- **[homework](./homework/)**: the homework helper, for school work in any subject. Install it once, then use its commands:
  - `/homework:study-setup`: one-time setup (language, subject, criteria, resources).
  - `/homework:exercise-review <exercise>`: status, score out of 5, and guiding problems.
  - `/homework:exercise-review-all`: one line per exercise.
  - `/homework:answer-check <answer>`: is the answer right, without revealing it.
  - `/homework:exercise-hint <exercise>`: a four-step hint with documentation links.
  - `/homework:topic-explain <topic>`: a step-by-step explanation, only when asked.
  - `/homework:topic-resources <topic>`: free documentation for a topic.
  - `/homework:brief-extract <file>`: converts a PDF, image or docx into markdown.

  Examples: [homework with a local brief](../../docs/workflows/homework-local-brief.md), [homework from a PDF](../../docs/workflows/homework-pdf-brief.md).

- **[mentor](./mentor/)**: a mentor for personal coding projects. No grade: the goal is to understand the concepts behind the project. The current task can come from a Linear project, for example one made with `/linear:plan-to-project` in its learning variant.
  - `/mentor:setup`: one-time setup (language, stack, level, goals, optional Linear project).
  - `/mentor:sync [issue]`: copies the current Linear issue, found from the git branch, and the project documents.
  - `/mentor:hint`: reads the code, explains the concept behind the blocker, and shows an example on a different problem.
  - `/mentor:review`: checks each success criterion and names the concepts to deepen.
  - `/mentor:explain <concept>`: a step-by-step explanation linked to the project, with free resources.
  - `/mentor:journal`: drafts a dated journal entry and, after approval, appends it to the Linear Journal.

  Example: [personal project with Linear](../../docs/workflows/personal-project-linear.md).

Neither plugin writes the code or gives the answer: `homework` guides toward what the teacher wants to assess, `mentor` toward concepts the learner can reuse.
