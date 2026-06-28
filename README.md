# Codex Skills Public Catalog

Public index for Jackie's Codex skill setup.

This repository intentionally does **not** store skill source folders. It only
stores category indexes, source notes, and restore instructions. Private and
personal skills live in the private repository.

## Repositories

- Public catalog: `codex-skills-public`
- Private source: `codex-skills-private`

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
- personal persona materials or their concrete skill names
- private business workflow contents or concrete skill names
- local tokens, cookies, or API keys
- raw or redacted chat corpus paths
