---
id: how-to-run-the-auto-subtitle-or-caption-cli-tool
aliases: []
tags: []
---

TAGS: [[content-creation]]

Here is a quick reference guide on how to use your
generate_reel_captions.py tool.

### 1. Before you run it

Since your whisper library is installed inside a virtual
environment, you must activate it every time you open a new
terminal:

```bash
source venv/bin/activate
```

(You'll know it worked when your terminal prompt has (venv) at the
beginning).

### 2. Basic Usage (Generates .srt only)

If you just want the raw .srt subtitle file:

```bash
  python generate_reel_captions.py "YourVideoFile.mp4"
```

### 3. Full Usage (Generates .srt AND Kdenlive titles)

To automatically create styling clips for Kdenlive, you must provide
your .kdenlivetitle template file. You can also specify the
framerate to ensure the titles align properly with your video:

```shell
 python generate_reel_captions.py "YourVideoFile.mp4" --template "my_template.kdenlivetitle" --fps 30
```

> [!NOTE] Make sure only use the templates available

### 4. Optional Customization Flags

You can tweak the generation by adding any of these flags to your command:

- `--words <number>` : Change the number of words per caption line
  (default is 1 for Reels).
- `--model <size>` : Pick the Whisper AI model size: tiny , base
  (default), small , medium , large .
- `--color1 <hex>` : Override your Kdenlive template's font color (e.g., --color1 FFFF00 for yellow).
- --custom_y <number> : Move your subtitles up or down (distance in pixels from the top of the screen).


![1784315472.png](assets/imgs/1784315472.png)



