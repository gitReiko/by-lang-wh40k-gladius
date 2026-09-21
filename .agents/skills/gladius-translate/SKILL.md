---
name: gladius-translate
description: Translate and edit Warhammer 40000 Gladius game text from English into Belarusian Cyrillic in this project, including XML entries, Barks dialogue and SRT subtitles, using the project glossary and faction voices.
---

# Translate Gladius

Read the project root `AGENTS.md` for version selection, terminology sources and game-format constraints. All paths below are relative to the project root. These instructions are in English; game translations and responses to the user remain in Belarusian unless requested otherwise.

## Select the text

- Determine the latest existing version in `мод/` by comparing numeric version components. Locate the relevant original in `зыходнікі/` and its counterpart in that version.
- Match XML entries by `entry name`, not line number. Read nearby entries to distinguish names, gameplay descriptions, narrative text and dialogue.
- Work in `BelarusianCyrillic` by default. Do not independently romanize text or automatically synchronize `BelarusianLatin`. A request to continue translating does not authorize conversion to Latin script. For explicitly requested Latin-script work, follow the user's supplied workflow or prepared text; do not invent a transliteration system. Do not make Latin synchronization an automatic follow-up task.

## Translate

- Look up terms in `слоўнік.txt`, including complete phrases, faction annotations and duplicate entries. Compare their usage in the latest version. Inflect terms to fit the sentence without replacing established terminology with arbitrary synonyms.
- Read `тарашкевіца.txt`; for names and dialogue, also read `асаблівасці.txt` and `промты.txt`. Preserve gameplay meaning, conditions, numbers and the distinction between bonuses and penalties. Prefer concise, clear wording for interface text.
- In `Barks.xml`, identify the faction and event from the key, such as `AdeptusMechanicus/...:Attack#0`. Apply Ork speech conventions only to Ork dialogue and relevant names, never to technical keys or the entire interface.
- Use the project's established Latin pronunciation for Imperial names. When `промты.txt` calls for transliterating a human-readable Latin-language utterance, render it in Belarusian Cyrillic while retaining glossary forms. Keep `Do not translate!` entries and technical values unchanged.
- If a term has no reliable equivalent, choose a contextually justified rendering and identify it as a proposal in the result. Continue independent translation work while individual terminology questions remain unresolved.

## Embedded tags inside `value`

- Preserve a snapshot of the relevant entries before editing. Separate human-readable text from technical markup and change only the text between tags.
- Preserve `<style name='Italic'/>`, `<style name='Default'/>`, `<style color='GUI/Red'/>`, `<icon texture='GUI/Bullet'/>` and `<br/>` exactly, including case, whitespace, paths, apostrophes and order. Style switches delimit formatted spans; keep the translated span between the corresponding tags. Preserve repeated breaks such as `<br/><br/>`.
- Do not treat the first `/>` as the end of an `entry`: it may belong to a tag inside `value`. Values in this project normally use double quotes, while embedded attributes use single quotes; inspect the actual entry before automating replacements.
- After translation, automatically compare the complete sequence of embedded tags for each changed `entry name` against its previous state. Comparing only total tag counts is insufficient. Unless markup repair is part of the task, every tag must match exactly. Separately verify that other values and everything outside `value` remain unchanged except for specific fixes within the requested scope.

## Verify and report

Preserve technical content, keys and formatting as specified in `AGENTS.md`. Check placeholder multiplicities, embedded tags and apostrophes, and ensure no duplicate keys were introduced. For SRT, check cue numbers and timestamps. Review the diff for changes outside the requested scope.

Report what was translated, the version and script used, the checks performed and any unresolved terminology. Do not claim in-game validation unless it was actually performed.
