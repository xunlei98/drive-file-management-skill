---
name: drive-file-management
description: Organize a personal Google Drive by purpose and area, while preserving linked files, AppSheet dependencies, shared folders, and sensitive records. Use when reviewing, filing, moving, archiving, or cleaning up Drive files.
---

# Drive file management

Use this skill to organize a personal Google Drive into a small set of purpose-based Areas. Classify by the responsibility the file serves and where the user would naturally look for it, not by extension, language, or the application that created it.

## Operating rules

- Inspect the relevant tree and enough metadata or content to establish purpose before moving anything.
- Preserve original filenames, folder names, document identities, sharing, ownership, and internal structure unless the user explicitly asks for a rename.
- Move the original Drive item when links matter. Never create a replacement copy as an incidental filing step.
- Ask about an ambiguous purpose, ownership, access change, or unresolved dependency before moving the affected item.
- Keep a move log with old and new paths. Verify the destination and old-path absence, and distinguish a local mounted result from confirmed cloud state.
- Delete only when the user explicitly requests deletion or confirms that a specific item is obsolete. Do not empty a bin or silently delete backups.
- Treat old modification dates as evidence, not proof that an item is obsolete.
- Keep everyday documents lightweight. Preserve linked collections, software repositories, media libraries, and other units intact.

## Canonical Areas

Use the existing Areas and the detailed map in [references/area-map.md](references/area-map.md). Create a new Area only when a reviewed group genuinely needs one.

The current main Areas are `00 Inbox`, `01 File Management`, `Family Business`, `Finances & Insurance`, `Health & Wellbeing`, `Home & Property`, `Learning & Interests`, `Personal Administration`, `Trading & Investing`, `Travel`, and `Work`.

## Protected systems

- Keep active AppSheet files under `Work/Pharmacy/Systems/AppSheet/`. Treat its `data/`, `Image/`, linked source Sheets, media folders, worksheet tabs, columns, row keys, app IDs, automations, and generated-file paths as a dependency group. Move them only as a coordinated, verified migration.
- Retired AppSheet project folders may go under `Work/Pharmacy/Systems/AppSheet/Archive/` after the app is retired and its data dependencies are understood. Do not archive a folder merely because it is old.
- Keep the shared `FARMASI HOSPITAL LIMBANG` folder as an intact shortcut under `Work/`. Do not reorganize its contents without explicit authorization; preserve staff access and shared structure.
- Keep password-vault database backups under `Personal Administration/Security/Password Vault Backups/`. Treat them as highly sensitive and do not inspect or expose their contents unnecessarily.
- Keep private family and close-contact records under `Personal Administration/Family & Friends/`; keep family-business entities under `Family Business/Operations/Records/`.

## AppSheet verification

Before a dependency migration, record the app ID and version, exact data-source identity, Drive parent, default app folder, relative media paths, static assets, templates, automations, shared dependencies, and any baseline loading errors. After moving, check sync, tables, images, attachments, sharing, and generated-file workflows as appropriate. Report untested writes, uploads, automations, or device behavior explicitly. Stop and roll back a failed migration before continuing.

## Maintenance

Use `00 Inbox` for incoming files awaiting classification. Keep the rulebook in `01 File Management` and record completed moves, user decisions, deletions, and verification limits in a separate progress or migration log. Do not place private file contents, credentials, app IDs, or personal identifiers in a shared skill package.
