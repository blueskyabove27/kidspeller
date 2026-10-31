# kidspeller

A standalone spelling quiz for children ages 8–11. Everything runs in a single HTML file using Chrome's built-in text-to-speech API; no installation, server, internet connection, or external libraries are required.

## Run

1. Open `index.html` in Google Chrome (double-click a downloaded copy or use File → Open File).
2. Choose a word level (age 8, 9, 10, or 11).
3. Set the delay between the sentence and spelling reveal (default: 20 seconds; 1–180 seconds).
4. Adjust the voice speed (0.50×–1.00×) and press **Play**.
5. Use **Pause** and **Resume** to stop and continue speaking and waiting.

## Quiz sequence

1. Speak a word.
2. Wait 1.6 seconds.
3. Speak a short sentence containing that word.
4. Wait for the configured thinking time.
5. Speak each letter slowly while revealing it on screen.
6. Hold the spelling for 3 seconds, clear it, say “Next word,” and repeat.

Word choices are shuffled within the selected age level. The browser's installed English voices determine the sound of the speech.
