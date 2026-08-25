# Repository Guidelines

## Scope

This repository maintains reusable agent skills. Skill sources live in `skills/`; each `skills/<skill-name>/SKILL.md` is that skill's canonical entrypoint. Packaged platform skills live in `skills/.system/` and are maintained separately from the personal skill catalog.

Read `README.md` when adding, removing, or renaming a skill; its catalog is the user-facing index that must match the top-level skill directories.

## Skill Layout

Keep each skill self-contained:

- `SKILL.md`: YAML front matter and executable instructions.
- `scripts/`: deterministic helpers.
- `references/`: material loaded only for the branches named by pointers in `SKILL.md`.
- `assets/`: reusable templates or media.
- `agents/`: agent-specific integration metadata.

Use only the directories a skill needs. Put shared behavior in one canonical location and point to it instead of copying instructions between files.

## Writing Skills

Follow `skills/writing-for-agents/SKILL.md` whenever creating or editing agent-consumed instructions, including `SKILL.md` and this file. Follow `skills/writing-for-agents/SKILL-MECHANICS.md` for skill front matter, invocation policy, and router skills.

Use lowercase `name` values and kebab-case directories, such as `skills/research-paper-writing/`. Write short imperative steps with checkable completion criteria. Keep definitions, rules, and caveats for one concept together. Move branch-specific reference material behind explicit pointers whose wording states when to read it.

Skills that only users should invoke, including aliases and workflow orchestrators, set `disable-model-invocation: true` in front matter.

Shell helpers use Bash with `set -euo pipefail`. Name shell tests `test-*.sh` and JavaScript tests `*.test.js`. Preserve ASCII unless the skill or source material requires another language.

## Documentation Sync

After every meaningful change, update the affected source of truth in the same patch:

- User-visible skill additions, removals, names, purposes, setup, or usage: update `README.md`.
- Contributor workflows, architecture, commands, or conventions: update `AGENTS.md`.
- Changes affecting both audiences: update both files.

`CLAUDE.md` is a symlink to `AGENTS.md`; edit only `AGENTS.md`.

## Validation

There is no repository-wide build. Validate the changed skill's relevant surface and finish only when all applicable checks pass:

1. Run `find skills -maxdepth 2 -name SKILL.md | sort` and confirm every intended personal skill entrypoint appears once.
2. Check edited front matter and every local pointer or referenced path.
3. Exercise the expected invocation plus adversarial or ambiguous prompts when behavior changed.
4. Run focused tests for edited scripts; keep outputs deterministic and record the commands used.
5. Compare top-level personal skill directories with the `README.md` catalog after adding, removing, or renaming a skill.

## Commits and Pull Requests

Use Conventional Commits, for example `docs(skills): clarify trigger wording`. Keep each commit and pull request scoped to one problem. Pull requests describe the problem and alternatives, list the validation environment and evidence, and record human review.
