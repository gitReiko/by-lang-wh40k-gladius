---
name: dow-de-translate
description: Translate and edit Warhammer 40000 Dawn of War - Definitive Edition UCS game text into Belarusian in this repository. Use for interface, descriptions and dialogue in dow 1 de, with English as the reference and the project's game and lore glossaries.
---

# Translate Dawn of War - Definitive Edition

Read the root `AGENTS.md` and `dow 1 de/AGENTS.md`. This skill applies to the first Dawn of War's Definitive Edition, not Gladius or other Dawn of War editions. All paths here are relative to the repository root. Respond in Belarusian unless requested otherwise.

## Select records and script

- Find the latest existing release in `dow 1 de/пераклад/` by numeric version components, unless the user specifies a version. The version at setup is `2.10.3`; ordinary translation does not create a new release.
- English originals in `dow 1 de/зыходнікі/English/` determine meaning, ID coverage and technical tokens. Match by corresponding filename and numeric ID, not line number. Read nearby English records for interface or dialogue context.
- Consult other source languages under `dow 1 de/зыходнікі/` only for candidate interpretations. Check each against English; they may omit records or give incorrect meanings. Do not translate solely from the destination's existing Czech or Ukranian text.
- Work by default in `dow 1 de/пераклад/<version>/Engine/Locale/Ukranian/Engine.ucs` for Belarusian Cyrillic. Belarusian Latin script belongs in the sibling `Czech/Engine.ucs`. Preserve the literal locale spellings. For additional files, establish their source and installation paths before editing.
- A request to continue translation defaults to Cyrillic. For explicitly requested Latin-script changes, use the user's supplied workflow or prepared text under the root rules; do not infer a romanization system from Czech spelling or Gladius conventions.
- Inspect the current destination rather than assuming it is already Belarusian or complete. Translate the requested records; when their English IDs are missing, add those records using English structure and order while preserving existing work. Do not fill every unrelated missing ID during a narrow edit.

## Translate and record terms

- Search complete English phrases in both `dow 1 de/слоўнік dow.txt` and the root `слоўнік warhammer 40k.txt` before searching components. Use the former for game and interface terms and the latter for Warhammer lore, including lore terms shown in menus. Resolve conflicting forms by context and established usage; report unresolved choices.
- Read the root `тарашкевіца.txt` and, for names and dialogue, `асаблівасці.txt`. Use classical Belarusian orthography, appropriate faction voices and concise interface wording. Preserve gameplay conditions, quantities, negation and bonuses or penalties.
- Add clear new equivalents to the appropriate glossary after checking both for existing entries, using `English term = Belarusian equivalent`. Include object or faction context when needed. Keep uncertain renderings as proposals and report them; do not standardize unrelated terminology.
- Separate human-readable text from IDs, placeholders, references and technical values. Empty or technical-only records do not automatically require translation.

## Edit and verify UCS safely

- Follow the UCS rules in `dow 1 de/AGENTS.md`: inspect raw encoding first, preserve UTF-16 LE with BOM and CRLF where present, and change only text after the first literal tab. Keep a pre-edit snapshot of the affected files or records.
- Preserve full tokens such as `%1PLAYERNAME%` and `$9506`; do not shorten checks to the Gladius `%1%` pattern. Compare token spelling, case and occurrence counts with English and the prior state. Investigate existing mismatches rather than copying them into new translations.
- Preserve IDs, order, empty values, final newline and unrelated records. Do not introduce duplicate IDs, physical newlines inside a value, extra tab separators or XML escaping. Do not rewrite a UCS file through a default UTF-8 writer.
- After saving, reread bytes and check encoding, BOM, line endings, record structure, token integrity and the exact scope of changed or added IDs. Keep all source-language originals and archived releases unchanged.

Report the version, script and locale slot, edited files or ID ranges, glossary additions, checks and unresolved questions. Distinguish untranslated starting material from finished work; do not claim installation or in-game validation unless performed.
