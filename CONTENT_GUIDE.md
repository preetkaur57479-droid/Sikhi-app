# Adding verified Gurbani content

Do not place unverified or generated Gurbani in the app.

For each Bani/section, supply:
- stable `id`
- exact title
- Gurmukhi text copied from a verified source
- source name and URL/reference
- ang/page/section reference where applicable
- attribution and license/permission details
- reviewer and verification date

Keep Unicode text in UTF-8. Preserve the source's line breaks and formatting. If multiple display formats are needed (larivaar and pad-ched), store them as separate explicitly named fields rather than silently transforming one into the other.

Translations and transliterations must be separately sourced and attributed. Audio requires its own permission record.

## Punjabi, English and Hindi meanings

The reader supports three separate meaning-language choices: Punjabi (`pa`), English (`en`) and Hindi (`hi`). Keep the original Gurmukhi text as its own field. Do not overwrite or replace it with a translation.

For every language meaning, record:
- the complete text in that language
- source and exact edition/page/URL reference
- translator or author attribution
- licence or written permission for reuse
- reviewer and verification date
- a `verified` status that is true only after a human review against the cited source

Do not machine-translate a meaning and label it verified. Do not assume that permission for a Gurmukhi transcription also grants permission to reuse a translation, commentary, scan or audio recording. A missing language pack should be shown as unavailable, not filled with generated text.


## Three Granth library entries

The app currently registers these as separate collections: Sri Dasam Granth Sahib Ji (user-shared Giani Narain Singh Ji Complete Steek reference), Sri Sarbloh Granth Sahib Ji (user-shared Sunpuran Steek reference), and Sri Gur Pratap Suraj Granth Sahib Ji (user-shared source link). The Google share links have not yet been resolved and their PDFs have not been inspected. The library UI therefore provides source links and edition notes, not a claim that full text is installed.

For Suraj Prakash, do not mark converted Unicode or machine-translated meanings as verified without checking them against the chosen printed edition. For every Granth, record volume/part, publication details, page/section, translator/teekakar, attribution, and reuse permission. Punjabi (`pa`), English (`en`) and Hindi (`hi`) are supported as language choices; missing translations must remain clearly unavailable.
