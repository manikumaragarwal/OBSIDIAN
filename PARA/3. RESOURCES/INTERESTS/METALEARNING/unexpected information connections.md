---
id: unexpected information connections
aliases: []
tags: []
---

- Claude Shannon- Father of Information Theory
  - _Mathematical theory of communication_
- Found out, how to measure information. (how unpredictable or surprising a message is.)

---

> "surprise" -> Information.

    - **More unlikely = more surprise = more information**

- Message that change your expectations carry more information.
- prediction algorithms _use entropy_ to measure how uncertain they are.

---

Perfect, let’s make this “surprise = information” thing less like a math lecture and more like something you’d actually bump into in life.

---

### 1. **Texting**

- If you text your friend:  
   **“I’m at the library.”**  
   → Not surprising, they already know you’re always studying. Low information.
- If you text:  
   **“I just saw a goat in the library.”**  
   → Surprising! That’s high information because it changes their mental picture of reality.

Shannon’s point: messages that _change your expectations_ carry more information.

---

### 2. **Typing & Autocorrect**

c

- Your keyboard predicts the next word you’ll type.
  - If you type “Happy”, the next word is often “Birthday”. Predictable = low surprise = less information.
  - If you type “Happy mitochondria”, that’s rare = high surprise = high information.

The prediction algorithms _use entropy_ to measure how uncertain they are.

---

### 3. **Movies & Spoilers**

- Imagine watching a murder mystery.
  - If it’s obvious who the killer is from the first scene, entropy is low → boring.
  - If every scene keeps you guessing, entropy is higher → engaging.
- Spoilers reduce surprise, so they also reduce information for you.

---

### 4. **Compression (WhatsApp, YouTube, ZIP files)**

- WhatsApp doesn’t literally send your entire text pixel by pixel. It looks at what’s _predictable_.
  - Example: In English, the letter “q” is almost always followed by “u”.
  - Since “u” after “q” is not surprising, it doesn’t need to waste extra storage.
- By removing predictable stuff, apps compress data → faster sending.

Entropy = the _theoretical limit_ of how much you can compress.

---

### 5. **Passwords**

- Password “aaaaaa” → super predictable, low entropy.
- Password “x9!pQ2&z” → very unpredictable, high entropy.  
   High entropy means harder to guess → more secure.

---

### 6. **Fair vs. unfair coin (in human terms)**

- Toss a fair coin → you really don’t know, so each result surprises you → 1 “bit” of information.
- Toss a biased coin (90% heads) → most of the time you _already knew_ it’d be heads. So only when tails shows up, you’re surprised. Average info is lower.

This is exactly how Shannon quantified uncertainty.

---

> So, why is this important?  
> Because the _entire internet_ runs on this. Your phone calls, memes, YouTube streams, even the security of your bank app — all rely on measuring and handling **information as surprise**. Without Shannon’s entropy, we’d still be sending smoke signals.
