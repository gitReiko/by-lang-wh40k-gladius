# Belarusian translation of Warhammer 40,000: Gladius — Relics of War

The root `AGENTS.md` contains shared language and terminology rules. These instructions apply to Gladius. All paths below are relative to the repository root unless stated otherwise.

## Working files

- Work with the latest version **present in the repository** under `gladius/пераклад/`. Compare numeric version components, not alphabetical order or modification dates: `1.10.0` is newer than `1.9.3`. The latest version when these instructions were written was `1.18.1`; determine it again before working.
- Other versions are archives: read them for comparison, but do not edit them without an explicit request. Do not create a new version when the task is to improve the current one.
- English originals are in `gladius/зыходнікі/English/*.xml` and `gladius/зыходнікі/srt/*.English.srt`. Do not change them while translating. The directory name does not establish their game version; verify that they match the target version when updating.
- In the latest version, language files are under `gladius/пераклад/<version>/Belarusian/Data/Core/Languages/BelarusianCyrillic/` and the sibling `BelarusianLatin/`. Subtitles are under `gladius/пераклад/<version>/Belarusian/Data/Cinematics/Clips/Intros/`. Check actual paths: archived versions have different layouts.
- Translate into `BelarusianCyrillic`. Follow the root rules for explicitly requested Latin-script work; do not independently romanize text or automatically synchronize `BelarusianLatin`.
- Within a release's `Belarusian/` directory, `Data/Core/Languages/Languages.xml`, `Data/GUI/LabelStyles/`, fonts, images and `SteamID.txt` are mod settings and assets; exclude them from bulk text translation.

## Gladius terminology and supporting materials

- Use `gladius/слоўнік gladius.txt` for Gladius game and interface terms and the shared root `слоўнік warhammer 40k.txt` for Warhammer universe terms. Search both before choosing or adding an equivalent, following the root terminology rules. Add new Gladius game terms to the former and new lore terms to the latter.
- Shared pronunciation and spelling guidance remains in the root `асаблівасці.txt` and `тарашкевіца.txt`.
- `gladius/лацінка.txt` documents Gladius conversion conventions. Consult it for explicitly requested Latin-script work; it does not authorize independent romanization or establish conventions for other games.
- `gladius/workshop.txt` contains Gladius Workshop material; `gladius/README.md` and `gladius/інфа.txt` are game-specific documentation and notes.
- Older instructions referred to `промты.txt`, `над чым варта папрацаваць.txt` and `спіс перакладзеных файлаў.txt`; these files are currently absent. If supplied again, verify their location and relevance to Gladius before using them. Dialogue prompts provide context, suggestions are not approved replacements, and progress percentages are not proof of completion.

## Preserve Gladius formatting

- Language XML uses the game's format with embedded tags inside `value`, for example `value="Тэкст<br/><style name='Default'/>"`. Strict XML parsers reject literal `<` characters in attributes. Do not reserialize these files through a standard XML parser or escape all their contents merely to pass XML validation.
- Edit text values selectively. Preserve `entry name`, structure, comments, entry order, technical attributes, UTF-8 encoding, BOM presence and line endings.
- Preserve placeholders such as `%1%` and `%2%`, including their occurrence counts. Their order may change to fit Belarusian sentence structure. Preserve embedded tags, nesting, style names, resource paths and syntactic apostrophes. Do not insert unescaped double quotes into `value="..."`.
- Do not translate technical values, `...Count` counters in `Barks.xml`, identifiers or entries under `Do not translate!` comments. Use context to distinguish human-readable Latin-language utterances from technical identifiers.
- In SRT files, change only subtitle text; preserve cue numbers, timestamps, block order and boundaries.
- Check changed entries against both the original and the state before editing. Distinguish pre-existing defects from introduced ones; do not incidentally “fix” an entire file. File checks do not replace checking the display in the game.
