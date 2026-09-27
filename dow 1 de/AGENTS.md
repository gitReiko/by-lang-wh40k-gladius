# Belarusian translation of Warhammer 40,000: Dawn of War - Definitive Edition

Read the root `AGENTS.md` for shared language and terminology rules. These instructions apply to the first Dawn of War's Definitive Edition. All repository paths below are relative to the repository root, including when the working directory is `dow 1 de/`.

## Working files and versions

- Releases live in `dow 1 de/пераклад/`. The current translation version at setup is `2.10.3`, also recorded in `dow 1 de/інфа.txt`. Recheck the latest existing version by numeric components before working; do not choose by file dates or alphabetical order. Use an explicitly requested version when supplied.
- Improve the latest existing release without creating a new version. Earlier releases are archives; preserve them unless the user explicitly requests changes there.
- Original files in different languages live under `dow 1 de/зыходнікі/`. English in `dow 1 de/зыходнікі/English/` is the reference for meaning, IDs and technical tokens. Other languages can be consulted for possible renderings but may be incomplete, outdated or wrong. A majority of secondary translations does not override English.
- Match originals by language, corresponding file and numeric string ID, never by line position. Inspect actual paths as more files are added; currently each source locale contains `Engine.ucs`. Do not assume all future files belong to the Engine component.
- Preserve all originals while translating. A source directory name does not prove its game version; verify the English baseline's version for release migrations. A translated release is not an older English baseline.

## Script-to-locale mapping

| Belarusian script | Destination relative to the release directory |
| --- | --- |
| Cyrillic | `Engine/Locale/Ukranian/Engine.ucs` |
| Latin | `Engine/Locale/Czech/Engine.ucs` |

- Keep the literal spelling `Ukranian`, including its missing second `i`; do not rename it to `Ukrainian` or to a Belarusian language name. These directory names are installation slots, not the intended language of the translated text.
- Default translation work targets Belarusian Cyrillic in `Ukranian`. `Czech` is reserved for Belarusian Latin script because the alphabets are similar; it is not a request to translate into Czech.
- Follow the root rules for explicitly requested Latin-script work using the user's supplied workflow or prepared text. The destination mapping alone does not authorize automatic romanization or synchronization. Do not import `gladius/лацінка.txt` as Dawn of War's conversion workflow without the user's instruction.
- At setup, the two destination files are byte-identical to their respective Czech and Ukranian originals; they are starting material, not completed Belarusian translations. Recheck their current contents before editing. The Ukranian original is substantially smaller than English. Do not assume an existing destination has every English ID or that a missing string will fall back correctly in the game.

## Terminology

- Use `dow 1 de/слоўнік dow.txt` for game and interface terms unrelated to Warhammer lore. This file is initially empty; add clear equivalents during translation in the existing project format `English term = Belarusian equivalent`.
- Use the root `слоўнік warhammer 40k.txt` for factions, names, units, weapons and other universe terms, even when they occur in the interface. Search the complete phrase in both glossaries before components; follow the root rules for conflicts, inflection, new entries and proposals.
- Read the root `тарашкевіца.txt` and, for names and faction voices, `асаблівасці.txt`. Apply Ork speech to appropriate dialogue, not technical IDs or the whole interface. Gladius-specific game terms are not Dawn of War's glossary.

## Preserve UCS format

- The inspected `.ucs` files are UTF-16 LE with BOM (`FF FE`) and CRLF line endings. Detect encoding and line endings from bytes before editing each file, then preserve them, including the final newline. Do not save these files using a tool's default UTF-8 encoding.
- An observed record is a decimal ID, a literal tab and its text, on one physical line. Split only at the first tab. Preserve the numeric ID spelling, delimiter, entry order, empty values and any non-record lines. Do not sort or rebuild the entire file for a text edit.
- Detect duplicate IDs before building a lookup; do not silently collapse them. Match IDs within corresponding files rather than assuming IDs are unique across every component. Add missing English IDs only within the translation or update scope, preserving existing records and using the corresponding English order to position additions. Do not remove extra IDs solely because they are absent from one source file.
- Preserve complete tokens such as `%1PLAYERNAME%`, `%2CHATMESSAGE%` and `$9506`, including spelling, case and multiplicity. Check token order constraints before rearranging them; a literal percentage such as `100%` is not itself a placeholder. Preserve any encountered control sequences, markup and technical paths according to the actual file, without imposing Gladius XML rules. Ordinary quotation marks in UCS text do not need XML escaping.
- Change text only after the first tab. Do not insert physical newlines or new tab separators inside a value. Distinguish an existing empty value or technical-only record from untranslated prose; do not fill it mechanically.
- Compare each edited record with both English and its pre-edit state. Report pre-existing missing IDs or token defects separately from introduced defects. After writing, reread bytes and verify encoding, BOM, line endings, IDs, tokens and unchanged out-of-scope records. File checks do not prove in-game display or font coverage.

## Installation at this stage

- Installation currently replaces game files. A release directory mirrors paths relative to the installed game root: for example, `dow 1 de/пераклад/2.10.3/Engine/Locale/Ukranian/Engine.ucs` replaces `Engine/Locale/Ukranian/Engine.ucs` under that root. The Czech destination is mapped in the same way.
- Preserve this directory structure when preparing files or a package. State which script and locale slot the package contains. Include translation files for the requested scope; originals and glossaries are reference material, not replacement game files.
- Installation instructions should say to back up the original files before replacement and explain how to restore them. Similar alphabets do not establish complete glyph support; report in-game validation only when performed. Creating or updating translation files does not itself install them into a live game directory.
