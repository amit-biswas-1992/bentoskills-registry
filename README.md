# bentoskills-registry

The official registry of UI/UX skills for [bentoskills.sh](https://github.com/amit-biswas-1992/bentoskills) — a marketplace for Claude Code agent skills.

## What is this?

This repo is the source of truth for every skill published to bentoskills.sh. The bentoskills web app syncs from this repo every 15 minutes via a Vercel Cron that reads `registry.json` and the contents of each skill directory.

## Structure

```
registry.json              # Index of every published skill
skills/
  design-critique/
    skill.yaml             # Metadata (see schema below)
    README.md              # Full skill documentation
  accessibility-review/
    skill.yaml
    README.md
  ...
```

## Adding a new skill

1. Fork this repo
2. Create a new directory under `skills/` with your slug (lowercase, hyphens)
3. Add a `skill.yaml` following the schema below
4. Add a `README.md` with usage examples and description
5. Append an entry to `registry.json`
6. Open a PR

Once merged, the next cron run (within 15 minutes) will publish your skill to bentoskills.sh.

## `skill.yaml` schema

```yaml
slug: my-skill              # lowercase, hyphens only, unique
name: My Skill              # display name, 1-80 chars
tagline: One line summary.  # 1-140 chars
version: 1.0.0              # semver
author: your-name
category: critique          # accessibility | critique | copy | handoff | research | system
tags:                       # up to 20 tags, 30 chars each
  - ui
  - feedback
license: MIT                # optional, SPDX identifier
homepage: https://...       # optional
publishedAt: 2026-04-01     # optional, ISO date
```

## `registry.json` schema

```json
[
  {
    "slug": "my-skill",
    "path": "skills/my-skill",
    "sha": "my-skill-v1"
  }
]
```

## License

Each skill is licensed independently by its author — check the `license` field in `skill.yaml` and the `README.md` of each skill. The registry index and this README are MIT-licensed.
