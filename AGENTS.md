# Belarusian translation of Warhammer 40,000: Gladius — Relics of War

## Working files

- Work with the latest version **present in the repository** under `мод/`. Compare numeric version components, not alphabetical order or modification dates: `1.10.0` is newer than `1.9.3`. The latest version when these instructions were written was `1.18.1`; determine it again before working.
- Other versions are archives: read them for comparison, but do not edit them without an explicit request. Do not create a new version when the task is to improve the current one.
- English originals are in `зыходнікі/English/*.xml` and `зыходнікі/srt/*.English.srt`. Do not change them while translating. The directory name does not establish their game version; verify that they match the target version when updating.
- In the latest version, language files are under `мод/<version>/Belarusian/Data/Core/Languages/BelarusianCyrillic/` and the sibling `BelarusianLatin/`. Subtitles are under `Belarusian/Data/Cinematics/Clips/Intros/`. Check actual paths: archived versions have different layouts.
- Translate into `BelarusianCyrillic`. Do not independently romanize text or automatically synchronize `BelarusianLatin`. A request to “continue” does not authorize romanization. For explicitly requested Latin-script work, use the workflow or prepared text supplied by the user; do not invent a conversion system. Do not make Latin synchronization an automatic next step.
- `Data/Core/Languages/Languages.xml`, `Data/GUI/LabelStyles/`, fonts, images and `SteamID.txt` are mod settings and assets; exclude them from bulk text translation.

## Language and terminology

- `слоўнік.txt` is the primary terminology source. Search for the complete English phrase, then its components and usage in the latest version. Consider faction and object-type annotations; inflect the translation to fit the context.
- The glossary contains duplicates and conflicting variants. Do not automatically choose the first entry or standardize the entire project. Follow context and established usage, and report unresolved conflicts.
- As part of translation work, add new terms to `слоўнік.txt` whenever their meaning and Belarusian rendering are clear from context and project usage; no separate request is needed. First check for an existing equivalent to avoid duplicates. Record the English term and Belarusian equivalent in the glossary's existing format, with faction or object-type context where needed. Do not arbitrarily replace established terminology. If a rendering remains uncertain, mark it as a proposal rather than an established equivalent and report the uncertainty. Mention glossary additions in the result.
- `асаблівасці.txt` covers name pronunciation and Ork speech; `тарашкевіца.txt` contains classical orthography notes; `лацінка.txt` documents conversion conventions. Read the relevant files without copying their rules into a separate glossary. Conversion notes do not authorize independent romanization.
- Translate into Belarusian using classical orthography and the style of nearby entries. Do not mechanically replace every `не` with `ня` or apply letter-pattern replacements globally based on search patterns in the notes.
- `промты.txt` provides dialogue context. `над чым варта папрацаваць.txt` contains suggestions and questions, not approved replacements. `спіс перакладзеных файлаў.txt` and README may lag behind the files; do not infer completion from percentages alone.

## Preserve formatting

- Language XML uses the game's format with embedded tags inside `value`, for example `value="Тэкст<br/><style name='Default'/>"`. Strict XML parsers reject literal `<` characters in attributes. Do not reserialize these files through a standard XML parser or escape all their contents merely to pass XML validation.
- Edit text values selectively. Preserve `entry name`, structure, comments, entry order, technical attributes, UTF-8 encoding, BOM presence and line endings.
- Preserve placeholders such as `%1%` and `%2%`, including their occurrence counts. Their order may change to fit Belarusian sentence structure. Preserve embedded tags, nesting, style names, resource paths and syntactic apostrophes. Do not insert unescaped double quotes into `value="..."`.
- Do not translate technical values, `...Count` counters in `Barks.xml`, identifiers or entries under `Do not translate!` comments. Use context to distinguish human-readable Latin-language utterances from technical identifiers.
- In SRT files, change only subtitle text; preserve cue numbers, timestamps, block order and boundaries.
- Check changed entries against both the original and the state before editing. Distinguish pre-existing defects from introduced ones; do not incidentally “fix” an entire file. File checks do not replace checking the display in the game.

## Project skills

- `gladius-translate`: translate and edit game text, dialogue and subtitles.
- `gladius-review`: review terminology, language, completeness and technical integrity.
- `gladius-update`: carry translations forward to a new game version and compare entry sets.

Skills are in `.agents/skills/`. Respond to the user in Belarusian unless they request another language. In the result, state the version where applicable, changed files, checks performed and unresolved issues. Do not update completion percentages without a defined calculation.
