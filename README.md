# JLPT Kanji Compounds

A study app for JLPT kanji (N5 to N1). Pick a level, open a kanji, and see its readings, stroke order and the compound words built from JLPT kanji, with the reading of each kanji highlighted (on'yomi in teal, kun'yomi in amber).

## Features

- 2,211 JLPT kanji across N5–N1, with meanings, on'yomi and kun'yomi
- About 17,000 words, filtered to words whose every kanji is on a JLPT list; spellings, readings and meanings from JMdict's common-word set
- Words ordered by real-world frequency, 10 per page, or as compact furigana tiles grouped by reading
- Hide meanings (and readings) to test yourself
- Furigana split per kanji, with the studied kanji's reading highlighted
- Filter words by reading, word type and the highest level of kanji they contain
- Animated stroke order
- Light, dark or system theme
- Resizable three-pane layout (drag the dividers; double-click to reset); hide the menu with ☰ or Ctrl+B
- Daily review with spaced repetition (Again / Hard / Good / Easy) for kanji and for words you add, new kanji introduced in frequency order
- Quizzes: type the reading (romaji turns into kana as you type), pick the meaning, pick a kanji's reading inside a word, English → kanji with look-alike choices, and listening
- Parts of each kanji, other kanji built from the same part, and easily confused look-alikes
- Word detail pages: example sentences, each kanji's reading in the word, frequency, and more words with the same kanji
- Weak kanji: the kanji you forget in reviews or miss in quizzes, ready to practise
- Find kanji by parts: pick the parts you can see to narrow down any JLPT kanji
- Backup and restore your progress as a file or text
- Progress page: streak, daily goal, 30-day activity, per-level progress and what to study next
- Search by kanji, English meaning, kana or romaji (`shoku`), and by whole words (`先生`)
- Learned progress and review schedule saved in your browser, zoom, keyboard shortcuts
- Audio uses your device's Japanese voice

## Run locally

The page loads its data with `fetch`, so serve the folder instead of opening the file directly:

```
python -m http.server 8000
```

Then open http://localhost:8000.

## Keyboard

`/` search · `←` `→` previous/next kanji · `[` `]` word pages · `R` review · `Q` quiz · `Ctrl` `B` hide menu · `Ctrl` `+`/`−` zoom

## Data and licences

- Words: [JMdict](https://www.edrdg.org/jmdict/j_jmdict.html) (release 2026-11-04, common entries, vulgar and X-rated senses excluded) by the Electronic Dictionary Research and Development Group, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- JLPT vocabulary levels: [open-anki-jlpt-decks](https://github.com/jamsinclair/open-anki-jlpt-decks), attached only where the word and its reading both match JMdict
- Kanji data and JLPT kanji levels: [kanji-data](https://github.com/davidluzgouveia/kanji-data), based on Jonathan Waller's JLPT lists and KANJIDIC
- Word frequency: [wordfreq](https://github.com/rspeer/wordfreq) by Robyn Speer (Wikipedia, subtitles, news, books, web text; data CC BY-SA 4.0), with JMdict's newspaper frequency bands for words the corpus splits apart
- Kanji parts: [KRADFILE/RADKFILE](https://www.edrdg.org/krad/kradinf.html) by EDRDG, CC BY-SA 4.0; radical names from [Kanji alive](https://github.com/kanjialive/kanji-data-media), CC BY 4.0
- Look-alike kanji: [Lars Yencken's kanji confusion data](https://lars.yencken.org/datasets/kanji-confusion/), CC BY 3.0
- Example sentences: [Tatoeba](https://tatoeba.org), CC BY 2.0 FR, linked to word senses by EDRDG's JMdict_e_examp (CC BY-SA 4.0)
- Romaji to kana: [WanaKana](https://github.com/WaniKani/WanaKana), MIT
- Stroke order: [KanjiVG](https://kanjivg.tagaini.net/) by Ulrich Apel, [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

The data files (`words.json`, `kanji.json`, `strokes.json`, `parts.json`, `ex/*.json`) are derived from these sources and are shared under the same CC BY-SA terms.
