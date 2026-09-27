---
name: dow-de-update
description: Compare English source versions and prepare a new Belarusian translation release for Warhammer 40000 Dawn of War - Definitive Edition in dow 1 de, preserving UCS IDs, archived releases and the file-replacement installation layout.
---

# Update Dawn of War - Definitive Edition

Read the root `AGENTS.md` and `dow 1 de/AGENTS.md`. All paths here are relative to the repository root. Use this skill for version migrations, source-change comparisons or release preparation for this edition. Ordinary translation stays in the current release. Report in Belarusian unless requested otherwise.

## Establish the baseline

- Find the latest existing release in `dow 1 de/пераклад/` by numeric version components. The version at setup is `2.10.3`, recorded in `dow 1 de/інфа.txt`; verify the current state and target from the user's request and supplied materials.
- Identify the target English originals under `dow 1 de/зыходнікі/English/` or in the user-supplied source location. Establish their version and look for an older English baseline. A source-language folder, a translated release or a file date does not prove the English game version.
- Other languages under `dow 1 de/зыходнікі/` can lag behind or mistranslate English. Do not use Czech or Ukranian key sets as the release baseline. Preserve all supplied originals during comparison and migration.
- If version information or originals are missing, complete the comparison that is possible, state its limits and ask only for information needed to finish the migration. Do not claim compatibility with an unconfirmed version.

## Compare and migrate

- Match files by component and corresponding filename, and records by numeric ID. Detect duplicates before making lookups. With both English versions, distinguish new IDs, removed IDs, unchanged text and text changed under existing IDs.
- Without the old English baseline, report coverage and key-set differences but do not infer which meanings changed under retained IDs. Flag uncertain carried-forward translations for review.
- Create `dow 1 de/пераклад/<target-version>/` only for an authorized new release. Copy the latest applicable translation package, preserving its archive. Inspect an existing target directory before merging; do not blanket-overwrite work already there. A comparison-only task does not create a release.
- Preserve the script mapping: `Engine/Locale/Ukranian/` for Belarusian Cyrillic and `Engine/Locale/Czech/` for Belarusian Latin. When copying a release, carry existing Latin files forward unchanged unless Latin edits are explicitly requested with a supplied workflow or prepared text. Report the scope and currency of each script separately.
- Retain translations whose meaning remains applicable. Use `dow-de-translate` for new or changed text. Add missing records from English within the migration scope; the initial Ukranian file is not a complete template. Do not replace existing translations wholesale with English or another source language.
- Investigate additional or removed IDs before deletion; they may reflect mismatched versions or component mappings. Confirm removals against the correct English baselines. Preserve all unaffected IDs, values and ordering, plus each file's encoding, BOM and line endings.
- For new files, establish the component, relative installation path and encoding from the supplied materials. Do not put every new UCS file in Engine merely because Engine is currently the only component represented.
- Consult `dow 1 de/слоўнік dow.txt` and the shared root `слоўнік warhammer 40k.txt`, adding clear game and lore equivalents to the appropriate file under the root terminology rules.

## Prepare and verify the release

- Keep paths relative to the installed game root inside the release. For example, the release's `Engine/Locale/Ukranian/Engine.ucs` replaces that same relative game path; `Engine/Locale/Czech/Engine.ucs` carries the Latin variant. State which script slots are included and any incomplete or unchanged variant.
- The current installation method replaces files. When preparing installation instructions, include backup before replacement and restoration from that backup. Package only the requested replacement files and relevant installation instructions; source-language references and glossaries are not game payload. Release preparation alone does not write into the live installation.
- Review changed files with `dow-de-review`, checking English ID coverage, full token integrity, UTF-16/BOM and line-ending preservation, and the destination layout. Confirm that originals and archived releases remain unchanged.
- Update `dow 1 de/інфа.txt` and any existing game-specific release notes only to reflect completed work. State unfinished translation, unknown English changes and script differences; do not infer percentages or full compatibility from a successful file comparison.

Report source and target versions, added/changed/removed ID counts where supported, changed files, glossary additions, carried-forward script variants, validation and remaining work. Distinguish package preparation from actual installation and in-game testing.
