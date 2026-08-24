---
id: TOOL_how-to-generate-captions-from-srt-files-using-remotion-for-reels
aliases: []
tags: []
---

For future videos, you have a few easy options:

1. **The Overwrite Method**: Just name your new files untitled.mp4 and untitled_reels.srt and drop them into the public folder to replace the old ones. The project will automatically pick them up, and you can just run npx remotion render SplitSubtitleScene out.mp4.

2. The Symlink Method: If you want to keep your videos in another folder, you can create a "symlink" (a shortcut) inside the public folder that points to your other directories.

3. Just Ask Me: If you have a new video in another folder, you can always just ask me to "Apply the DanielDalen caption style to the video at /path/to/video.mp4," and I will automatically handle copying the files into the right folder and rendering it for you!
