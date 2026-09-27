---
name: dow-de-review
description: Review this repository's Belarusian Dawn of War - Definitive Edition UCS translation for meaning, terminology, missing English IDs, placeholders, encoding and locale placement. Use for audits, proofreading and review of translation changes in dow 1 de.
---

# Review Dawn of War - Definitive Edition

Read the root `AGENTS.md` and `dow 1 de/AGENTS.md`. All paths here are relative to the repository root. Use the requested scope and version, otherwise the latest numerically selected release in `dow 1 de/пераклад/`. A review reports findings; a request to fix errors authorizes targeted corrections within that scope. Report in Belarusian unless requested otherwise.

## Establish the comparison

- Use `dow 1 de/зыходнікі/English/` as the reference. Match corresponding files and numeric IDs; other source languages provide optional clues, not authority or proof of completeness. Identify whether the English source version is known when assessing compatibility.
- Check Belarusian Cyrillic in `Engine/Locale/Ukranian/` and Belarusian Latin in `Engine/Locale/Czech/`, relative to the chosen release. Keep the spelling `Ukranian`. Review the requested script; the default is Cyrillic. Comparing both scripts when requested does not authorize generating or synchronizing the Latin variant.
- Initial destination files came from the corresponding source locales and may still contain Czech, Ukrainian or English starting material. Determine their current content, not their language from the folder name. A destination can be much smaller than English; do not assume runtime fallback covers missing records.
- Use the pre-edit state when reviewing a change. Separate pre-existing defects from introduced ones and avoid attributing the initial state to the current edit.

## Technical checks

- Read raw bytes to verify encoding, BOM and line endings. Inspected UCS files use UTF-16 LE with BOM and CRLF; flag unintended conversion to UTF-8 or damage to the final newline.
- Parse numeric ID, first tab and value without dropping empty values or non-record lines. Detect duplicates before creating lookups. Compare IDs per corresponding file; report missing, additional and duplicate IDs separately. Additional IDs need investigation, not automatic deletion.
- Compare edited records' IDs, order, delimiters and out-of-scope text against the previous state. Ensure new English IDs were inserted without overwriting existing translations or introducing extra physical lines or separators.
- Check complete placeholders and references, including `%1PLAYERNAME%`, `%2CHATMESSAGE%` and `$9506`, for exact spelling, case and multiplicity against English and the prior state. Distinguish ordinary percentages from tokens. Check encountered escapes, paths and markup without treating UCS as Gladius XML.
- For a release/package review, verify that replacement paths match the chosen locale slots under `Engine/Locale/`, with no accidental extra version directory at the game destination. Confirm installation instructions cover backup and restoration if those instructions are in scope. Do not equate a correct package layout with tested installation or font coverage.

## Language and completeness

- Check meaning against English, including quantities, conditions, negation, upgrades, bonuses and penalties. Use other languages only to investigate possible renderings, then resolve them against English.
- Search complete phrases in both `dow 1 de/слоўнік dow.txt` and the root `слоўнік warhammer 40k.txt`. Check game terminology in the former and lore terms in the latter; distinguish correct inflection from conflicting terminology. Use the root `тарашкевіца.txt` and `асаблівасці.txt` for orthography and faction voice.
- Assess existing Latin-script text against the user's supplied conventions or prepared counterpart. If these are unavailable, report the limit rather than inventing a conversion system or treating Czech orthography as Belarusian Latin.
- Unchanged English, Latin letters or a difference from a source locale is only a review signal. Exclude technical-only values, legitimate names and intentionally empty records before judging translation status. Clearly distinguish missing IDs, untranslated values and incorrect Belarusian text.
- Define the counting unit and exclusions before reporting completeness. Neither ID coverage nor the number of values that differ from English measures translation quality. Do not update percentages from a partial review.

For each finding, give the file, numeric ID, problem and suggested correction. Prioritize broken format or meaning, then terminology and style. State the version, script, checks and limitations, including any unknown English version or missing in-game validation.
