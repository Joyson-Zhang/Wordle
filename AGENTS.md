Create a complete Wordle-style mini-game in a single index.html file.

Requirements:
- Use only HTML, CSS, and JavaScript.
- Put all HTML, CSS, and JavaScript in one file.
- The game should run by double-clicking index.html in a browser.
- Do not use external libraries, npm, React, backend, or database.

Game rules:
- The game randomly chooses one hidden 5-letter word from a small predefined word list.
- The player has 6 attempts to guess the word.
- Each guess must be exactly 5 letters.
- After each guess, color each tile:
  - Green if the letter is correct and in the correct position.
  - Yellow if the letter is in the word but in the wrong position.
  - Gray if the letter is not in the word.
- Handle duplicate letters correctly using a two-pass algorithm:
  1. First mark exact matches as green.
  2. Track remaining unmatched letters in the answer.
  3. Then mark yellow only if the guessed letter still exists in the remaining unmatched letters.
  4. Otherwise mark gray.

Interface requirements:
- Show a 6-row by 5-column game board.
- Allow typing letters with the physical keyboard.
- Support Enter to submit a guess.
- Support Backspace to delete a letter.
- Show messages such as "Not enough letters", "You won", and "Game over".
- Reveal the answer after losing.
- Add a Restart button.
- Make the design clean and readable.

Optional, only if easy:
- Add an on-screen keyboard.
- Update keyboard colors based on feedback.
- Add simple tile flip animation.

Please generate the full index.html file.
