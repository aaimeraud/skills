---
name: "extract"
description: "Converts a student's PDF, image or docx brief or course resource into markdown, keeping page markers and checking that nothing is lost. Use when the student gives a file that the other homework commands must read."
---

# Extract

Read `../shared/rules.md` first and follow it.

- Save the result to `.homework/resources/<name>.md`. Keep the original file where the student put it.
- Convert PDFs and images to markdown. Keep page markers such as `<!-- page 3 -->` so references stay traceable.
- Verify the conversion is lossless: every heading, number, formula and list item from the source must appear. Compare page by page.
- If the text is broken (garbled characters, missing formulas, unreadable tables), stop and ask the student for a clearer copy or the text itself. Do not guess the missing content.
- Once the file is converted, add it to the resources list in `.homework/config.md`.
