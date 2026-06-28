# Codex Skills Public Catalog

[中文说明](README.zh-CN.md)

Public index for Jackie's Codex skill setup.

This repository intentionally does **not** store skill source folders. It only
stores category indexes, source notes, and restore instructions. Private-only
skills and public-eligible local skills are currently staged in the private
management repository until public source publishing is explicitly enabled.

## Repositories

- Public catalog: `codex-skills-public`
- Private source: `codex-skills-private`

## What This Repository Tracks

This repository has no `skills/` directory. It tracks installable sources,
public-safe categories, and restore guidance.

| Group | Storage | Purpose |
| --- | --- | --- |
| Public-eligible local skills | Indexed here, source staged privately | Local/self-authored skills that can potentially be published later |
| Third-party skills | Source and install command only | Reinstall from upstream projects |
| Codex system skills | Mentioned only | Managed by Codex, not synced |
| Private-only skills | Category only, no concrete names | Personal/digital-self and local monitor materials stay private |

## Public-Eligible Local Skills

These skill bodies are not published here yet, but they are not classified as
private-only:

| Category | Skills | Purpose |
| --- | --- | --- |
| dontbesilent workflows | `dbs`, `dbs-*` | Business diagnosis, content, goals, decisions, benchmarking, reports, and learning workflows |
| Digital immortality tooling | `immortal-skill` | Persona/distillation framework and reusable templates |
| Design and creation | `design`, `design-system`, `brand`, `banner-design`, `ui-styling`, `slides`, `hatch-pet` | Brand, UI, slides, banners, sprites, and visual production |

## Use-Case Categories

This is the day-to-day entry view inspired by the four-bucket workflow:

| Use case | Meaning | Representative skills |
| --- | --- | --- |
| `write` | Writing, editing, content, teaching, narrative, and messaging | `dbs-content`, `dbs-content-system`, `dbs-hook`, `dbs-xhs-title`, `dbs-ai-check`, `brand`, `slides`, `teach`, `writing-great-skills` |
| `draw` | Design, visuals, UI, banners, slides, and generated assets | `design`, `design-system`, `banner-design`, `ui-styling`, `hatch-pet`, `ui-ux-pro-max`, `imagegen` |
| `info` | Information lookup, diagnosis, architecture, domain understanding, and analysis | `ask-matt`, `diagnosing-bugs`, `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, `dbs-diagnosis`, `dbs-benchmark`, `dbs-deconstruct`, `openai-docs` |
| `pm` | Planning, project management, execution, state, PRD, issues, triage, and handoff | `dbs`, `dbs-action`, `dbs-goal`, `dbs-good-question`, `dbs-decision`, `dbs-save`, `dbs-restore`, `dbs-report`, `to-prd`, `to-issues`, `triage`, `tdd`, `implement`, `handoff` |

## Third-Party Source-Only Skills

| Source | Skills | Purpose |
| --- | --- | --- |
| `mattpocock/skills` | `setup-matt-pocock-skills`, `ask-matt`, `grill-with-docs`, `grill-me`, `grilling`, `to-prd`, `to-issues`, `triage`, `tdd`, `diagnosing-bugs`, `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, `prototype`, `implement`, `resolving-merge-conflicts`, `handoff`, `teach`, `writing-great-skills` | Engineering workflows, TDD, architecture, PRDs, issues, triage, handoffs, and teaching |
| `ui-ux-pro-max` | `ui-ux-pro-max` | Searchable UI/UX design intelligence |

## Codex System Skills

These are bundled with Codex and are not synced by these repositories:

- `imagegen`
- `openai-docs`
- `plugin-creator`
- `skill-creator`
- `skill-installer`

## Restore Overview

1. Clone this public catalog.
2. Clone the private repository on trusted machines.
3. Use the private repository's restore script:

```bash
cd ~/Documents/codex-skills-private
./scripts/sync-to-codex.sh
```

4. Reinstall third-party skills from `catalog/sources.md` or
   `manifests/third-party.json`.

## Safety Boundary

This public repo must not contain:

- `skills/` source directories
- personal persona or digital-self materials
- local Codex usage monitor internals
- local tokens, cookies, or API keys
- raw or redacted chat corpus paths
