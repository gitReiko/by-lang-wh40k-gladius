---
name: gladius-update
description: Prepare this project's Gladius translation for a new game version, compare updated English originals with existing translations and carry forward translated entries while preserving archived releases.
---

# Update the Gladius translation

Read the project root `AGENTS.md` for shared rules and `gladius/AGENTS.md` for Gladius paths and format constraints. All paths below are relative to the repository root, even when the working directory is `gladius/`. Use this skill for Gladius version migrations or analysis of its source changes; other games use their own update workflows. Ordinary translation work belongs in the latest existing release without creating a new version directory. Report in Belarusian unless requested otherwise.

## Establish the baseline

- Find the latest version in `gladius/пераклад/` using numeric comparison. Determine the target version from the user's request and available materials, not from file dates.
- Gladius originals are in `gladius/зыходнікі/English/` and `gladius/зыходнікі/srt/`. Check whether their version is known and whether earlier English originals are available. An archived Belarusian release is not itself an earlier English baseline.
- If the target version or its originals are unknown, prepare the comparison that is possible and ask only for the missing information. Do not describe a translation as updated for an unconfirmed version.

## Compare and migrate

- Match XML by filename and `entry name`. When both old and new English originals are available, distinguish added keys, removed keys, unchanged entries and entries whose English text changed under an existing key.
- Without the old English baseline, key-set differences can be identified, but not all meaning changes under existing keys. Flag those entries for manual review.
- When the user asks to create a new release, copy the latest mod release into `gladius/пераклад/<target-version>/`, preserving the previous release as an archive. If the target directory already exists, inspect its state first and do not overwrite existing work with a blanket copy. Do not create a directory for a comparison-only request.
- Retain existing translations that remain applicable. Translate new entries and review changed entries using `gladius-translate`, consulting `gladius/слоўнік gladius.txt` for game and interface terms and the shared root `слоўнік warhammer 40k.txt` for Warhammer universe terms. Add clear new equivalents to the appropriate glossary after checking both files for existing entries. Do not replace an entire Belarusian file with an English template.
- Do not delete additional keys merely because they are absent from the originals: they may be mod settings or evidence of mismatched versions. Removals must follow a confirmed comparison.
- Translate in `BelarusianCyrillic`. When copying an authorized release package, carry forward existing Latin-script files unchanged. Do not independently romanize new text or regenerate or synchronize `BelarusianLatin`. Follow the user's supplied workflow or prepared text for explicitly requested Latin-script changes; do not invent a conversion system or treat synchronization as an automatic follow-up.
- Match new subtitles to the corresponding cinematics. If the edit of a cinematic changed, do not mechanically transfer old timestamps to the new original.
- Preserve settings, fonts and other mod resources. Change them only when necessary for the specific update and supported by the new version's materials.

## Finish

Check changed files using `gladius-review` and confirm that archives and originals remain unchanged. Report the source and target versions, counts of added and reviewed entries, unknown changes and the actual scope of any script variants carried forward. Update `gladius/README.md` and any Gladius progress tracking only to reflect completed work; do not claim full compatibility without appropriate validation.
