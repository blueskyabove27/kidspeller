# kidspeller

A standalone spoken spelling quiz for children ages 8–11. The entire app, including its vocabulary, runs from a single `index.html` file in Chrome—no build step, server, or external JavaScript libraries.

## Run

1. Download `index.html` and open it in Google Chrome, or open it from the repository.
2. Choose a word level: **8**, **9**, **10**, or **11** years old.
3. Select a **word list from 1–30**. Every age has **30 fixed lists of 30 words** (900 unique words per age, 3,600 total).
4. Set **Answer timing**:
   - **Countdown (seconds)**: reveal the answer after a configurable delay (20 seconds by default, 1–180 seconds).
   - **Listen for “I’m done”**: listen for the learner to say **“I'm done”** after the example sentence. No countdown is used. Alternatively, press the **I'm done — reveal spelling** button.
5. Adjust **Voice speed** (0.50×–1.00×) for each word and example sentence.
6. Adjust **Pause between letters** (0.10–2.00 seconds, default 0.26 seconds) to control **only the silent gap** between spoken letters. Letter pronunciation and speech rate stay unchanged by this control.
7. Press **Play** to begin, **Pause** to stop, and **Resume** to continue.

## Question sequence

For each word, the screen shows **List N · Word X of 30**. Chrome announces **“Word number 1 is…”** for the first word, or **“Next word, number 5 is…”** for later words.

1. Say the question number and spelling word while keeping the spelling hidden.
2. Wait **1.6 seconds**, then say a short sentence containing the word.
3. Wait for either the configured countdown or **“I'm done”** (Listen mode).
4. Speak and reveal the word **letter by letter** at the original spoken-letter rate, leaving the selected pause between letters.
5. Hold the complete spelling on screen for **3 seconds**, clear it, then advance.
6. After **word 30**, show **List complete** and stop. Play restarts the current list.

Words stay in a fixed order within each list, so the spoken word number is stable. Changing the age or list during playback takes effect after the current question and resets numbering to 1. Mode changes during the current question take effect when the following question begins.

## Chrome audio and microphone notes

- **Timed mode** can run offline if Chrome has an available local text-to-speech voice.
- **Listen mode** uses Chrome's `SpeechRecognition` or `webkitSpeechRecognition` API. Grant microphone permission when requested. Depending on Chrome and your platform, recognition **may require internet access**.
- The microphone starts listening **only after the example sentence finishes**, and stops on **Pause**, when the answer is revealed, or when the recognition session is stopped.
- If speech recognition is unsupported, blocked, or unavailable, the quiz remains in Listen mode and the **I'm done — reveal spelling** button lets you proceed without waiting for a timer.
- Use Chrome on a supported platform and allow microphone permission. System speech voices determine exact audio quality and pronunciation.

## Vocabulary

All lists are embedded in `index.html`. The original example sentences are retained for the original hand-written words; additional words receive a short fallback sentence that contains the word. The banks were expanded with a filtered selection from the public [Google 10,000 English words frequency list](https://github.com/first20hours/google-10000-english). Age levels are approximate vocabulary difficulty categories.
