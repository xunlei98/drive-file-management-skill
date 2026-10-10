# Drive File Management Skill

This repository contains a reusable AI skill for organizing a personal Google Drive by purpose while protecting linked systems and sensitive records.

It was adapted from a real Drive organization rulebook. The package intentionally contains no private filenames, document IDs, credentials, or file contents. It teaches the operating decisions that matter:

- classify by Area and responsibility;
- preserve original Drive items, names, links, sharing, and collection structure;
- ask before moving ambiguous or dependency-sensitive files;
- protect AppSheet data and media as coordinated dependency groups;
- keep shared workplace folders intact;
- separate personal, family-business, finance, health, learning, work, and archive material;
- record moves, deletions, verification limits, and user decisions.

## Package contents

- `SKILL.md` — the entrypoint loaded by an AI agent.
- `references/area-map.md` — the current destination map for common file purposes.
- `agents/openai.yaml` — optional display metadata for Codex-style skill interfaces.

## Use by another AI agent

Copy the `drive-file-management` folder into the agent's skills directory, then invoke it for Drive filing or migration work. The agent should read the user's current rulebook and inspect the live Drive before making decisions; this repository is a reusable operating guide, not a copy of the user's private Drive.

## Safety boundary

The skill does not grant permission to delete files, change sharing, or move linked application data. The user must authorize those actions in the active task, and the agent must verify the result and report anything it did not test.
