---
id: how-to-enhance-the-audio-in-cli-for-content-creation
aliases:
  - how-to-enhance-the-audio-in-cli-for-content-creation
tags: []
---

Tags: [[content-creation]]

# how-to-enhance-the-audio-in-cli-for-content-creation

## Goal Description

You requested to learn exactly what commands to run to enhance your audio. This guide is broken down into two parts:

1. **The Automated Way**: The single command you need to run using the script we built.
2. **The Manual Way (Under the Hood)**: The exact raw terminal commands the script runs behind the scenes, so you can learn how the AI noise reduction and FFmpeg studio filters actually work.

## User Review Required

Please review this guide. Let me know if you want me to explain any specific audio filter (like the compressor or equalizer) in more detail!

---

## 1. The Automated Way (Recommended)

Since we already built the `enhance.sh` script, you don't need to memorize complex commands. The script handles the extraction, AI processing, EQ filtering, and video muxing all at once.

**Command:**

```bash
cd ~/Videos/reels
./enhance.sh "your_file_name.mp4"
```

_Note: This works for both video files (`.mp4`, `.mkv`) and audio files (`.m4a`, `.mp3`). It will automatically spit out a new file named `your_file_name_enhanced.mp4`._

---

## 2. The Manual Way (Under the Hood)

If you want to run the process manually step-by-step (or tweak the parameters yourself directly in the terminal), here are the exactly commands you would run.

### Step 1: Extract Audio for the AI

DeepFilterNet requires uncompressed WAV audio at exactly 48kHz. This command strips the audio from your video and converts it:

```bash
ffmpeg -i "input.mp4" -vn -c:a pcm_s16le -ar 48000 "temp.wav"
```

- `-vn`: Removes the video track.
- `-c:a pcm_s16le`: Converts to 16-bit uncompressed WAV.
- `-ar 48000`: Sets the sample rate to 48kHz.

### Step 2: AI Noise Reduction

We push the WAV file through the DeepFilterNet AI model (using the virtual environment we set up). This strips out background hiss, fans, and room echo.

```bash
~/Videos/reels/venv/bin/deepFilter "temp.wav" -o .
```

_This will generate a deeply cleaned audio file named something like `temp_DeepFilterNet3.wav` in your current folder._

### Step 3: Studio Filters & Muxing

This is the "magic" FFmpeg command that applies the parametric EQ, compression, and loudness normalization, and stitches it back to your original video.

```bash
ffmpeg -i "input.mp4" -i "temp_DeepFilterNet3.wav" \
  -map 0:v -map 1:a \
  -c:v copy \
  -af "anequalizer=c0 f=100 w=200 g=6 t=1|c1 f=100 w=200 g=6 t=1|c0 f=4000 w=2000 g=3 t=1|c1 f=4000 w=2000 g=3 t=1,acompressor=threshold=-15dB:ratio=3:attack=5:release=50:makeup=3dB,loudnorm=I=-16:TP=-1.5:LRA=11" \
  -c:a aac -b:a 256k \
  "output_enhanced.mp4"
```

**What the filters (`-af`) are doing:**

- **`anequalizer`**: We are boosting 100Hz (bass) by `6dB` for that deep radio voice, and boosting 4000Hz (treble) by `3dB` for crispness.
- **`acompressor`**: Squashes the dynamic range. Anything louder than `-15dB` gets compressed at a `3:1` ratio, making quiet parts easier to hear.
- **`loudnorm`**: A broadcast-standard filter that analyzes the whole track and forces the final output to perfectly hit `-16 LUFS` (the standard loudness for podcasts and YouTube).
- **`-c:v copy`**: Copies the video frames exactly as they were, so you don't lose any video quality!
