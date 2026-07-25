# Repository Guidelines

## Project Structure & Module Organization

This repository is centered on `skills/`. Each skill lives in `skills/<skill-name>/` and should treat `SKILL.md` as the canonical entrypoint. Keep supporting material close to the skill: use `scripts/` for helpers, `references/` for source material, and `assets/` for reusable templates or media. System-level packaged skills live under `skills/.system/`.

## Documentation Update Policy

Keep documentation in sync with the repository after every meaningful change.

- Update `README.md` for user-facing changes such as features, setup steps, or usage instructions.
- Update `AGENTS.md` for contributor-facing changes such as architecture, commands, workflows, or internal conventions.
- If a change affects both audiences, update both files in the same patch.

## Build, Test, and Development Commands

There is no single repository-wide build step. Work at the skill level and validate only the relevant surface:

- `find skills -maxdepth 2 -name SKILL.md | sort` lists installed skills and confirms layout.

## Coding Style & Naming Conventions

Write skills in Markdown with YAML front matter. Keep `name` lowercase and directory names in kebab-case, for example `skills/use-x-chat/`. Use short, imperative instructions and keep examples concrete. Preserve ASCII by default unless the skill already requires another language. Shell helpers should be Bash with `set -euo pipefail`. Test scripts should follow `test-*.sh`; JavaScript tests should end in `*.test.js`.

## Testing Guidelines

When editing a skill, verify both the expected path and adversarial or ambiguous prompts. Prefer focused tests over broad rewrites, and keep outputs deterministic so failures are easy to review.

## Commit & Pull Request Guidelines

Use Conventional Commits such as `docs(skills): clarify trigger wording`. Keep each PR scoped to one problem. Describe the problem, explain alternatives considered, record the environment tested, include evaluation evidence, and confirm human review before submission.
