# JLPT Kanji Compounds

A study app for JLPT kanji (N5 to N1). Pick a level, open a kanji, and see its readings, stroke order and the compound words built from JLPT kanji, with the reading of each kanji highlighted (on'yomi in teal, kun'yomi in amber).

## Features

- 2,211 JLPT kanji across N5–N1, with meanings, on'yomi and kun'yomi
- 16,000+ words, filtered to words whose every kanji is on a JLPT list
- Words ordered by real-world frequency, 10 per page
- Furigana split per kanji, with the studied kanji's reading highlighted
- Filter words by reading, word type and the highest level of kanji they contain
- Animated stroke order
- Resizable three-pane layout (drag the dividers; double-click to reset)
- Flashcards, learned progress (saved in your browser), zoom, keyboard shortcuts
- Audio uses your device's Japanese voice

## Run locally

The page loads its data with `fetch`, so serve the folder instead of opening the file directly:

```
python -m http.server 8000
```

Then open http://localhost:8000.

## Keyboard

`/` search · `←` `→` previous/next kanji · `P` flashcards · `Ctrl` `+`/`−` zoom

## Data and licences

- Words: [JMdict](https://www.edrdg.org/jmdict/j_jmdict.html) by the Electronic Dictionary Research and Development Group, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- JLPT vocabulary levels: [open-anki-jlpt-decks](https://github.com/jamsinclair/open-anki-jlpt-decks)
- Kanji data and JLPT kanji levels: [kanji-data](https://github.com/davidluzgouveia/kanji-data), based on Jonathan Waller's JLPT lists and KANJIDIC
- Word frequency: [wordfreq](https://github.com/rspeer/wordfreq) by Robyn Speer (Wikipedia, subtitles, news, books, web text; data CC BY-SA 4.0), with JMdict's newspaper frequency bands for words the corpus splits apart
- Stroke order: [KanjiVG](https://kanjivg.tagaini.net/) by Ulrich Apel, [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

The data files (`words.json`, `kanji.json`, `strokes.json`) are derived from these sources and are shared under the same CC BY-SA terms.
