# kidspeller

A standalone spelling quiz for children ages 8–11. Everything runs in one `index.html` file using Chrome's built-in text-to-speech API; no installation, server, account, internet connection, or external libraries are needed.

## Run

1. Open `index.html` in Google Chrome (double-click a downloaded copy or use File → Open File).
2. Choose a word level: age **8**, **9**, **10**, or **11**.
3. Choose a numbered **word list (1–20)**. Each age has 20 fixed lists of exactly 40 words, or 800 distinct words per age.
4. Set the spelling delay (default **20 seconds**, adjustable from 1 to 180 seconds).
5. Set the voice speed (**0.50×–1.00×**) and press **Play**. Use **Pause**/**Resume** to freeze and continue the quiz.

## Spoken quiz sequence

For each word, the screen shows **List N · Word X of 40** and Chrome announces **“Word number 1 is…”** for the first word, or **“Next word, number 5 is…”** for later words.

1. Say the question number and the spelling word without displaying the answer.
2. Wait **1.6 seconds**, then say a short sentence containing the word.
3. Wait the configured thinking period.
4. Slowly speak the letters, revealing each letter on screen.
5. Show the completed spelling for **3 seconds**, clear it, and introduce the next numbered word.
6. After word **40**, display **List complete** and stop. Press Play to restart that list.

Words are asked in **fixed list order**, so the spoken number corresponds to the selected list's actual word number. Changing age or list while a quiz is in progress takes effect after the current word; numbering restarts at 1. The age levels are approximate vocabulary difficulty groupings. The English voice used is the one available in your Chrome installation.

## Word data

The lists include the original hand-authored spelling words and are expanded with common English vocabulary selected from the public [Google 10,000 English words frequency list](https://github.com/first20hours/google-10000-english). Commonly unsuitable terms are filtered out. All list data and example-sentence fallbacks are bundled directly into the HTML file for offline use.
