---
id: 15th-july-audio-epub-system-detailed-nerding-out
aliases: []
tags: []
---

whispersync is a paid tool by amazon, which highlight the part of the e-book, that is being spoken in the audiobook.

here's how I building it for FREE.. and without using AI. [fingers pointing meme]

- **This is a pipeline, which helps us create an epub3 file, with the audiobook as an media overlay.**

under the hood... this is an orchestration of few opensource engines and packages..

The process can be divided into three parts :

1. [[Forced Alignment]] : this was the hardest as well as the most satisfying process.

- we use Text-To-SPeech to map every chunk of text with a Audio.. this audio is almost unbearable.. but it will do..

- [ ] now we have some idea, roughly what kind of frequency every chunk of text makes..

- Now, we will use our **dynamic time warping algorithm**... it's just a name, but what it does is... it handles [[***temporal variance***]]
  meaning... it stretches and compresses the time of sound.. to match the wavelengths.... and once the wavelengths are matched..
  [btw, this same principal is used in video editing apps to match 2 soundtracks. ]

- it prooves that the audio is supposed to be played at this time chunk...

2. ID MAPPING...
   this is simply mapping the timeline of our audiobook to each text chunk...
   (_example: kisi text chunk ko pata chalega, that ussey audiobook ke 0.1 second se 0.4 second tak audio play karni hai_)

3. SMIL overlays..

- once we have every text chunk, mapped with the timeline of the audiobook.. we can create SMIL files (synchronized multimedia integratoin language.)
- we use [[syncabook]] engine to convert the timing data into SMIL files....

### EPUB3

finally our EPUB3 file is generated... which contains 3 things..

1. XHTML FILES (text chunks with id's )
2. MP3/WAV files (raw audiobook tracks)
3. SMIL files (maps text IDs to audio timestamps)
