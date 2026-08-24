# Caption Generator Usage Guide

This guide explains how to use the updated [generate_reel_captions.py](file:///home/manish/Videos/reels/generate_reel_captions.py) script to generate word-level SRT subtitles with character constraints (perfect for Instagram Reels and Shorts).

---

## 1. Character-Based Subtitle Splitting (Default)

By default, the script now automatically groups words together into subtitle lines such that the total length of the line (including spaces) is **at most 15 characters**.

### How to Run:
```bash
./venv/bin/python3 generate_reel_captions.py <path_to_audio_or_video>
```
* **Example**: `./venv/bin/python3 generate_reel_captions.py input.mp4`
* This creates a subtitle file `input_reels.srt` in the same directory.
* If a word is 15 or more characters long, it gets placed on its own line.
* If multiple words fit within 15 characters, they are grouped onto the same line.

### Changing the Character Limit:
You can specify a different character limit using the `--max_chars` flag:
```bash
./venv/bin/python3 generate_reel_captions.py <path_to_audio_or_video> --max_chars 20
```

---

## 2. Word-Based Subtitle Splitting (Optional)

If you want to revert to the old behavior where subtitles are grouped by a specific number of words per line (ignoring character counts), use the `--words` argument:

```bash
./venv/bin/python3 generate_reel_captions.py <path_to_audio_or_video> --words 2
```
* This will group words in chunks of exactly 2 words per subtitle block.

---

## 3. Example Command with Templates (Kdenlive integration)

If you are using the Kdenlive title generation integration:
```bash
./venv/bin/python3 generate_reel_captions.py input.mp4 --template my-custom-template.kdenlivetitle
```
This will:
1. Generate the character-constrained SRT file.
2. Auto-generate `.kdenlivetitle` files in a folder named `input_reels_Titles/` utilizing the configured visual style template.
