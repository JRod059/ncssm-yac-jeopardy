# YAC Jeopardy

A Jeopardy-style trivia game for the NCSSM Young Alumni Council. One facilitator runs it on a shared screen at events; players just watch and answer.

## Play it

- **From the link:** open the project's GitHub Pages address (shown under Settings → Pages in this repository).
- **From the file:** download `yac-jeopardy.html` and double-click it. It opens in any browser and needs no install.

The "NCSSM Jeopardy!" board is built in. Boards you create or edit are saved in your own browser, so use **Export** to send a board to someone else and **Import** to load one you were sent.

## How a round works

1. Pick a board and press **Play**, then set the teams and the timer length.
2. Click a square to show the clue. Press **Start timer** once the teams have read it.
3. Press **Reveal answer**, then choose what happened: the team got it, another team stole it, or no one scored.
4. Click any score to type a correction. **Undo** reverses the last outcome.

Keyboard: `Space` reveals the answer, `T` starts or pauses the timer, `Esc` goes back to the board.

## Editing the app

Everything is in one file, `yac-jeopardy.html`: styles, code and the starter board. `index.html` only forwards the GitHub Pages address to it. `PLANNING.md` records the decisions behind the app and a build log.

Changes pushed to the `main` branch appear at the link a minute or two later.
