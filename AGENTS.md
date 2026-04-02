# Repository Guidelines

## Project Structure & Module Organization

This repository is centered on `skills/`. Each skill lives in `skills/<skill-name>/` and should treat `SKILL.md` as the canonical entrypoint. Keep supporting material close to the skill: use `scripts/` for helpers, `references/` for source material, and `assets/` for reusable templates or media. System-level packaged skills live under `skills/.system/`. The `superpowers/` directory is an upstream repository referenced here for integration and test harnesses; do not treat it as the primary place for new contribution work unless a change explicitly targets that dependency.

## 文档更新政策
**关键：每次代码更改后必须更新 README.md 和 AGENTS.md**

- 面向用户的更改（功能、设置、使用说明）→ 更新 `README.md`
- 开发相关的更改（架构、命令、工作流、内部系统）→ 更新 `AGENTS.md`
- 必须确保文档与代码库同步

## Build, Test, and Development Commands

There is no single repository-wide build step. Work at the skill level and validate only the relevant surface:

- `find skills -maxdepth 2 -name SKILL.md | sort` lists installed skills and confirms layout.
- `./superpowers/tests/skill-triggering/run-all.sh` runs prompt-trigger regression checks against the referenced Superpowers harness.
- `./superpowers/tests/claude-code/run-skill-tests.sh` runs Claude Code skill tests; add `--integration` for slower end-to-end coverage.
- `cd superpowers/tests/brainstorm-server && npm test` runs the small Node-based brainstorm server test.

## Coding Style & Naming Conventions

Write skills in Markdown with YAML front matter. Keep `name` lowercase and directory names in kebab-case, for example `skills/use-x-chat/`. Use short, imperative instructions and keep examples concrete. Preserve ASCII by default unless the skill already requires another language. Shell helpers should be Bash with `set -euo pipefail`. Test scripts should follow `test-*.sh`; JavaScript tests should end in `*.test.js`.

## Testing Guidelines

When editing a skill, verify both the expected path and adversarial or ambiguous prompts. Put prompt fixtures under the existing `superpowers/tests/**/prompts/` directories when extending harness coverage. Prefer focused tests over broad rewrites, and keep outputs deterministic so failures are easy to review.

## Commit & Pull Request Guidelines

This checkout currently has no local commit history on `main`, so follow the documented workflow rather than local precedent: use Conventional Commits such as `docs(skills): clarify trigger wording`. Keep each PR scoped to one problem. Mirror the upstream PR template expectations in `superpowers/.github/PULL_REQUEST_TEMPLATE.md`: describe the problem, explain alternatives considered, record environment tested, include evaluation evidence, and confirm human review before submission.
