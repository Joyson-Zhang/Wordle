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

- Two players guess the same hidden word
- Word length can be set to 5 or 6 letters
- Turn time can be typed in from 5 to 300 seconds
- The match target can be set from 2 to 6 round wins
- Players take turns making one guess at a time
- Each player gets 6 guesses per round
- The first player to guess correctly wins the round
- The first player to reach the match target wins the match
- Draw rounds are recorded but do not add wins to either player
- If both players run out of guesses in a round, the answer is revealed
- Timing out costs one guess
- Each player has a separate board and on-screen keyboard
- Keyboard color hints are shared, so both players can use clues from every guess
- Round history records each round result, answer, and running score

## How to Play

1. Double-click `index.html` or `two-player.html`.
2. In `two-player.html`, set turn time, word length, and wins to match if desired.
3. Type a guess with your physical keyboard or the on-screen keyboard.
4. Press `Enter` to submit.
5. Press `Backspace` or `Del` to remove a letter.
6. Use `Restart` or `Apply / Restart Match` to start over.

## Tile Colors

- Green: the letter is correct and in the correct position.
- Yellow: the letter is in the word but in the wrong position.
- Gray: the letter is not in the word.

## Implementation Notes

- All HTML, CSS, and JavaScript are kept inside the HTML files.
- The games use predefined word lists.
- Duplicate letters are handled with a two-pass scoring algorithm:
  - First mark exact matches as green.
  - Count the remaining unmatched letters in the answer.
  - Mark yellow only when a guessed letter still exists in the remaining unmatched letters.
  - Mark all other letters gray.
