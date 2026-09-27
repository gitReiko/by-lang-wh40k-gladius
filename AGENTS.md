# Belarusian translations of Warhammer 40,000 games

## Repository layout

- Shared Warhammer terminology and language guidance live in the project root: `слоўнік warhammer 40k.txt`, `асаблівасці.txt` and `тарашкевіца.txt`.
- Game-specific originals, translations, glossaries and supporting materials belong in each game's subdirectory. Determine the game before selecting files, versions or skills; do not apply Gladius formats or terminology to another game by default.
- Gladius lives in `gladius/`. Read `gladius/AGENTS.md` for its working paths, version selection and format constraints. Its releases are in `gladius/пераклад/`, originals in `gladius/зыходнікі/`, and game terminology in `gladius/слоўнік gladius.txt`.
- Dawn of War - Definitive Edition lives in `dow 1 de/`. Read `dow 1 de/AGENTS.md` for its English baseline, UCS format, script-to-locale mapping and file-replacement installation layout. Its releases are in `dow 1 de/пераклад/`, multilingual originals in `dow 1 de/зыходнікі/`, and game terminology in `dow 1 de/слоўнік dow.txt`.
- Project skills remain in `.agents/skills/` at the repository root. The `gladius-*` skills apply to Gladius only; the `dow-de-*` skills apply to the first Dawn of War's Definitive Edition only.

## Language and terminology

- Use the relevant game's glossary for game and interface terms and the root `слоўнік warhammer 40k.txt` for Warhammer universe terms, including factions, names, units, weapons and buildings.
- Search for the complete English phrase in the shared glossary and the relevant game's glossary, where available, before looking up its components and usage in the target translation. Choose the equivalent for the meaning in context; a lore name in an interface remains a lore term. Consider faction and object-type annotations and inflect the translation to fit the sentence.
- The glossaries may contain duplicates and conflicting variants, including across the two files. Do not automatically choose the first entry or give one file blanket priority. Follow context and established usage, and report unresolved conflicts without standardizing the entire project.
- As part of translation work, add new terms to the appropriate glossary whenever their meaning and Belarusian rendering are clear from context and project usage; no separate request is needed. Check the shared and relevant game glossaries for an existing equivalent first. Add game and interface terminology to that game's glossary and Warhammer universe terminology to the root `слоўнік warhammer 40k.txt`, using the existing `English term = Belarusian equivalent` format and faction or object-type context where needed. Do not duplicate a term in both files merely because it occurs in both interface and narrative text. Do not arbitrarily replace established terminology. If a rendering remains uncertain, mark it as a proposal rather than an established equivalent and report the uncertainty. Mention glossary additions and the file used in the result.
- `асаблівасці.txt` covers name pronunciation and Ork speech; `тарашкевіца.txt` contains classical orthography notes. Read the relevant files without copying their rules into a separate glossary.
- Translate into Belarusian using classical orthography and the style of nearby entries. Do not mechanically replace every `не` with `ня` or apply letter-pattern replacements globally based on search patterns in the notes.
- Translate into Belarusian Cyrillic by default. Do not independently romanize text or automatically synchronize Latin-script translations. A request to “continue” does not authorize romanization. For explicitly requested Latin-script work, use the workflow or prepared text supplied by the user; do not invent a conversion system or make synchronization an automatic next step.
- README and progress notes may lag behind the files; do not infer completion from percentages alone. Suggestions and questions in notes are not approved replacements.

## Preserve formatting

- Edit translation text selectively. Preserve the game's identifiers, structure, comments, entry order, technical attributes, encoding, BOM presence and line endings. Follow the relevant game's instructions for its actual file format.
- Preserve placeholders and their occurrence counts, markup and resource paths. Do not translate technical values or identifiers; use context to distinguish human-readable text from technical content.
- Keep originals unchanged while translating. Archived releases are for comparison; edit them only on explicit request. Do not create a new version for an improvement to an existing release.
- Check changed entries against both the original and the state before editing. Distinguish pre-existing defects from introduced ones; do not incidentally “fix” an entire file. File checks do not replace checking the display in the game.

## Project skills

- `gladius-translate`: translate and edit game text, dialogue and subtitles.
- `gladius-review`: review terminology, language, completeness and technical integrity.
- `gladius-update`: carry translations forward to a new game version and compare entry sets.
- `dow-de-translate`: translate and edit Dawn of War - Definitive Edition UCS text into Belarusian.
- `dow-de-review`: review Dawn of War - Definitive Edition terminology, language, English ID coverage and UCS integrity.
- `dow-de-update`: compare Dawn of War - Definitive Edition source versions and prepare translation releases for installation by replacing files.

Skills are in `.agents/skills/`. Respond to the user in Belarusian unless they request another language. In the result, state the version where applicable, changed files, checks performed and unresolved issues. Do not update completion percentages without a defined calculation.
