# Education

Skills for students and self-learners: reviewing exercises, checking answers, and getting hints without being handed the solution.

## Plugins

- **[homework](./homework/)**: the homework helper. Install it once, then use its commands:
  - `/homework:study-setup`: one-time setup (language, subject, criteria, resources).
  - `/homework:exercise-review <exercise>`: status, score out of 5, and guiding problems.
  - `/homework:exercise-review-all`: one line per exercise.
  - `/homework:answer-check <answer>`: is the answer right, without revealing it.
  - `/homework:exercise-hint <exercise>`: a four-step hint with documentation links.
  - `/homework:topic-explain <topic>`: a step-by-step explanation, only when asked.
  - `/homework:topic-resources <topic>`: free documentation for a topic.
  - `/homework:brief-extract <file>`: converts a PDF, image or docx into markdown.
  - `/homework:linear-sync [issue]`: copies the current Linear issue and the project documents into the homework folder.
  - `/homework:journal`: drafts a dated journal entry and, after approval, appends it to the Linear Journal.

Examples: [homework with a local brief](../../docs/workflows/homework-local-brief.md), [homework from a PDF](../../docs/workflows/homework-pdf-brief.md), [personal project with Linear](../../docs/workflows/personal-project-linear.md).

With no brief in the folder, setup can use a Linear project instead, for example one made with `/linear:plan-to-project` in its learning variant. The current issue then becomes the exercise, and the commands switch to guide mode: they may explain concepts and show examples on other problems, but still never write the code the issue asks for.
