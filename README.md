# Qualtinger – 15 Puzzle

A browser-based 15-puzzle (sliding tile game) using a portrait of Helmut Qualtinger as the puzzle image, with *Krüppellied* playing in the background.

## How to play

- Click any tile in the same row or column as the red empty field — all tiles between slide at once
- Reassemble the portrait to win
- **Mischen** — shuffle the board
- **Lösung** — reset to solved state

## Run locally

```
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080).

## Files

| File | Description |
|------|-------------|
| `index.html` | Complete app — game logic, styles, markup |
| `qualtingerportraet.5005575.jpg` | Puzzle image (Qualtinger portrait) |
| `Krüppellied.mp3` | Background music, starts on first click |