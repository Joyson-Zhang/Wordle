# Wordle Mini Games

A small collection of Wordle-style browser games built with plain HTML, CSS, and JavaScript.

No build step, no dependencies, no server, and no database. Open either HTML file directly in a modern browser and play.

## Games

### Single-Player Wordle

Open `index.html` to play the original solo version.

- One hidden 5-letter word
- 6 guesses
- Physical keyboard support
- On-screen keyboard
- Restart button
- Tile colors and keyboard colors update after each guess

### Two-Player Wordle

Open `two-player.html` to play the turn-based two-player version.

- Two players guess the same hidden 5-letter word
- Players take turns making one guess at a time
- Each player gets 6 guesses
- The first player to guess correctly wins
- If both players run out of guesses, the answer is revealed
- Each turn has a 30-second timer, and timing out costs one guess
- Each player has a separate board and on-screen keyboard
- Keyboard color hints are shared, so both players can use clues from every guess

## How to Play

1. Double-click `index.html` or `two-player.html`.
2. Type a 5-letter guess with your physical keyboard or the on-screen keyboard.
3. Press `Enter` to submit.
4. Press `Backspace` or `Del` to remove a letter.
5. Use `Restart` to start a new game.

## Tile Colors

- Green: the letter is correct and in the correct position.
- Yellow: the letter is in the word but in the wrong position.
- Gray: the letter is not in the word.

## Implementation Notes

- All HTML, CSS, and JavaScript are kept inside the HTML files.
- The games use a predefined list of 5-letter words.
- Duplicate letters are handled with a two-pass scoring algorithm:
  - First mark exact matches as green.
  - Count the remaining unmatched letters in the answer.
  - Mark yellow only when a guessed letter still exists in the remaining unmatched letters.
  - Mark all other letters gray.
