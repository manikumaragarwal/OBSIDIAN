08-02-2026 02:42

Status: #Completed
Tags: [[Artificial Intelligence (AI)]] [[CODING]] 


# LLM under the HOOD
### **1. The LLM Ecosystem (2025)**

- **Major Players:** While **ChatGPT (OpenAI)** is the "Original Gangster" and most feature-rich incumbent, several other powerful models exist, including **Gemini (Google)**, **Claude (Anthropic)**, **Co-pilot (Microsoft)**, **Grok (xAI)**, **DeepSeek (Chinese)**, and **Mistral (French)**.
- **Tracking Performance:** Leaderboards like **Chatbot Arena** (LMSYS) and **Scale AI’s SEAL Leaderboard** are essential for tracking the *ELO scores* and relative strengths of various models.
- **Pricing Tiers:** Companies typically offer free, plus, and pro tiers. Higher tiers (like ChatGPT Pro at $200/month) provide access to the most powerful reasoning models and features like **Deep Research**.

### **2. Core Technical Concepts**

- **Tokens:** LLMs do not see text directly; they process **tokens**, which are small chunks of text. A typical vocabulary consists of roughly 200,000 possible tokens.
- **The Context Window:** This is the **"working memory"** of the model. Any information within this window is directly accessible, but tokens here are "precious resources" because they are computationally expensive and can distract the model if they are irrelevant.
- **Training Stages:**
    - **Pre-training:** A costly, months-long process where the internet is "compressed" into a probabilistic **one-terabyte "zip file"** (neural network parameters). This leads to a **knowledge cutoff**, meaning the model only knows what happened up to its training date.
    - **Post-training:** The stage where human labelers program the model’s **personality and style** (e.g., an assistant) and refine its reasoning through *reinforcement learning*.

### **3. "Thinking" Models (Reasoning)**

- **Mechanics:** These models (e.g., OpenAI's **o1/o3**, DeepSeek **R1**) are trained via **reinforcement learning** to practice problem-solving strategies.
- **Capabilities:** They use an **inner monologue** to backtrack, revisit assumptions, and think through hard problems in **math and code**.
- **Trade-offs:** They can take several minutes to "think" as they emit thousands of tokens internally before responding, but they offer significantly higher accuracy for complex tasks.

### **4. Advanced Tool Integration**

- **Internet Search:** Essential for bypassing knowledge cutoffs and finding recent or esoteric information. Tools like **Perplexity** or ChatGPT's search button automate browsing and pull web content directly into the context window for the model to reference.
- **Deep Research:** A newer capability that combines internet search and thinking over an extended period (up to 10–20 minutes) to produce a **comprehensive report with citations**. It is best used for complex product comparisons or deep dives into niche topics.
- **Python Interpreter:** LLMs can write and execute computer programs to perform **exact math** or generate **data visualizations** (plots and charts).

### **5. Practical Application Workflows**

- **Reading Companion:** Uploading PDFs or pasting book chapters (e.g., _The Wealth of Nations_) allows you to **read "together"** with the LLM, asking for summaries and clarifications to increase retention.
- **Professional Coding:** Rather than using a browser, professional developers use apps like **Cursor** or **Windsurf** that have access to the local file system.
    - **"Vibe Coding":** A term for letting an autonomous agent (like Cursor's **Composer**) edit across multiple files based on high-level commands while the human supervises.
- **Custom GPTs:** These are "saved prompts" that reduce the need for repetitive instructions. Examples include **detailed translators** that break down grammar or OCR tools that translate text from screenshots.

### **6. Multimodality (Audio, Image, Video)**

- **Voice Interactions:**
    - **"Fake" Audio:** Using system-wide speech-to-text (like **Super Whisper**) to type queries faster.
    - **"True" Audio (Advanced Voice Mode):** Native audio handling where the model hears and speaks in audio tokens directly, allowing for nuances like singing, fast counting, or character voices (e.g., Yoda, Pirate).
- **Visual Input:** Using the camera or screenshots for **OCR and interpretation** of blood tests, nutrition labels, and memes.
- **Video Generation:** Rapidly evolving tools like **Sora**, **Luma**, and **Kling** can generate high-quality cinematic clips from text prompts.

### **7. Personalization and Quality of Life**

- **Memory:** ChatGPT can maintain a **database of your preferences** and identity across different chats. This is currently a unique feature to OpenAI.
- **Custom Instructions:** Global settings that allow you to define the model’s tone (e.g., "be educational," "don't be an HR partner") and provide context about yourself.
- **Chat Hygiene:** **Start new chats frequently** to clear the context window, which keeps the model fast and reduces the likelihood of hallucinations caused by "distraction" from past tokens.

---

_Note: The term "Vibe Coding" mentioned in these notes was specifically coined by the video's creator, Andrej Karpathy._

---
# **How Andrej Karpathy Utilises LLMs**

Andrej Karpathy uses a variety of Large Language Models (LLMs) as part of an **"LLM Council,"** often asking the same query to multiple models—such as ChatGPT, Claude, and Gemini—to compare their insights. His usage spans professional coding, personal learning, and daily productivity.

#### **1. Professional Coding and Data Analysis**

- **Vibe Coding:** Karpathy uses the term **"Vibe Coding"** to describe his professional workflow in apps like **Cursor** or Windsurf. Instead of writing every line of code, he uses an autonomous agent (Composer) to edit across multiple files based on high-level commands, such as building a Tic-Tac-Toe app with confetti effects.
- **Thinking Models for Debugging:** When stuck on complex programming bugs, such as a "gradient check" failure, he switches to **reasoning models** (like OpenAI’s o1 or DeepSeek R1). These models use an "inner monologue" to backtrack and revisit assumptions, often solving problems that standard models fail to grasp.
- **Advanced Data Analysis:** He employs the **Python Interpreter** to perform exact mathematics and generate data visualisations, though he notes that users must scrutinise the code for "sneaky" implicit assumptions.

#### **2. Learning and Reading Companion**

- **Active Reading:** Karpathy "reads together" with LLMs to increase retention. He uploads long documents, such as biology papers or chapters from Adam Smith's _The Wealth of Nations_, to ask for summaries and clarifications as he progresses through the text.
- **Conceptual Diagrams:** He uses Claude’s **Artifacts** feature to generate **mermaid diagrams** that map out the logical flow of book chapters, helping him visualise complex arguments spatially.

#### **3. Information Retrieval and "Deep Research"**

- **Internet Search:** For recent or esoteric information—like the release date of _White Lotus_ or specific stock movements—he uses tools like **Perplexity** or ChatGPT’s search function.
- **Deep Research:** For high-stakes comparisons, such as choosing a more private web browser or investigating the safety of longevity supplements, he uses **Deep Research** modes. These models spend 10–20 minutes browsing dozens of sources to produce a comprehensive report with citations.

#### **4. Customised Personal Tools**

- **Korean Language Learning:** Karpathy has built several **Custom GPTs** specifically for his Korean studies.
    - **Detailed Translator:** Provides part-by-part breakdowns of sentences, including nuances and slang.
    - **Vocabulary Extractor:** Formats words into semicolon-separated lists for easy import into flashcard apps like Anki.
    - **OCR for TV:** He takes screenshots of hard-coded subtitles from shows like _Single’s Inferno_ and pastes them into a GPT to have the text transcribed and translated instantly.

#### **5. Daily Productivity and Multimodality**

- **Voice over Typing:** He prefers **voice input** for efficiency, estimating that 80% of his mobile queries and 50% of his desktop queries are spoken. On desktop, he uses system-wide tools like **Super Whisper** to transcribe his speech into any app.
- **Visual Interpretation:** He uses the camera to interpret **blood test results**, check the safety of **toothpaste ingredients**, and explain the logic behind complex **internet memes**.
- **Knowledge Verification:** While he uses LLMs to check things like caffeine content or medication ingredients (e.g., DayQuil), he treats the output as a **probabilistic recollection** and verifies critical details against primary sources.

#### **6. Workflow Habits**

- **Chat Hygiene:** Karpathy recommends **starting new chats frequently**. This wipes the "context window," preventing the model from becoming distracted by irrelevant past tokens, which maintains accuracy and speed.
- **Custom Instructions:** He uses global settings to ensure his models are **educational and insightful** rather than sounding like an "HR business partner".

## References
https://youtu.be/EWvNQjAaOHw?si=ivM_H_QCIdw5Z7F0
