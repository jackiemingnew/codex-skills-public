# Third-Party Skill Sources

Third-party skill bodies are not copied into this public catalog. Reinstall them
from source.

## Matt Pocock Skills

- Source: <https://github.com/mattpocock/skills>
- Purpose: engineering workflow skills, including TDD, bug diagnosis, PRD,
  issue splitting, triage, handoff, and architecture vocabulary.

```bash
npx skills@latest add mattpocock/skills -g -a codex --full-depth
```

## UI/UX Pro Max

- Source: <https://github.com/nextlevelbuilder/ui-ux-pro-max-skill>
- Purpose: searchable UI/UX design intelligence.

```bash
npm install -g ui-ux-pro-max-cli
uipro init --ai codex --global
```

## Ponytail

- Source: <https://github.com/DietrichGebert/ponytail>
- Purpose: Codex plugin for YAGNI, standard-library-first, smallest-correct
  implementation, and over-engineering review.

```bash
codex plugin marketplace add DietrichGebert/ponytail
codex plugin add ponytail@ponytail
```

## Addy Osmani Agent Skills

- Source: <https://github.com/addyosmani/agent-skills>
- Purpose: production-grade engineering lifecycle skills for AI coding agents,
  covering spec, plan, build, test, review, security, performance,
  observability, and shipping.

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo addyosmani/agent-skills \
  --path skills/api-and-interface-design skills/browser-testing-with-devtools \
  skills/ci-cd-and-automation skills/code-review-and-quality \
  skills/code-simplification skills/context-engineering \
  skills/debugging-and-error-recovery skills/deprecation-and-migration \
  skills/documentation-and-adrs skills/doubt-driven-development \
  skills/frontend-ui-engineering skills/git-workflow-and-versioning \
  skills/idea-refine skills/incremental-implementation skills/interview-me \
  skills/observability-and-instrumentation skills/performance-optimization \
  skills/planning-and-task-breakdown skills/security-and-hardening \
  skills/shipping-and-launch skills/source-driven-development \
  skills/spec-driven-development skills/test-driven-development \
  skills/using-agent-skills
```

## Codex System Skills

System skills such as `imagegen`, `openai-docs`, `skill-installer`,
`skill-creator`, and `plugin-creator` are bundled with Codex and are not synced.
