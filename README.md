# Wordle Mini Game

A complete Wordle-style mini-game built in a single `index.html` file.

## How to Play

1. Open `index.html` in any modern web browser.
2. Guess the hidden 5-letter word in 6 attempts or fewer.
3. Type with your physical keyboard or use the on-screen keyboard.
4. Press `Enter` to submit a guess.
5. Press `Backspace` or `Del` to remove a letter.
6. Use `Restart` to start a new game.

## Tile Colors

- Green means the letter is correct and in the correct position.
- Yellow means the letter is in the word but in the wrong position.
- Gray means the letter is not in the word.

## Implementation Notes

- The game uses only HTML, CSS, and JavaScript.
- All code lives inside `index.html`.
- There are no external libraries, npm packages, backend services, or databases.
- Duplicate letters are scored with a two-pass algorithm so repeated letters are handled correctly.
