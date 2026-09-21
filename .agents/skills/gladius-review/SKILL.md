---
name: gladius-review
description: Review this project's Belarusian Gladius translation for terminology and language errors, missing entries, damaged placeholders and game markup. Use for audits, proofreading or reviewing translation changes.
---

# Review the Gladius translation

Read the project root `AGENTS.md`. Select the latest existing version by numeric comparison and use the scope requested by the user. For a review request, report findings; when asked to fix errors, make targeted corrections within that scope. Report in Belarusian unless requested otherwise.

## Technical checks

- Compare the full sequence of embedded tags for each changed `entry name` with its previous state, not merely the tag count. Spelling, attributes, case, whitespace and apostrophes must match unless markup repair is part of the task. Check that translated formatted spans remain between the appropriate style tags and that `<br/><br/>` preserves paragraph boundaries.
- Do not treat the first `/>` as the end of an `entry`: embedded tags inside `value` use the same ending. Verify all keys, their order, entries outside the requested scope and the file's outer structure. Check for stray characters after the final `/>` separately from the value's translation.
- Match English originals and translations by `entry name`. Report missing keys, additional keys and duplicates separately. Local language settings may have no English counterpart; that alone is not an error.
- Check the number of occurrences of every placeholder, such as `%1%`; their order in a sentence may differ. Check technical tags, paths and attributes: `GUI/Yellow` and `GUI / Yellow` are different technical strings.
- Check for unclosed quotes, damaged entry boundaries, accidentally translated keys, `...Count` counters and entries marked `Do not translate!`.
- Do not use strict XML validity as the acceptance criterion for language files: they contain literal tags inside attributes. If parsing is needed, handle this dialect without rewriting originals. Strict XML validation is appropriate for ordinary XML configuration files.
- For SRT, compare cue numbers, timestamps and block boundaries. When a review explicitly covers both script variants, match them by keys or subtitle cues, not by file line positions. Reviewing the Latin variant does not authorize generating or synchronizing it.

## Language checks

- Check terminology against `слоўнік.txt`, faction voices against `асаблівасці.txt`, and spelling against `тарашкевіца.txt`. For explicitly requested review of existing Latin-script text, consult `лацінка.txt` and existing counterparts as reference material. Do not independently romanize text or derive a conversion system from examples.
- Verify gameplay conditions, quantities, negation, units and bonuses. Distinguish errors of meaning from optional stylistic improvements.
- An unchanged English value or the presence of Latin letters is a candidate for review, not proof of missing translation. Exclude model codes, proper names, Latin-language phrases, technical values and `Do not translate!` entries.
- Do not treat percentages in `спіс перакладзеных файлаў.txt` as audit results. When measuring completeness, define the counting unit and exclusions. Counting values that differ from English does not measure translation quality.

## Report

For each significant finding, provide the file, `entry name` or subtitle cue number, the issue and a suggested correction. Prioritize damage to format or meaning, followed by terminology and style. Distinguish pre-existing issues from newly introduced ones when a baseline is available. If the English baseline for the relevant version is missing, explain the limits of conclusions about completeness and currency. Do not turn Latin synchronization into an automatic next step after a Cyrillic review.
