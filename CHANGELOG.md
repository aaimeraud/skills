# Changelog

All notable changes to this repository are documented here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/) per plugin.

## [Unreleased]

### Added

- Repository layout by topic and use case: `skills/<topic>/<use-case>/`, with one installable plugin per use case.
- `homework` plugin (topic `education`) with eight skills: `study-setup`, `exercise-review`, `exercise-review-all`, `answer-check`, `exercise-hint`, `topic-explain`, `topic-resources` and `brief-extract`. Shared rules, the setup procedure and the documentation catalogue live in its `shared/` folder.
- `.claude-plugin/marketplace.json` listing the plugins for Claude Code.
- MIT license.
- Issue forms (skill bug report, idea or feedback) and a pull request template adapted to skills.
- This changelog, `CLAUDE.md`, and `AGENTS.md`.

### Changed

- The `homework` skills keep the student's settings in `.homework/` and add that folder to `.gitignore` during setup, so it is never committed by mistake.
- Setup no longer creates a `homework/` folder or an `instructions.md`. It reads the brief where it already is.
