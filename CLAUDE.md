# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-page 15-puzzle (sliding tile game) built in vanilla HTML/CSS/JS. No build step, no dependencies.

## Files

- `index.html` — entire app (game logic, styles, markup)
- `qualtingerportraet.5005575.jpg` (472×315px) — portrait used as puzzle image
- `Krüppellied.mp3` — background music, starts on first user click

## Architecture

All logic lives in `index.html`:

- `tiles[]` — flat array of 16 values (1–15 = pieces, 0 = empty slot), index = board position
- `render()` — rebuilds the DOM grid from `tiles[]`; sets `background-size` and `background-position` per tile to show the correct image slice
- `tryMove(pos)` — handles multi-tile sliding: if clicked tile is in same row or column as empty, all tiles between slide at once
- `isSolvable()` — checks inversion parity + empty-row parity before accepting a shuffle
- Image display: scaled so shorter side fills the 480px board (`scale = 480 / min(472, 315)`), then horizontally center-cropped via `cropX` offset in `bgPos()`

## To preview

Open `index.html` directly in a browser, or serve locally:

```
python3 -m http.server 8080
```

bei jeder ànderung des projects neu committen und pushenl